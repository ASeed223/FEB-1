import csv
import os
import time
import datetime
import requests

# Configuration
NEXUS_URL = "https://lxpd195:8444"
USERNAME = "nexus"
PASSWORD = os.getenv("NEXUS_PASSWORD", "your_password_here")

CSV_FILE = r"C:\Users\C4387\Desktop\nexus_cleanup\cleanup_candidates_lxpd195_SIP_Development_DeepScan.csv"

VERIFY_SSL = False
TIMEOUT_SECONDS = 30
SLEEP_SECONDS = 0.05

DRY_RUN = True

BASE_DIR = r"C:\Users\C4387\Desktop\nexus_cleanup"
os.makedirs(BASE_DIR, exist_ok=True)

timestamp = datetime.datetime.now().strftime("%Y%m%d_%H%M%S")
REPORT_FILE = os.path.join(BASE_DIR, f"deletion_audit_{timestamp}.txt")

requests.packages.urllib3.disable_warnings()


def safe_float(v, default=0.0):
    try:
        if v is None:
            return default
        s = str(v).strip()
        if not s:
            return default
        return float(s)
    except Exception:
        return default


def execute_mass_deletion():
    if not os.path.exists(CSV_FILE):
        print(f"CSV file not found: {CSV_FILE}")
        return

    start_time = datetime.datetime.now()

    success_count = 0
    fail_count = 0
    skip_count = 0
    deleted_mb = 0.0

    with open(REPORT_FILE, mode="w", encoding="utf-8") as log_file:

        def log(msg):
            print(msg)
            log_file.write(msg + "\n")

        log("=" * 70)
        log("Nexus Mass Deletion Audit")
        log("=" * 70)
        log(f"StartTime: {start_time.strftime('%Y-%m-%d %H:%M:%S')}")
        log(f"NexusURL: {NEXUS_URL}")
        log(f"CSVFile: {CSV_FILE}")
        log(f"DryRun: {DRY_RUN}")
        log("=" * 70)
        log("")

        session = requests.Session()
        session.auth = (USERNAME, PASSWORD)
        session.verify = VERIFY_SSL

        with open(CSV_FILE, mode="r", encoding="utf-8-sig", newline="") as f:
            reader = csv.DictReader(f)
            rows = list(reader)

        total_items = len(rows)
        log(f"TotalRows: {total_items}")
        log("")

        for index, row in enumerate(rows, 1):
            comp_id = (row.get("Component ID") or "").strip()
            name = (row.get("Name") or "").strip()
            version = (row.get("Version") or "").strip()
            size_mb = safe_float(row.get("Size (MB)"), 0.0)

            if not comp_id:
                log(f"{index}/{total_items} SKIP MissingComponentId name={name} version={version}")
                skip_count += 1
                continue

            del_url = f"{NEXUS_URL}/service/rest/v1/components/{comp_id}"

            if DRY_RUN:
                log(f"{index}/{total_items} DRYRUN Delete name={name} version={version} sizeMB={size_mb:.2f} id={comp_id}")
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
                log(f"{index}/{total_items} OK Deleted name={name} version={version} sizeMB={size_mb:.2f} id={comp_id}")
                success_count += 1
                deleted_mb += size_mb
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
        duration = end_time - start_time
        deleted_gb = deleted_mb / 1024.0

        log("")
        log("=" * 70)
        log("Summary")
        log("=" * 70)
        log(f"EndTime: {end_time.strftime('%Y-%m-%d %H:%M:%S')}")
        log(f"Duration: {duration}")
        log(f"Deleted: {success_count}")
        log(f"Failed: {fail_count}")
        log(f"Skipped: {skip_count}")
        if not DRY_RUN:
            log(f"DeletedSizeGB: {deleted_gb:.2f}")
        log("=" * 70)

        if not DRY_RUN:
            log("")
            log("NextSteps")
            log("Run blob store compaction in Nexus to reclaim disk space")

    print(f"Audit report written to: {REPORT_FILE}")


if __name__ == "__main__":
    execute_mass_deletion()
