import requests

# ============== Update these values ==============
NEXUS_URL = "https://lxpd208:8443"
USERNAME = "nexus"
PASSWORD = "1234?231245!leHFuywjW"
# =================================================

REPO_NAME = "SIP_Development"

requests.packages.urllib3.disable_warnings()


def test_connection():
    print(f"Testing connection to {NEXUS_URL}")

    search_url = f"{NEXUS_URL}/service/rest/v1/search"
    params = {
        "repository": REPO_NAME,
        "count": 1
    }

    try:
        r = requests.get(
            search_url,
            auth=(USERNAME, PASSWORD),
            params=params,
            verify=False
        )

        if r.status_code == 200:
            print("Connection successful")
            data = r.json()
            items = data.get("items", [])

            if items:
                print(f"Found component: {items[0]['name']}")
                print("Access and network look good")
            else:
                print("Connected but no component found. Check repository name")

        elif r.status_code == 401:
            print("Unauthorized. Check username or password")

        else:
            print(f"Request failed with status code {r.status_code}")
            print(r.text)

    except Exception as e:
        print(f"Connection error: {e}")


if __name__ == "__main__":
    test_connection()


    Traceback (most recent call last):
  File "c:/Users/C4387/Desktop/nexus_cleaner.py", line 1, in <module>
    import requests
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\requests\__init__.py", line 43, in <module>
    import urllib3
  File "C:\Users\C4387\AppData\Roaming\Python\Python37\site-packages\urllib3\__init__.py", line 42, in <module>
    "urllib3 v2.0 only supports OpenSSL 1.1.1+, currently "
ImportError: urllib3 v2.0 only supports OpenSSL 1.1.1+, currently the 'ssl' module is compiled with 'OpenSSL 1.1.0j  20 Nov 2018'. See: https://github.com/urllib3/urllib3/issues/2168
