Scan started
NexusHost: lxpd195
Repository: SIP_Development
Policy: idle>730 days and keep newest 10 versions by publish date
Output: C:\Users\C4387\Desktop\nexus_cleanup\cleanup_candidates_lxpd195_SIP_Development.csv
ClusterCheck: True
Scanning cluster NON_PROD (https://api.ocpnprcl01.ftb.ca.gov:6443/)
Traceback (most recent call last):
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\urllib3\connection.py", line 175, in _new_conn
    (self._dns_host, self.port), self.timeout, **extra_kw
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\urllib3\util\connection.py", line 72, in create_connection
    for res in socket.getaddrinfo(host, port, family, socket.SOCK_STREAM):
  File "C:\Program Files\Python37\lib\socket.py", line 748, in getaddrinfo
    for res in _socket.getaddrinfo(host, port, family, type, proto, flags):
socket.gaierror: [Errno 11001] getaddrinfo failed

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\urllib3\connectionpool.py", line 723, in urlopen
    chunked=chunked,
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\urllib3\connectionpool.py", line 404, in _make_request
    self._validate_conn(conn)
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\urllib3\connectionpool.py", line 1061, in _validate_conn
    conn.connect()
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\urllib3\connection.py", line 363, in connect
    self.sock = conn = self._new_conn()
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\urllib3\connection.py", line 187, in _new_conn
    self, "Failed to establish a new connection: %s" % e
urllib3.exceptions.NewConnectionError: <urllib3.connection.HTTPSConnection object at 0x0000026BD6A76710>: Failed to establish a new connection: [Errno 11001] getaddrinfo failed

During handling of the above exception, another exception occurred:

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
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\kubernetes\client\rest.py", line 221, in request
    headers=headers)
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\urllib3\connectionpool.py", line 843, in urlopen
    **response_kw
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\urllib3\connectionpool.py", line 843, in urlopen
    **response_kw
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\urllib3\connectionpool.py", line 843, in urlopen
    **response_kw
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\urllib3\connectionpool.py", line 803, in urlopen
    method, url, error=e, _pool=self, _stacktrace=sys.exc_info()[2]
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\urllib3\util\retry.py", line 594, in increment
    raise MaxRetryError(_pool, url, error or ResponseError(cause))
urllib3.exceptions.MaxRetryError: HTTPSConnectionPool(host='https', port=443): Max retries exceeded with url: //api.ocpnprcl01.ftb.ca.gov:6443//api/v1/pods?limit=500&watch=False (Caused by NewConnectionError('<urllib3.connection.HTTPSConnection object at 0x0000026BD6A76710>: Failed to establish a new connection: [Errno 11001] getaddrinfo failed'))
PS C:\Users\C4387>
