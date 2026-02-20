import requests

# ============== Update these values ==============
NEXUS_URL = "https://lxpd208:8443"
USERNAME = "admin"
PASSWORD = "your_admin_password"
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
