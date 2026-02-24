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
VERIFY_SSL = True  # keep True for http, set False only for self-signed https

requests.packages.urllib3.disable_warnings()

projects_info = defaultdict(
    lambda: {
        "latest_date": datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc),
        "latest_tag": "N/A",
        "total_versions": 0,
    }
)


def parse_asset_dt(dt_str):
    if not dt_str:
        return None

    s = str(dt_str).strip()

    # Typical Nexus: 2024-01-02T03:04:05.678+00:00 or ...Z
    if s.endswith("Z"):
        s = s[:-1] + "+00:00"

    try:
        dt = datetime.datetime.fromisoformat(s)
    except Exception:
        try:
            base = s[:19]
            dt = datetime.datetime.strptime(base, "%Y-%m-%dT%H:%M:%S")
            dt = dt.replace(tzinfo=datetime.timezone.utc)
        except Exception:
            return None

    if dt.tzinfo is None:
        dt = dt.replace(tzinfo=datetime.timezone.utc)

    return dt.astimezone(datetime.timezone.utc)


def fetch_components(session):
    """
    Nexus versions differ:
      - Some support /service/rest/v1/components
      - Some support /service/rest/beta/components
    This tries v1 first, then beta.
    """
    base = NEXUS_URL.rstrip("/")
    paths = ["/service/rest/v1/components", "/service/rest/beta/components"]

    last_err = None
    for p in paths:
        components = []
        token = None
        scanned = 0
        page = 0

        while True:
            params = {"repository": REPOSITORY}
            if token:
                params["continuationToken"] = token

            url = f"{base}{p}"
            try:
                r = session.get(url, params=params, timeout=TIMEOUT_SECONDS, verify=VERIFY_SSL)
                if r.status_code == 404:
                    last_err = f"404 on {url}"
                    break
                r.raise_for_status()
                data = r.json() or {}
            except Exception as e:
                last_err = str(e)
                break

            items = data.get("items") or []
            components.extend(items)
            scanned += len(items)
            page += 1

            if scanned and scanned % 1000 == 0:
                print(f"Scanned {scanned} components")

            token = data.get("continuationToken")
            if not token:
                return components, p

            # Safety: stop if API loops
            if page > 10000:
                raise RuntimeError("Too many pages, possible API loop")

        # try next path
    raise RuntimeError(f"Could not fetch components. LastError: {last_err}")


def get_dead_projects():
    print(f"Scanning repository {REPOSITORY}")
    print(f"InactiveDaysThreshold: {DAYS_DEAD}")

    session = requests.Session()
    session.auth = (USERNAME, PASSWORD)

    try:
        components, api_used = fetch_components(session)
    except Exception as e:
        print(f"Fetch error: {e}")
        return

    print(f"APIUsed: {api_used}")
    print(f"TotalComponentsFetched: {len(components)}")

    if not components:
        print("No components returned by API")
        return

    for item in components:
        project_name = item.get("name") or ""
        tag_version = item.get("version") or "N/A"
        if not project_name:
            continue

        projects_info[project_name]["total_versions"] += 1

        for asset in item.get("assets") or []:
            asset_dt = parse_asset_dt(asset.get("lastModified"))
            if not asset_dt:
                continue

            if asset_dt > projects_info[project_name]["latest_date"]:
                projects_info[project_name]["latest_date"] = asset_dt
                projects_info[project_name]["latest_tag"] = tag_version

    now = datetime.datetime.now(datetime.timezone.utc)
    csv_filename = f"dead_docker_projects_{REPOSITORY}_{now.strftime('%Y%m%d_%H%M')}.csv"

    dead_rows = []
    for project, info in projects_info.items():
        days_inactive = (now - info["latest_date"]).days
        if days_inactive > DAYS_DEAD:
            dead_rows.append(
                [
                    project,
                    days_inactive,
                    info["latest_date"].strftime("%Y-%m-%d %H:%M:%S"),
                    info["latest_tag"],
                    info["total_versions"],
                    "DELETE_ENTIRE_PROJECT",
                ]
            )

    try:
        out_path = os.path.join(os.getcwd(), csv_filename)
        with open(out_path, mode="w", newline="", encoding="utf-8") as f:
            writer = csv.writer(f)
            writer.writerow(
                [
                    "ProjectPath",
                    "DaysInactive",
                    "LastActiveDateUTC",
                    "LatestTag",
                    "TotalVersions",
                    "Action",
                ]
            )
            writer.writerows(dead_rows)

        print(f"Report written: {out_path}")
        print(f"DeadProjects: {len(dead_rows)}")

    except Exception as e:
        print(f"CSV write error: {e}")


if __name__ == "__main__":
    get_dead_projects()
