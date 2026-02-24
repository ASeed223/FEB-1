import csv
import datetime
import os
from collections import defaultdict

import requests

# Configuration
NEXUS_URL = "http://lxpd195:8081"
USERNAME = "nexus"
PASSWORD = os.getenv("NEXUS_PASSWORD", "your_password_here")
REPOSITORY = "SIP_Development"
DAYS_DEAD = 365

TIMEOUT_SECONDS = 30
VERIFY_SSL = True  # set False only if you use https with self-signed cert

requests.packages.urllib3.disable_warnings()


def parse_nexus_dt(dt_str):
    if not dt_str:
        return datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)

    s = str(dt_str).strip()

    # Common Nexus formats:
    # 2025-01-02T03:04:05.678Z
    # 2025-01-02T03:04:05Z
    # 2025-01-02T03:04:05.678+00:00
    try:
        if s.endswith("Z"):
            s = s[:-1] + "+00:00"
        dt = datetime.datetime.fromisoformat(s)
        if dt.tzinfo is None:
            dt = dt.replace(tzinfo=datetime.timezone.utc)
        return dt.astimezone(datetime.timezone.utc)
    except Exception:
        # Fallback for older python or odd formats
        try:
            base = s[:19]
            dt = datetime.datetime.strptime(base, "%Y-%m-%dT%H:%M:%S")
            return dt.replace(tzinfo=datetime.timezone.utc)
        except Exception:
            return datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)


def get_dead_projects():
    print("Starting scan")
    print(f"Repository: {REPOSITORY}")
    print(f"DeadDays: {DAYS_DEAD}")

    projects = defaultdict(
        lambda: {
            "latest_dt": datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc),
            "latest_tag": "N/A",
            "total_versions": 0,
        }
    )

    session = requests.Session()
    session.auth = (USERNAME, PASSWORD)
    session.verify = VERIFY_SSL

    url = f"{NEXUS_URL}/service/rest/v1/components"
    params = {"repository": REPOSITORY}
    scanned = 0

    while True:
        try:
            r = session.get(url, params=params, timeout=TIMEOUT_SECONDS)
        except Exception as e:
            print(f"Request error: {e}")
            return

        if r.status_code != 200:
            print(f"Fetch failed status={r.status_code} body={r.text}")
            return

        data = r.json() or {}
        items = data.get("items") or []

        for item in items:
            scanned += 1
            project_name = (item.get("name") or "").strip()
            tag_version = (item.get("version") or "N/A").strip()

            if not project_name:
                continue

            projects[project_name]["total_versions"] += 1

            assets = item.get("assets") or []
            for asset in assets:
                dt = parse_nexus_dt(asset.get("lastDownloaded") or asset.get("lastModified"))
                if dt > projects[project_name]["latest_dt"]:
                    projects[project_name]["latest_dt"] = dt
                    projects[project_name]["latest_tag"] = tag_version

        token = data.get("continuationToken")
        if not token:
            break

        params = {"repository": REPOSITORY, "continuationToken": token}

        if scanned and scanned % 1000 == 0:
            print(f"Scanned {scanned} components")

    now = datetime.datetime.now(datetime.timezone.utc)
    csv_filename = f"dead_projects_{REPOSITORY}_{now.strftime('%Y%m%d_%H%M')}.csv"

    dead_rows = []
    for project, info in projects.items():
        days_inactive = (now - info["latest_dt"]).days
        if days_inactive > DAYS_DEAD:
            dead_rows.append(
                {
                    "Project Path": project,
                    "Days Inactive": days_inactive,
                    "Last Active Date": info["latest_dt"].strftime("%Y-%m-%d %H:%M:%S"),
                    "Latest Tag": info["latest_tag"],
                    "Total Versions": info["total_versions"],
                    "Action": "REVIEW AND DELETE PROJECT",
                }
            )

    dead_rows.sort(key=lambda x: x["Total Versions"], reverse=True)

    try:
        with open(csv_filename, mode="w", newline="", encoding="utf-8-sig") as f:
            fieldnames = [
                "Project Path",
                "Days Inactive",
                "Last Active Date",
                "Latest Tag",
                "Total Versions",
                "Action",
            ]
            w = csv.DictWriter(f, fieldnames=fieldnames)
            w.writeheader()
            w.writerows(dead_rows)

        print("Scan complete")
        print(f"ComponentsScanned: {scanned}")
        print(f"DeadProjects: {len(dead_rows)}")
        print(f"ReportWritten: {os.path.abspath(csv_filename)}")

    except Exception as e:
        print(f"CSV write error: {e}")


if __name__ == "__main__":
    get_dead_projects()
