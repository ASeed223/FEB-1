Nexus Blob Store Pre-sync (lxpd195 to lxpd208)

Title: Nexus Blob Store Pre-sync (lxpd195 to lxpd208)

Description: Perform initial hot sync of ~2.7TB Blob Store data from lxpd195 to lxpd208 HA mount. Command: rsync -avzP -e ssh --bwlimit=100000 /opt/appdata/nexus/sonatype-work/nexus3/blobs/ cmdeploy@lxpd208:/opt/appdata/nexus/sonatype-work/nexus3/blobs/
