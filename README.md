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


def parse_nexus_iso(dt_str: str) -> datetime.datetime:
    if not dt_str:
        return datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)

    s = dt_str.strip()
    if s.endswith("Z"):
        s = s[:-1] + "+00:00"

    # Nexus commonly returns: 2025-01-02T03:04:05.678Z
    # datetime.fromisoformat supports offsets and fractional seconds
    try:
        dt = datetime.datetime.fromisoformat(s)
    except ValueError:
        # Fallback for odd formats
        try:
            dt = datetime.datetime.strptime(dt_str, "%Y-%m-%dT%H:%M:%S.%fZ").replace(
                tzinfo=datetime.timezone.utc
            )
        except ValueError:
            try:
                dt = datetime.datetime.strptime(dt_str, "%Y-%m-%dT%H:%M:%SZ").replace(
                    tzinfo=datetime.timezone.utc
                )
            except ValueError:
                dt = datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)

    if dt.tzinfo is None:
        dt = dt.replace(tzinfo=datetime.timezone.utc)

    return dt.astimezone(datetime.timezone.utc)


def get_asset_last_active_dt(asset: dict) -> datetime.datetime:
    dt_str = asset.get("lastDownloaded") or asset.get("lastModified")
    return parse_nexus_iso(dt_str)


def get_component_last_active_dt(component: dict) -> datetime.datetime:
    assets = component.get("assets") or []
    if not assets:
        return datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)
    return max(get_asset_last_active_dt(a) for a in assets)


def fetch_all_components(session: requests.Session) -> list[dict]:
    components = []
    url = f"{NEXUS_URL}/service/rest/v1/components"
    params = {"repository": REPO_NAME}

    while True:
        r = session.get(url, params=params, timeout=TIMEOUT_SECONDS)
        if r.status_code != 200:
            raise RuntimeError(f"List components failed status={r.status_code} body={r.text}")

        data = r.json() or {}
        items = data.get("items") or []
        components.extend(items)

        token = data.get("continuationToken")
        if not token:
            break

        params = {"repository": REPO_NAME, "continuationToken": token}
        print(f"Fetched {len(components)} components so far")

    return components


def run_cleanup_dryrun():
    print("Starting dry-run scan")
    print(f"NexusURL: {NEXUS_URL}")
    print(f"Repository: {REPO_NAME}")
    print(f"PolicyDaysOld: {DAYS_OLD}")
    print(f"KeepVersionsPerName: {KEEP_VERSIONS}")

    session = requests.Session()
    session.auth = (USERNAME, PASSWORD)
    session.verify = VERIFY_SSL

    try:
        components = fetch_all_components(session)
    except Exception as e:
        print(f"Error fetching components: {e}")
        return

    print(f"Total components fetched: {len(components)}")

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
                        "Repository": comp.get("repository", REPO_NAME),
                        "Component ID": comp.get("id", ""),
                        "Name": name,
                        "Version": comp.get("version", ""),
                        "Last Active Date": last_active.isoformat(),
                        "Reason": f"Older than {DAYS_OLD} days and not in top {KEEP_VERSIONS}",
                    }
                )

    print(f"Candidates: {len(candidates)}")

    if not candidates:
        print("No cleanup candidates found")
        return

    try:
        with open(CSV_REPORT_FILE, mode="w", encoding="utf-8-sig", newline="") as f:
            fieldnames = [
                "Repository",
                "Component ID",
                "Name",
                "Version",
                "Last Active Date",
                "Reason",
            ]
            writer = csv.DictWriter(f, fieldnames=fieldnames)
            writer.writeheader()
            writer.writerows(candidates)

        print(f"Report written: {CSV_REPORT_FILE}")
        print("Review the CSV before running any deletion script")

    except Exception as e:
        print(f"Error writing CSV: {e}")


if __name__ == "__main__":
    run_cleanup_dryrun()
