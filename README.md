#!/usr/bin/python3

"""
File:   purge_images.py
Author: Sam Peterson
Modified for Nexus By: Brandon Urban

This is the main python script which is used to clean up the Nexus docker registry for OCP images.

This script requires 4 configuration parameters as environment variables:

    REG_HOST_PORT - The registry host to connect to (optionally including port)
    REG_USERNAME  - The username for repository login
    REG_PASSWORD  - The password for repository login

    ACTUALLY_DELETE - If set to 'true' will actually cause deletions, rather
                      than simply echoing the skopeo commands to the log.
                      Variable can be ommitted, in which case it's false.

Optionally, a third configuration parameter determines the prefixes of the
repositories that purging will be limited to. By default, ["ets/", "b2b/"] will be
used.

    REPO_PREFIXES  - json array of string prefixes to limit purging to.

The basic logic of the script is to discover all image sha256 urls not in use.
First, we inspect all image streams in the cluster. Then all docker repo tags
are inspected for their sha256 values. Then the set of those values, minus the
image stream values, is created, and that final list is sequentially deleted by
using "skopeo delete"

Note that disk space will not be cleared until garbage collection is run on the
respective docker registry. This should have already been configured to run hourly
on the DMZ registries. Once garbage collection is run, it is important that the
registry is restarted as well.

"""

import subprocess as sub
import sys
import json
import os
import pprint
import argparse
import logging
import getpass
import urllib3
import requests
import openshift_client as oc
import openshift
import pprint
import base64
from requests.auth import HTTPBasicAuth
from typing import List, Tuple, Set
from kubernetes import client, config
from kubernetes.config.config_exception import ConfigException
from urllib3.exceptions import InsecureRequestWarning
from urllib.parse import urlparse
from openshift.dynamic import DynamicClient
from openshift.helper.userpassauth import OCPLoginConfiguration

logging.basicConfig(level=logging.INFO,
        format="%(asctime)s %(levelname)s - %(filename)s: %(message)s")

def parse_args():
    parser = argparse.ArgumentParser(description="Clean up unused Nexus images by comparing with OCP clusters")

    # Core Nexus parameters
    parser.add_argument("--nexusHost", required=False, help="Nexus repository hostname")
    parser.add_argument("--nexusUsername", required=False, help="Nexus login username")
    parser.add_argument("--nexusPassword", required=False, help="Nexus login password")
    parser.add_argument("--nexusRepo", action="append", required=False, help="Name(s) of the Nexus repository")
    
    # OpenShift clusters
    parser.add_argument("--nonConfClusterHost", required=True, help="Non-confidential OpenShift cluster host")
    parser.add_argument("--confClusterHost", required=False, help="Confidential OpenShift cluster host")

    # Cluster auth options
    parser.add_argument("--nonConfUsername", required=True, help="Non-Conf cluster username")
    parser.add_argument("--nonConfToken", required=True, help="Bearer token for non-conf OCP cluster")
    parser.add_argument("--confUsername", required=False,help="Conf cluster username")
    parser.add_argument("--confToken", required=False, help="Bearer token for confidential OCP cluster")
    parser.add_argument("--maxResultPages",required=False,const=50, nargs='?', type=int, help="Max number of pages for returned results.")
    return parser.parse_args()

def get_images_from_cluster(cluster_host, token=None, verify_ssl=True, auth_mode=None):
    logging.info(f"Connecting to OpenShift cluster at {cluster_host}")
    configuration = client.Configuration()
    configuration.host = f"https://{cluster_host}"
    configuration.verify_ssl = verify_ssl
    configuration.ssl_ca_cert = "/home/cmdeploy/burban/nonprod.pem"
    try:
        configuration.api_key = {"authorization": f"Bearer {token}"}
        logging.debug("Using bearer token authentication")
    except Exception as e:
        logging.error(f"Error fetching pod data from {cluster_host}: {e}")
        return set()

    # Use manual configuration    
    api_client = client.ApiClient(configuration)
    v1 = client.CoreV1Api(api_client)
    images = set()
    try:       
        pod_list = v1.list_pod_for_all_namespaces(watch=False)
        for pod in pod_list.items:
            for container in pod.spec.containers:
                images.add(container.image)
            if pod.spec.init_containers:
                for init in pod.spec.init_containers:
                    images.add(init.image)
    except Exception as e:
        logging.error(f"Error fetching pod data from {cluster_host}: {e}")
        return set()
    logging.info(f"Found {len(images)} unique images in use on {cluster_host}")    
    logging.info(f"The following images were found:\n {pprint.pprint(images)} ")
    return images

