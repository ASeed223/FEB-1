import csv
import datetime
import os
import time
import requests

# Configuration
NEXUS_URL = "https://lxpd208:8443"
USERNAME = "nexus"
PASSWORD = os.getenv("NEXUS_PASSWORD", "your_password_here")
REPO_NAME = "SIP_Development"

CSV_FILE = r"C:\Users\C4387\Desktop\nexus_cleanup\docker.csv"
REPORT_FILE = r"C:\Users\C4387\Desktop\nexus_cleanup\deletion_report.txt"

# Request settings
VERIFY_SSL = False
TIMEOUT_SECONDS = 30
SLEEP_BETWEEN_DELETES_SECONDS = 0.2

requests.packages.urllib3.disable_warnings()


def start_deletion():
    if not os.path.exists(CSV_FILE):
        print(f"File not found: {CSV_FILE}")
        return

    success_count = 0
    fail_count = 0
    skip_count = 0

    start_time = datetime.datetime.now()

    with open(REPORT_FILE, mode="w", encoding="utf-8") as log_file:

        def log(message: str) -> None:
            print(message)
            log_file.write(message + "\n")

        log("=" * 60)
        log("Nexus Bulk Deletion Audit Report")
        log(f"StartTime: {start_time.strftime('%Y-%m-%d %H:%M:%S')}")
        log(f"Repository: {REPO_NAME}")
        log(f"NexusURL: {NEXUS_URL}")
        log(f"CSV: {CSV_FILE}")
        log("=" * 60)
        log("")

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
                        log(f"SKIP MissingVersion name={name}")
                        skip_count += 1
                        continue

                    search_url = f"{NEXUS_URL}/service/rest/v1/search"
                    params = {"repository": REPO_NAME, "name": name, "version": version}

                    try:
                        r = session.get(search_url, params=params, timeout=TIMEOUT_SECONDS)
                    except Exception as e:
                        log(f"FAIL SearchRequest name={name} version={version} error={e}")
                        fail_count += 1
                        continue

                    if r.status_code != 200:
                        log(f"FAIL SearchStatus name={name} version={version} status={r.status_code}")
                        fail_count += 1
                        continue

                    items = (r.json() or {}).get("items") or []
                    if not items:
                        log(f"SKIP NotFound name={name} version={version}")
                        skip_count += 1
                        continue

                    deleted_any = False

                    for item in items:
                        comp_id = item.get("id")
                        if not comp_id:
                            continue

                        del_url = f"{NEXUS_URL}/service/rest/v1/components/{comp_id}"

                        try:
                            del_r = session.delete(del_url, timeout=TIMEOUT_SECONDS)
                        except Exception as e:
                            log(f"FAIL DeleteRequest name={name} version={version} id={comp_id} error={e}")
                            fail_count += 1
                            continue

                        if del_r.status_code == 204:
                            log(f"OK Deleted name={name} version={version} id={comp_id}")
                            success_count += 1
                            deleted_any = True
                        else:
                            log(f"FAIL DeleteStatus name={name} version={version} id={comp_id} status={del_r.status_code}")
                            fail_count += 1

                        time.sleep(SLEEP_BETWEEN_DELETES_SECONDS)

                    if not deleted_any:
                        log(f"FAIL NoDeletion name={name} version={version}")

        except Exception as e:
            log(f"FATAL CSVReadError error={e}")

        end_time = datetime.datetime.now()

        log("")
        log("=" * 60)
        log("Summary")
        log(f"EndTime: {end_time.strftime('%Y-%m-%d %H:%M:%S')}")
        log(f"Deleted: {success_count}")
        log(f"Failed: {fail_count}")
        log(f"Skipped: {skip_count}")
        log("=" * 60)
        log("")
        log("NextSteps")
        log("Run cleanup tasks in Nexus to reclaim disk space")
        log("1 Docker - Delete unused manifests and images")
        log("2 Admin - Compact blob store")

    print(f"Report written to: {REPORT_FILE}")


if __name__ == "__main__":
    start_deletion()
