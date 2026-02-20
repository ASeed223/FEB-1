import csv
import datetime
import os
from collections import defaultdict

import requests

# Configuration
NEXUS_URL = "https://lxpd208:8443"
USERNAME = "nexus"
PASSWORD = os.getenv("NEXUS_PASSWORD", "your_password_here")
REPO_NAME = "SIP_Development"

DAYS_OLD = 365
KEEP_VERSIONS = 10

BASE_DIR = r"C:\Users\C4387\Desktop\nexus_cleanup"
if not os.path.exists(BASE_DIR):
    os.makedirs(BASE_DIR)

CSV_REPORT_FILE = os.path.join(BASE_DIR, "ultimate_cleanup_candidates.csv")

VERIFY_SSL = False
TIMEOUT_SECONDS = 30

requests.packages.urllib3.disable_warnings()


def parse_nexus_iso(dt_str):
    if not dt_str:
        return datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)

    s = dt_str.strip()
    try:
        base = s[:19]  # YYYY-MM-DDTHH:MM:SS
        dt = datetime.datetime.strptime(base, "%Y-%m-%dT%H:%M:%S")
        return dt.replace(tzinfo=datetime.timezone.utc)
    except Exception:
        return datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)


def analyze_component(component):
    assets = component.get("assets") or []
    if not assets:
        epoch = datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)
        return epoch, epoch, 0

    publish_dates = []
    used_dates = []
    total_bytes = 0

    for a in assets:
        size = a.get("fileSize") or 0
        if not isinstance(size, int):
            try:
                size = int(size)
            except Exception:
                size = 0
        total_bytes += size

        p_dt = parse_nexus_iso(a.get("lastModified"))
        publish_dates.append(p_dt)

        d_str = a.get("lastDownloaded")
        if d_str:
            used_dates.append(parse_nexus_iso(d_str))
        else:
            used_dates.append(p_dt)

    return max(publish_dates), max(used_dates), total_bytes


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
    print("Starting scan")
    print(f"OutputDir: {BASE_DIR}")
    print(f"Repository: {REPO_NAME}")
    print(f"DaysOld: {DAYS_OLD}")
    print(f"KeepVersions: {KEEP_VERSIONS}")

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

    cutoff_dt = datetime.datetime.now(datetime.timezone.utc) - datetime.timedelta(days=DAYS_OLD)

    candidates = []
    total_freed_bytes = 0

    for name, versions in grouped.items():
        for comp in versions:
            p_dt, u_dt, size = analyze_component(comp)
            comp["_publish_dt"] = p_dt
            comp["_used_dt"] = u_dt
            comp["_size"] = size

        versions.sort(key=lambda x: x["_publish_dt"], reverse=True)

        for comp in versions[KEEP_VERSIONS:]:
            if comp["_used_dt"] < cutoff_dt:
                total_freed_bytes += comp["_size"]
                candidates.append(
                    {
                        "Name": name,
                        "Version": comp.get("version", ""),
                        "Component ID": comp.get("id", ""),
                        "Publish Date": comp["_publish_dt"].strftime("%Y-%m-%d"),
                        "Last Downloaded": comp["_used_dt"].strftime("%Y-%m-%d"),
                        "Size (MB)": round(comp["_size"] / (1024 * 1024), 2),
                        "Reason": f"Outside top {KEEP_VERSIONS} and last used before {cutoff_dt.strftime('%Y-%m-%d')}",
                    }
                )

    total_gb = total_freed_bytes / (1024 * 1024 * 1024)

    print("Report")
    print(f"ScannedComponents: {len(components)}")
    print(f"Candidates: {len(candidates)}")
    print(f"EstimatedMaxFreedGB: {total_gb:.2f}")

    if not candidates:
        print("No candidates found")
        return

    try:
        with open(CSV_REPORT_FILE, mode="w", encoding="utf-8-sig", newline="") as f:
            fieldnames = [
                "Name",
                "Version",
                "Component ID",
                "Publish Date",
                "Last Downloaded",
                "Size (MB)",
                "Reason",
            ]
            writer = csv.DictWriter(f, fieldnames=fieldnames)
            writer.writeheader()
            writer.writerows(candidates)

        print(f"Report written: {CSV_REPORT_FILE}")

    except Exception as e:
        print(f"CSV write error: {e}")


if __name__ == "__main__":
    run_rigorous_scan()