def get_imagestreams_from_cluster(cluster_host, token=None, verify_ssl=True, auth_mode=None):
    logging.info(f"Connecting to OpenShift cluster at {cluster_host}")
    configuration = client.Configuration()
    configuration.host = f"https://{cluster_host}"
    configuration.verify_ssl = verify_ssl
    configuration.api_key =  {"authorization": f"Bearer {token}" }    
    # Use manual configuration    
    theClient = client.ApiClient(configuration)    
    api_client = DynamicClient(theClient)    
    ets_pods = []
    used_images= set()
    tags = set()
    validNamespaces = "ets-tst1a,ets-tst1b,ets-tst2a,ets-tst2b,ets-tst2c,ets-tst2d"
    namespaceList = validNamespaces.split(',')
    for namespace in namespaceList:        
        try:            
            imagestream_api = api_client.resources.get(api_version='image.openshift.io/v1', kind='ImageStream')            
            # List imagestreams in the specified namespace
            imagestreams = imagestream_api.get(namespace=namespace)

            if imagestreams.items:                
                for iStream in imagestreams.items:                    
                    streamName = iStream.metadata.name
                    imageStream = imagestream_api.get(name=streamName, namespace=namespace)
                    if(imageStream.spec.tags):
                        print(f"Tags for ImageStream '{streamName}' in namespace '{namespace}':")
                        for tag in imageStream.spec.tags:                            
                            if tag["from"]:
                                tagKind = tag["from"]
                                if tagKind.kind == 'DockerImage':
                                    print(f"    Source Docker Image: {tagKind.name}")                                
                                else:
                                    print(f"Could not find a tag type of DockerImage for ImageStream '{streamName}' in '{namespace}'.")
                            else:
                                print(f"Could not retrieve tags for ImageStream '{streamName}' in '{namespace}'.")
                    else:
                        print(f"No tags found for ImageStream '{streamName}' in '{namespace}'")
            else:
                print(f"No imagestreams found in namespace '{namespace}'.")
        except client.ApiException as e:
            print(f"Error listing Image Streams: {e}")
            return set()
        logging.info(f"Found {len(tags)} unique images in use on {cluster_host}")    
        logging.info(f"The following images were found:\n {pprint.pprint(tags)} ")
    return tags


def get_images_from_nexus(nexus_host, username, password, repo, verify_ssl=True, max_pages=50):
    logging.info("Fetching images from Nexus...")    
    base_url = f"https://{nexus_host}/service/rest/v1/components?repository={repo}"
    all_images = set()    
    continuation_token = None        
    page = 0
    while True:
        if page >= max_pages:
            logging.warning(f"Reached maxPages ({max_pages}) for repo '{repo}' — stopping pagination")
            break       
        if continuation_token:
            params["continuationToken"] = continuation_token

        response = requests.get(
            base_url,
            auth=HTTPBasicAuth(username, password),
            verify=verify_ssl
        )

        if response.status_code != 200:
            logging.error(f"Failed to fetch from Nexus ({repo}): {response.status_code} - {response.text}")
            break
        data = response.json()
        for item in data.get("items", []):           
            image_name = item.get("name")
            for asset in item.get("assets", []):
                tag = asset.get("attributes", {}).get("docker", {}).get("tag")
                if image_name and tag:
                    full_name = f"{repo}/{image_name}:{tag}"
                    all_images.add(full_name)

        continuation_token = data.get("continuationToken")
        if not continuation_token:
            break
        page += 1
    logging.info(f"Fetched {len(all_images)} total images from Nexus.")
    return all_images

