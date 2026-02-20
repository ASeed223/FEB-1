import csv
import os
import time
import requests

# Configuration
NEXUS_URL = "https://lxpd208:8443"
USERNAME = "nexus"
PASSWORD = os.getenv("NEXUS_PASSWORD", "your_password_here")
REPO_NAME = "SIP_Development"
CSV_FILE = r"C:\Users\C4387\Desktop\nexus_cleanup\docker.csv"

# Request settings
VERIFY_SSL = False
TIMEOUT_SECONDS = 30
SLEEP_BETWEEN_DELETES_SECONDS = 0.2

requests.packages.urllib3.disable_warnings()


def find_component_ids(session: requests.Session, name: str, version: str) -> list[str]:
    url = f"{NEXUS_URL}/service/rest/v1/search"
    params = {
        "repository": REPO_NAME,
        "name": name,
        "version": version,
    }

    r = session.get(url, params=params, timeout=TIMEOUT_SECONDS)
    if r.status_code != 200:
        raise RuntimeError(f"Search failed for {name}:{version} status={r.status_code} body={r.text}")

    data = r.json()
    items = data.get("items") or []

    ids = []
    for item in items:
        item_name = item.get("name")
        item_version = item.get("version")
        item_id = item.get("id")
        if item_id and item_name == name and item_version == version:
            ids.append(item_id)

    return ids


def delete_component(session: requests.Session, comp_id: str) -> bool:
    url = f"{NEXUS_URL}/service/rest/v1/components/{comp_id}"
    r = session.delete(url, timeout=TIMEOUT_SECONDS)
    return r.status_code == 204


def start_deletion():
    if not os.path.exists(CSV_FILE):
        print(f"File not found: {CSV_FILE}")
        print("Make sure the CSV file path is correct")
        return

    success_count = 0
    fail_count = 0
    skip_count = 0

    print("Starting deletion job")
    print(f"NexusURL: {NEXUS_URL}")
    print(f"Repository: {REPO_NAME}")
    print(f"CSV: {CSV_FILE}")

    session = requests.Session()
    session.auth = (USERNAME, PASSWORD)
    session.verify = VERIFY_SSL

    try:
        with open(CSV_FILE, mode="r", encoding="utf-8-sig", newline="") as file:
            reader = csv.DictReader(file)

            for row in reader:
                name = (row.get("Name") or "").strip()
                version = (row.get("Version") or "").strip()

                if not name:
                    continue

                if not version:
                    print(f"Skipping item with missing Version: {name}")
                    skip_count += 1
                    continue

                try:
                    comp_ids = find_component_ids(session, name, version)
                except Exception as e:
                    print(f"Search error for {name}:{version} error={e}")
                    fail_count += 1
                    continue

                if not comp_ids:
                    print(f"Not found: {name}:{version}")
                    skip_count += 1
                    continue

                deleted_any = False
                for comp_id in comp_ids:
                    ok = False
                    try:
                        ok = delete_component(session, comp_id)
                    except Exception as e:
                        print(f"Delete error for {name}:{version} id={comp_id} error={e}")
                        ok = False

                    if ok:
                        deleted_any = True
                        success_count += 1
                        print(f"Deleted: {name}:{version} id={comp_id}")
                    else:
                        fail_count += 1
                        print(f"Delete failed: {name}:{version} id={comp_id}")

                    time.sleep(SLEEP_BETWEEN_DELETES_SECONDS)

                if not deleted_any:
                    print(f"No deletions completed for: {name}:{version}")

    except Exception as e:
        print(f"Fatal error: {e}")

    print("Job finished")
    print(f"Deleted: {success_count}")
    print(f"Failed: {fail_count}")
    print(f"Skipped: {skip_count}")
    print("Run the appropriate cleanup task in Nexus if you need to reclaim disk space")


if __name__ == "__main__":
    start_deletion()
