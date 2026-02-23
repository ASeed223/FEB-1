import csv
import os
import time
import datetime
import requests

# Configuration
NEXUS_URL = "https://lxpd195:8444"
USERNAME = "nexus"
PASSWORD = "cs12312314!leHFuywjW"
CSV_FILE = r"C:\Users\C4387\Desktop\nexus_cleanup\ultimate_cleanup_candidates.csv"
VERIFY_SSL = False
TIMEOUT_SECONDS = 30
SLEEP_SECONDS = 0.05

DRY_RUN = False  # Set True to test without deleting

REPORT_FILE = "mass_deletion_report.txt"

requests.packages.urllib3.disable_warnings()


def execute_mass_deletion():
    if not os.path.exists(CSV_FILE):
        print(f"File not found: {CSV_FILE}")
        return

    start_time = datetime.datetime.now()

    success_count = 0
    fail_count = 0
    skip_count = 0

    with open(REPORT_FILE, mode="w", encoding="utf-8") as log_file:

        def log(msg: str) -> None:
            print(msg)
            log_file.write(msg + "\n")

        log("Mass deletion job started")
        log(f"StartTime: {start_time.strftime('%Y-%m-%d %H:%M:%S')}")
        log(f"NexusURL: {NEXUS_URL}")
        log(f"CSVFile: {CSV_FILE}")
        log(f"DryRun: {DRY_RUN}")
        log("")

        session = requests.Session()
        session.auth = (USERNAME, PASSWORD)
        session.verify = VERIFY_SSL

        with open(CSV_FILE, mode="r", encoding="utf-8-sig", newline="") as file:
            reader = csv.DictReader(file)
            rows = list(reader)

        total_items = len(rows)
        log(f"TotalRows: {total_items}")
        log("")

        for index, row in enumerate(rows, 1):
            comp_id = (row.get("Component ID") or "").strip()
            name = (row.get("Name") or "").strip()
            version = (row.get("Version") or "").strip()

            if not comp_id:
                log(f"{index}/{total_items} SKIP MissingComponentId name={name} version={version}")
                skip_count += 1
                continue

            del_url = f"{NEXUS_URL}/service/rest/v1/components/{comp_id}"

            if DRY_RUN:
                log(f"{index}/{total_items} DRYRUN Delete name={name} version={version} id={comp_id}")
                time.sleep(SLEEP_SECONDS)
                continue

            try:
                r = session.delete(del_url, timeout=TIMEOUT_SECONDS)
            except Exception as e:
                log(f"{index}/{total_items} FAIL DeleteRequest name={name} version={version} id={comp_id} error={e}")
                fail_count += 1
                time.sleep(SLEEP_SECONDS)
                continue

            if r.status_code == 204:
                log(f"{index}/{total_items} OK Deleted name={name} version={version} id={comp_id}")
                success_count += 1
            elif r.status_code == 404:
                log(f"{index}/{total_items} SKIP NotFound name={name} version={version} id={comp_id}")
                skip_count += 1
            elif r.status_code == 401:
                log(f"{index}/{total_items} FAIL Unauthorized name={name} version={version} id={comp_id}")
                fail_count += 1
            else:
                log(f"{index}/{total_items} FAIL DeleteStatus name={name} version={version} id={comp_id} status={r.status_code} body={r.text}")
                fail_count += 1

            time.sleep(SLEEP_SECONDS)

        end_time = datetime.datetime.now()

        log("")
        log("Job summary")
        log(f"EndTime: {end_time.strftime('%Y-%m-%d %H:%M:%S')}")
        log(f"Deleted: {success_count}")
        log(f"Failed: {fail_count}")
        log(f"Skipped: {skip_count}")
        log("")
        log("Next steps")
        log("Run repository cleanup and blob store compaction tasks in Nexus to reclaim disk space")

    print(f"Report written to: {REPORT_FILE}")


if __name__ == "__main__":
    execute_mass_deletion()