def get_specific_project_images_from_nexus(nexus_host, username, password, repo, project_list, release_list, verify_ssl=True, max_pages=50):
    logging.info("Fetching images from Nexus...")    
    base_url = f"https://{nexus_host}/service/rest/v1/components?repository={repo}"
    all_images = []        
    continuation_token = None        
    page = 0
    
    while True:
        params = {}
        print(f"Page # {page}")
        if page >= max_pages:
            logging.warning(f"Reached maxPages ({max_pages}) for repo '{repo}' — stopping pagination")
            break
        
        if continuation_token:
            params["continuationToken"] = continuation_token        

        response = requests.get(
            base_url,
            auth=(username, password),
            params=params,
            verify=verify_ssl
        )

        if response.status_code != 200:
            logging.error(f"Failed to fetch from Nexus ({repo}): {response.status_code} - {response.text}")
            break
        data = response.json()
        for item in data.get("items", []):
            image_name = item.get("name")
            print(f"Checking item: {image_name}")
            img_proj = image_name.split("/", 1)
            print(f"image_name split: {img_proj}")
            project = img_proj[len(img_proj)-1]
            print(f"project: {project}")
            if project in project_list:                                                    
                version = item.get("version")
                print(f"Found name: {project}")
                print(f"Found version: {version}")
                if image_name and version:                    
                    for release in release_list:
                        if release in version:
                            print("Found project name and release number.")
                            component_id = item.get("id")
                            full_name = f"{project}:{version}:{component_id}"
                            all_images.append(full_name)
        continuation_token = data.get("continuationToken")
        print(f"Continuation token: {continuation_token}")
        if not continuation_token:
            break
        page += 1
    all_images.sort()
    #pprint.pprint(all_images)
    logging.info(f"Fetched {len(all_images)} total images from Nexus.")
    return all_images

def delete_nexus_images(nexus_host, username, password, repo, image_path_list, verify_ssl=True, dry_run=True, max_pages=50):
    logging.info("Deleting unused images in Nexus...")
    base_url = f"https://{nexus_host}"    
    deleted_count = 0    
    kept_count = 0    
    for image_path in image_path_list:   
        print(f"current image path: {image_path}")
        image_data = image_path.split(':')
        component_name = image_data[0]
        component_version = image_data[1]
        component_id = image_data[2]
        if not dry_run:
            delete_url = f"{base_url}/service/rest/v1/components/{component_id}"
            print(f"Delete URL: {delete_url}")
            del_resp = requests.delete(delete_url, auth=(username, password))
            if del_resp.status_code == 204:
                logging.info(f"Deleted {component_name} with image path: {image_path}")
                deleted_count += 1
            else:
                logging.error(f"Failed to delete {component_name}, version {component_version} with image path: {image_path}: {del_resp.status_code}")
        else:
            logging.info(f"[Dry-run] Would delete: {base_url}{image_path}")
            deleted_count += 1                        
    logging.info(f"Deletion summary: {deleted_count} deleted (or would be), {kept_count} kept")


def redact(s):
    return "****" if s else None 

def main():
    """Main"""
    args = parse_args()

    # Setup logging    
    logging.basicConfig(filename='~/burban/output.log', encoding='uft-8', level=logging.DEBUG, format="%(asctime)s [%(levelname)s] %(message)s")

    # Normalize SSL flag    
    verify_ssl = False
    nexusImages = []
    nexusUsername = 'f5593'
    nexusPassword = 'VegasR@iders2023'
    repo = 'SIP_Development'
    releaseList = ['25.1.']
    projectList = ['noticing-services-app','noticing-ui-app']
        
    nexusImages = get_specific_project_images_from_nexus(
            nexus_host = args.nexusHost, 
            username = nexusUsername, 
            password = nexusPassword, 
            repo = repo,
            project_list = projectList,
            release_list = releaseList,
            verify_ssl=verify_ssl,
            max_pages = args.maxResultPages
        )
    logging.info("Nexus images found:")
    logging.info(pprint.pprint(nexusImages))
        
    deleted_images = delete_nexus_images(
        nexus_host = args.nexusHost,
        username = nexusUsername,
        password = nexusPassword,
        repo = repo,
        image_path_list = nexusImages,
        dry_run = True
    )
    
    logging.info(pprint.pprint(deleted_images))


    #logging.info("Querying images from confidential cluster...")
    #conf_images = get_images_from_cluster(
    #    cluster_host=args.confClusterHost,
    #    token=args.confToken,
    #    verify_ssl=args.verify_ssl,
    #    auth_mode=args.clusterAuthMode
    #)

    #all_used_images = non_conf_images.union(conf_images)
    #logging.info(f"Total unique iU0lQX0RldmVsb3BtZW50Ojc1ODgwNTEwmages in use: {len(all_used_images)}")

    # Run cleanup    
    #delete_unused_nexus_images(
    #    nexus_host=args.nexusHost,
    #    username=args.nexusUsername,
    #    password=args.nexusPassword,
    #    repos=args.nexusRepo,
    #    used_images=all_used_images,
    #    verify_ssl=args.verify_ssl,
    #    dry_run=args.dry_run,
    #    max_pages=args.maxPages,
    #    protect_patterns=args.protectRegex,
    #    summary_log_path=args.logSummaryFile,
    #    summary_format=args.summaryFormat
    #)

if __name__ == "__main__":
    main()
