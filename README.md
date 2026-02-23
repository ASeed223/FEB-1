PS C:\Users\C4387> & "C:/Program Files/Python37/python.exe" c:/Users/C4387/Desktop/nexus_cleanup/nexus_cleaner_OCP.py
Scan started
NexusHost: lxpd195
Repository: SIP_Development
Policy: idle>730 days and keep newest 10 versions by publish date
Output: C:\Users\C4387\Desktop\nexus_cleanup\cleanup_candidates_lxpd195_SIP_Development.csv
ClusterCheck: True
Scanning cluster NON_PROD (api.ocpnprcl01.ftb.ca.gov:6443/)
Traceback (most recent call last):
  File "c:/Users/C4387/Desktop/nexus_cleanup/nexus_cleaner_OCP.py", line 343, in <module>
    run_rigorous_scan()
  File "c:/Users/C4387/Desktop/nexus_cleanup/nexus_cleaner_OCP.py", line 227, in run_rigorous_scan
    active_images_map = get_active_images_from_all_clusters()
  File "c:/Users/C4387/Desktop/nexus_cleanup/nexus_cleaner_OCP.py", line 195, in get_active_images_from_all_clusters
    _continue=continue_token,
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\kubernetes\client\api\core_v1_api.py", line 17630, in list_pod_for_all_namespaces
    return self.list_pod_for_all_namespaces_with_http_info(**kwargs)  # noqa: E501
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\kubernetes\client\api\core_v1_api.py", line 17755, in list_pod_for_all_namespaces_with_http_info
    collection_formats=collection_formats)
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\kubernetes\client\api_client.py", line 353, in call_api     
    _preload_content, _request_timeout, _host)
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\kubernetes\client\api_client.py", line 184, in __call_api   
    _request_timeout=_request_timeout)
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\kubernetes\client\api_client.py", line 377, in request      
    headers=headers)
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\kubernetes\client\rest.py", line 248, in GET
    query_params=query_params)
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\kubernetes\client\rest.py", line 238, in request
    raise ApiException(http_resp=r)
kubernetes.client.exceptions.ApiException: (401)
Reason: Unauthorized
HTTP response headers: HTTPHeaderDict({'Audit-Id': 'd2e91637-0d43-4f93-9f3c-307c41b00bba', 'Cache-Control': 'no-cache, private', 'Content-Type': 'application/json', 'Strict-Transport-Security': 'max-age=31536000; includeSubDomains; preload', 'Date': 'Mon, 23 Feb 2026 20:11:22 GMT', 'Content-Length': '129'})
HTTP response body: {"kind":"Status","apiVersion":"v1","metadata":{},"status":"Failure","message":"Unauthorized","reason":"Unauthorized","code":401}
