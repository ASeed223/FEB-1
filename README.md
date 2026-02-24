import csv
import datetime
import os
from collections import defaultdict
from urllib.parse import urlparse
import requests

# Configuration
NEXUS_URL = "https://lxpd195:8444"
USERNAME = "nexus"
PASSWORD = "124124124?3212312412!leHFuywjW"
REPO_NAME = "SIP_Development"

DAYS_OLD = 365
KEEP_VERSIONS = 5

VERIFY_SSL = False
TIMEOUT_SECONDS = 30

BASE_DIR = r"C:\Users\C4387\Desktop\nexus_cleanup"
if not os.path.exists(BASE_DIR):
    os.makedirs(BASE_DIR)

parsed_url = urlparse(NEXUS_URL)
hostname = parsed_url.hostname or "unknown_host"

report_filename = f"cleanup_candidates_{hostname}_{REPO_NAME}.csv"
CSV_REPORT_FILE = os.path.join(BASE_DIR, report_filename)

requests.packages.urllib3.disable_warnings()

def parse_nexus_iso(dt_str):
    if not dt_str:
        return datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)
    s = str(dt_str).strip()
    try:
        base = s[:19]
        dt = datetime.datetime.strptime(base, "%Y-%m-%dT%H:%M:%S")
        return dt.replace(tzinfo=datetime.timezone.utc)
    except Exception:
        return datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)

def safe_int(v, default=0):
    try:
        if v is None:
            return default
        return int(v)
    except Exception:
        return default

def analyze_component(component):
    assets = component.get("assets") or []
    epoch = datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)

    if not assets:
        return epoch, epoch, 0, 0, 0

    publish_dates = []
    used_dates = []
    total_bytes = 0
    total_downloads = 0

    for a in assets:
        total_bytes += safe_int(a.get("fileSize"), 0)
        total_downloads += safe_int(a.get("downloadCount"), 0)
        
        p_dt = parse_nexus_iso(a.get("lastModified"))
        publish_dates.append(p_dt)
        
        d_str = a.get("lastDownloaded")
        used_dates.append(parse_nexus_iso(d_str) if d_str else p_dt)

    return max(publish_dates), max(used_dates), total_bytes, total_downloads, len(assets)

def fetch_all_components(session):
    components = []
    url = f"{NEXUS_URL}/service/rest/beta/components"
    params = {"repository": REPO_NAME}

    while True:
        r = session.get(url, params=params, timeout=TIMEOUT_SECONDS, verify=VERIFY_SSL)
        if r.status_code != 200:
            raise RuntimeError(f"Fetch failed status={r.status_code} body={r.text}")

        data = r.json() or {}
        items = data.get("items") or []
        components.extend(items)

        token = data.get("continuationToken")
        if not token:
            break

        params = {"repository": REPO_NAME, "continuationToken": token}
        print(f"Fetched {len(components)} components...")

    return components

def run_rigorous_scan():
    print("--- Nexus Cleanup Scan Started ---")
    print(f"Host: {hostname}")
    print(f"Repository: {REPO_NAME}")
    print(f"Policy: Delete images idle > {DAYS_OLD} days (Keeping top {KEEP_VERSIONS} newest)")
    print(f"Output File: {CSV_REPORT_FILE}")
    print("----------------------------------")

    session = requests.Session()
    session.auth = (USERNAME, PASSWORD)
    session.verify = VERIFY_SSL

    try:
        components = fetch_all_components(session)
    except Exception as e:
        print(f"Fetch error: {e}")
        return

    grouped = defaultdict(list)
    for comp in components:
        name = comp.get("name")
        if name:
            grouped[name].append(comp)

    now_utc = datetime.datetime.now(datetime.timezone.utc)
    cutoff_dt = now_utc - datetime.timedelta(days=DAYS_OLD)

    candidates = []
    total_freed_bytes = 0

    for name, versions in grouped.items():
        for comp in versions:
            p_dt, u_dt, size, d_count, a_count = analyze_component(comp)
            comp["_publish_dt"] = p_dt
            comp["_used_dt"] = u_dt
            comp["_size"] = size
            comp["_total_downloads"] = d_count
            comp["_asset_count"] = a_count

        versions.sort(key=lambda x: x["_publish_dt"], reverse=True)

        for comp in versions[KEEP_VERSIONS:]:
            if comp["_used_dt"] < cutoff_dt:
                total_freed_bytes += comp["_size"]
                age_days = (now_utc - comp["_publish_dt"]).days
                idle_days = (now_utc - comp["_used_dt"]).days

                candidates.append(
                    {
                        "Repository": REPO_NAME,
                        "Image Path": name,
                        "Version/Tag": comp.get("version", ""),
                        "Size (MB)": round(comp["_size"] / (1024 * 1024), 2),
                        "Last Downloaded": comp["_used_dt"].strftime("%Y-%m-%d"),
                        "Days Idle": idle_days,
                        "Publish Date": comp["_publish_dt"].strftime("%Y-%m-%d"),
                        "Age (Days)": age_days,
                        "Total Downloads": comp["_total_downloads"],
                        "Asset Count": comp["_asset_count"],
                        "Justification": f"Idle > {DAYS_OLD} days, not in top {KEEP_VERSIONS}",
                        "Component ID": comp.get("id", "")
                    }
                )

    total_gb = total_freed_bytes / (1024 * 1024 * 1024)

    print("\n--- Scan Complete ---")
    print(f"Total Components Analyzed: {len(components)}")
    print(f"Cleanup Candidates Found: {len(candidates)}")
    print(f"Estimated Space to Free: {total_gb:.2f} GB")

    if not candidates:
        print("No candidates found. Exiting.")
        return

    try:
        with open(CSV_REPORT_FILE, mode="w", encoding="utf-8-sig", newline="") as f:
            fieldnames = [
                "Repository",
                "Image Path",
                "Version/Tag",
                "Size (MB)",
                "Last Downloaded",
                "Days Idle",
                "Publish Date",
                "Age (Days)",
                "Total Downloads",
                "Asset Count",
                "Justification",
                "Component ID"
            ]
            writer = csv.DictWriter(f, fieldnames=fieldnames)
            writer.writeheader()
            writer.writerows(candidates)

        print(f"Report successfully written to: {CSV_REPORT_FILE}")

    except Exception as e:
        print(f"CSV write error: {e}")

if __name__ == "__main__":
    run_rigorous_scan()
