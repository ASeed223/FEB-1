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

CSV_REPORT_FILE = "ultimate_cleanup_candidates.csv"

VERIFY_SSL = False
TIMEOUT_SECONDS = 30

requests.packages.urllib3.disable_warnings()


def parse_nexus_iso(dt_str):
    if not dt_str:
        return datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)

    s = dt_str.strip()

    # Handle: 2025-01-02T03:04:05.678Z
    # Handle: 2025-01-02T03:04:05Z
    # Handle: 2025-01-02T03:04:05.678+00:00 (rare)
    try:
        base = s[:19]  # YYYY-MM-DDTHH:MM:SS
        dt = datetime.datetime.strptime(base, "%Y-%m-%dT%H:%M:%S")
        return dt.replace(tzinfo=datetime.timezone.utc)
    except Exception:
        return datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)


def get_asset_last_active_dt(asset):
    dt_str = asset.get("lastDownloaded") or asset.get("lastModified")
    return parse_nexus_iso(dt_str)


def get_component_last_active_dt(component):
    assets = component.get("assets") or []
    if not assets:
        return datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)
    return max(get_asset_last_active_dt(a) for a in assets)


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


def run_cleanup_dryrun():
    print("Starting scan")
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

    print(f"Total components: {len(components)}")

    grouped = defaultdict(list)
    for comp in components:
        name = comp.get("name")
        if name:
            grouped[name].append(comp)

    cutoff_dt = datetime.datetime.now(datetime.timezone.utc) - datetime.timedelta(days=DAYS_OLD)

    candidates = []

    for name, versions in grouped.items():
        for comp in versions:
            comp["_last_active_dt"] = get_component_last_active_dt(comp)

        versions.sort(key=lambda x: x["_last_active_dt"], reverse=True)

        for comp in versions[KEEP_VERSIONS:]:
            last_active = comp["_last_active_dt"]
            if last_active < cutoff_dt:
                candidates.append(
                    {
                        "Name": name,
                        "Version": comp.get("version", ""),
                        "Component ID": comp.get("id", ""),
                        "Last Active Date": last_active.isoformat(),
                        "Reason": f"Older than {DAYS_OLD} days and not in top {KEEP_VERSIONS}",
                    }
                )

    print(f"Candidates: {len(candidates)}")

    if not candidates:
        print("No candidates found")
        return

    try:
        with open(CSV_REPORT_FILE, mode="w", encoding="utf-8-sig", newline="") as f:
            fieldnames = ["Name", "Version", "Component ID", "Last Active Date", "Reason"]
            writer = csv.DictWriter(f, fieldnames=fieldnames)
            writer.writeheader()
            writer.writerows(candidates)

        print(f"Report written: {CSV_REPORT_FILE}")

    except Exception as e:
        print(f"CSV write error: {e}")


if __name__ == "__main__":
    run_cleanup_dryrun()
