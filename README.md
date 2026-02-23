import csv
import os
import requests

# Configuration
NEXUS_URL = "https://lxpd195:8444"
USERNAME = "nexus"
PASSWORD = os.getenv("NEXUS_PASSWORD", "your_password_here")

CSV_FILE = r"C:\Users\C4387\Desktop\nexus_cleanup\cleanup_candidates_lxpd195_SIP_Development.csv"

VERIFY_SSL = False
TIMEOUT_SECONDS = 10
PRINT_EVERY = 50

requests.packages.urllib3.disable_warnings()


def check_component_existence():
    if not os.path.exists(CSV_FILE):
        print(f"File not found: {CSV_FILE}")
        return

    exists_count = 0
    not_found_count = 0
    error_count = 0
    skip_count = 0

    session = requests.Session()
    session.auth = (USERNAME, PASSWORD)
    session.verify = VERIFY_SSL

    print("Starting component existence check")
    print(f"NexusURL: {NEXUS_URL}")
    print(f"CSVFile: {CSV_FILE}")

    with open(CSV_FILE, mode="r", encoding="utf-8-sig", newline="") as f:
        reader = csv.DictReader(f)
        rows = list(reader)

    total = len(rows)
    print(f"TotalRows: {total}")

    for i, row in enumerate(rows, 1):
        comp_id = (row.get("Component ID") or "").strip()
        name = (row.get("Name") or "").strip()
        version = (row.get("Version") or "").strip()

        if not comp_id:
            skip_count += 1
            continue

        url = f"{NEXUS_URL}/service/rest/v1/components/{comp_id}"

        try:
            r = session.get(url, timeout=TIMEOUT_SECONDS)

            if r.status_code == 200:
                exists_count += 1
                status = "EXISTS 200"
            elif r.status_code == 404:
                not_found_count += 1
                status = "NOT_FOUND 404"
            elif r.status_code == 401:
                error_count += 1
                status = "UNAUTHORIZED 401"
            else:
                error_count += 1
                status = f"ERROR {r.status_code}"

            if i % PRINT_EVERY == 0 or i == total:
                print(f"Progress {i}/{total} Current {name}:{version} Status {status}")

        except Exception as e:
            error_count += 1
            if i % PRINT_EVERY == 0 or i == total:
                print(f"Progress {i}/{total} Current {name}:{version} Status REQUEST_ERROR {e}")

    print("Summary")
    print(f"CheckedRows: {total}")
    print(f"Exists: {exists_count}")
    print(f"NotFound: {not_found_count}")
    print(f"Errors: {error_count}")
    print(f"SkippedMissingId: {skip_count}")

    if exists_count == 0 and not_found_count > 0:
        print("Result: all candidates are not found. Consider rebuilding search index")
    elif exists_count > 0:
        print("Result: some components still exist. Deletion may be incomplete")


if __name__ == "__main__":
    check_component_existence()
