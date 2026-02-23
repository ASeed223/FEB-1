import csv
import datetime
import os
from collections import defaultdict
from urllib.parse import urlparse

import requests

# Optional (only needed if ENABLE_CLUSTER_CHECK = True)
# pip install --user kubernetes
try:
    from kubernetes import client  # type: ignore
except Exception:
    client = None


# -------------------- Configuration --------------------
NEXUS_URL = "https://lxpd195:8444"
USERNAME = "nexus"
PASSWORD = os.getenv("NEXUS_PASSWORD", "your_password_here")
REPO_NAME = "SIP_Development"

# Policy: idle > 730 days AND not in newest 10 by publish date
DAYS_OLD = 730
KEEP_VERSIONS = 10

# Safety limits
MAX_COMPONENT_PAGES = 50
TIMEOUT_SECONDS = 30
VERIFY_SSL = False

ENABLE_CLUSTER_CHECK = True

OPENSHIFT_CLUSTERS = [
    {
        "env_name": "NON_PROD",
        "host": "api.ocpnprc123:6443",
        "token": os.getenv("OCP_NONPROD_TOKEN", "your_token_here"),
        "verify_ssl": False,
    },
    {
        "env_name": "PROD",
        "host": "api.prod-openshift.com:6443",
        "token": os.getenv("OCP_PROD_TOKEN", "your_token_here"),
        "verify_ssl": False,
    },
]

BASE_DIR = r"C:\Users\C4387\Desktop\nexus_cleanup"
os.makedirs(BASE_DIR, exist_ok=True)

hostname = urlparse(NEXUS_URL).hostname or "unknown_host"
CSV_REPORT_FILE = os.path.join(BASE_DIR, f"cleanup_candidates_{hostname}_{REPO_NAME}.csv")

requests.packages.urllib3.disable_warnings()
# ------------------------------------------------------


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

    page_count = 0
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

        page_count += 1
        if page_count >= MAX_COMPONENT_PAGES:
            print(f"Stopped at MAX_COMPONENT_PAGES={MAX_COMPONENT_PAGES}")
            break

        params = {"repository": REPO_NAME, "continuationToken": token}
        print(f"Fetched {len(components)} components so far (page {page_count})")

    return components


def image_matches_name_tag(image_ref, name, version):
    """
    Match images like:
      registry/path/name:tag
      name:tag
    """
    if not image_ref or not name or not version:
        return False

    # Remove digest part if present: name:tag@sha256:...
    image_no_digest = str(image_ref).split("@", 1)[0].strip()

    # Compare only the last path segment (after last '/')
    last_part = image_no_digest.rsplit("/", 1)[-1]
    return last_part == f"{name}:{version}"


def get_active_images_from_all_clusters():
    active_images_map = defaultdict(set)

    if client is None:
        print("kubernetes library not available. Run: pip install --user kubernetes")
        return active_images_map

    for cluster in OPENSHIFT_CLUSTERS:
        env = cluster["env_name"]
        host = cluster["host"]
        token = cluster["token"]
        verify_ssl = cluster.get("verify_ssl", False)

        if not token or token == "your_token_here":
            print(f"Skipping cluster {env}: missing token")
            continue

        print(f"Scanning cluster {env} ({host})")

        cfg = client.Configuration()
        cfg.host = f"https://{host}"
        cfg.verify_ssl = bool(verify_ssl)
        cfg.api_key = {"authorization": f"Bearer {token}"}

        v1 = client.CoreV1Api(client.ApiClient(cfg))

        continue_token = None
        while True:
            pod_list = v1.list_pod_for_all_namespaces(
                watch=False,
                limit=500,
                _continue=continue_token,
            )
            for pod in pod_list.items:
                containers = []
                if pod.spec and pod.spec.containers:
                    containers.extend(pod.spec.containers)
                if pod.spec and pod.spec.init_containers:
                    containers.extend(pod.spec.init_containers)

                for c in containers:
                    if c and c.image:
                        active_images_map[c.image].add(env)

            continue_token = getattr(pod_list.metadata, "continue", None)
            if not continue_token:
                break

        print(f"Cluster {env} scan complete")

    return active_images_map


def run_rigorous_scan():
    print("Scan started")
    print(f"NexusHost: {hostname}")
    print(f"Repository: {REPO_NAME}")
    print(f"Policy: idle>{DAYS_OLD} days and keep newest {KEEP_VERSIONS} versions by publish date")
    print(f"Output: {CSV_REPORT_FILE}")
    print(f"ClusterCheck: {ENABLE_CLUSTER_CHECK}")

    active_images_map = defaultdict(set)
    if ENABLE_CLUSTER_CHECK:
        active_images_map = get_active_images_from_all_clusters()

    session = requests.Session()
    session.auth = (USERNAME, PASSWORD)

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
    saved_by_cluster = 0
    total_candidate_bytes = 0

    for name, versions in grouped.items():
        for comp in versions:
            p_dt, u_dt, size, d_count, a_count = analyze_component(comp)
            comp["_publish_dt"] = p_dt
            comp["_used_dt"] = u_dt
            comp["_size"] = size
            comp["_downloads"] = d_count
            comp["_asset_count"] = a_count

        # Newest by publish date first
        versions.sort(key=lambda x: x["_publish_dt"], reverse=True)

        # Keep newest KEEP_VERSIONS unconditionally
        for comp in versions[KEEP_VERSIONS:]:
            version = comp.get("version", "") or ""
            if not version:
                continue

            # Cluster protection check
            in_use_envs = set()
            if ENABLE_CLUSTER_CHECK and active_images_map:
                for img_ref, envs in active_images_map.items():
                    if image_matches_name_tag(img_ref, name, version):
                        in_use_envs |= set(envs)

            if in_use_envs:
                saved_by_cluster += 1
                continue

            # Idle check
            if comp["_used_dt"] < cutoff_dt:
                total_candidate_bytes += comp["_size"]

                age_days = (now_utc - comp["_publish_dt"]).days
                idle_days = (now_utc - comp["_used_dt"]).days

                candidates.append(
                    {
                        "Format": comp.get("format", "docker"),
                        "Name": name,
                        "Version": version,
                        "Component ID": comp.get("id", ""),
                        "Publish Date": comp["_publish_dt"].strftime("%Y-%m-%d"),
                        "Age (Days)": age_days,
                        "Last Downloaded": comp["_used_dt"].strftime("%Y-%m-%d"),
                        "Days Idle": idle_days,
                        "Total Downloads": comp["_downloads"],
                        "Asset Count": comp["_asset_count"],
                        "Size (MB)": round(comp["_size"] / (1024 * 1024), 2),
                        "Justification": f"Idle>{DAYS_OLD} days and outside newest {KEEP_VERSIONS}; not in use in clusters",
                    }
                )

    est_gb = total_candidate_bytes / (1024 ** 3)

    print("Scan complete")
    print(f"TotalComponents: {len(components)}")
    print(f"SavedByCluster: {saved_by_cluster}")
    print(f"Candidates: {len(candidates)}")
    print(f"EstimatedCandidateSizeGB: {est_gb:.2f}")

    if not candidates:
        print("No candidates found")
        return

    try:
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
        with open(CSV_REPORT_FILE, mode="w", encoding="utf-8-sig", newline="") as f:
            writer = csv.DictWriter(f, fieldnames=fieldnames)
            writer.writeheader()
            writer.writerows(candidates)

        print(f"Report written: {CSV_REPORT_FILE}")

    except Exception as e:
        print(f"CSV write error: {e}")


if __name__ == "__main__":
    run_rigorous_scan()
