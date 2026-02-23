import csv
import datetime
import os
from collections import defaultdict
from urllib.parse import urlparse

import requests

# Configuration
NEXUS_URL = "https://lxpd195:8444"
USERNAME = "nexus"
PASSWORD = os.getenv("NEXUS_PASSWORD", "your_password_here")
REPO_NAME = "SIP_Development"

DAYS_OLD = 730
KEEP_VERSIONS = 10

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
        base = s[:19]  # YYYY-MM-DDTHH:MM:SS
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
    url = f"{NEXUS_URL}/service/rest/v1/components"
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
        print(f"Fetched {len(components)} components")

    return components


def run_rigorous_scan():
    print("Scan started")
    print(f"Host: {hostname}")
    print(f"Repository: {REPO_NAME}")
    print(f"PolicyDaysOld: {DAYS_OLD}")
    print(f"KeepVersions: {KEEP_VERSIONS}")
    print(f"Output: {CSV_REPORT_FILE}")

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
                        "Format": comp.get("format", "docker"),
                        "Name": name,
                        "Version": comp.get("version", ""),
                        "Component ID": comp.get("id", ""),
                        "Publish Date": comp["_publish_dt"].strftime("%Y-%m-%d"),
                        "Age (Days)": age_days,
                        "Last Downloaded": comp["_used_dt"].strftime("%Y-%m-%d"),
                        "Days Idle": idle_days,
                        "Total Downloads": comp["_total_downloads"],
                        "Asset Count": comp["_asset_count"],
                        "Size (MB)": round(comp["_size"] / (1024 * 1024), 2),
                        "Justification": f"Idle>{DAYS_OLD} days and outside top {KEEP_VERSIONS} newest",
                    }
                )

    total_gb = total_freed_bytes / (1024 * 1024 * 1024)

    print("Scan complete")
    print(f"TotalComponents: {len(components)}")
    print(f"Candidates: {len(candidates)}")
    print(f"EstimatedSizeGB: {total_gb:.2f}")

    if not candidates:
        print("No candidates found")
        return

    try:
        with open(CSV_REPORT_FILE, mode="w", encoding="utf-8-sig", newline="") as f:
            fieldnames = [
                "Format",
                "Name",
                "Version",
                "Component ID",
                "Publish Date",
                "Age (Days)",
                "Last Downloaded",
                "Days Idle",
                "Total Downloads",
                "Asset Count",
                "Size (MB)",
                "Justification",
            ]
            writer = csv.DictWriter(f, fieldnames=fieldnames)
            writer.writeheader()
            writer.writerows(candidates)

        print(f"Report written: {CSV_REPORT_FILE}")

    except Exception as e:
        print(f"CSV write error: {e}")


if __name__ == "__main__":
    run_rigorous_scan()
