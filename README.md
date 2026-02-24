import csv
import datetime
import os
from collections import defaultdict
from urllib.parse import urlparse

import requests

# ============================================================
# Configuration
# ============================================================

NEXUS_URL = os.getenv("NEXUS_URL", "https://lxpd195:8444")
USERNAME = os.getenv("NEXUS_USERNAME", "nexus")
PASSWORD = os.getenv("NEXUS_PASSWORD", "CHANGE_ME")  # Use environment variable in real use

REPO_NAME = "SIP_Development"

# Candidate rules
DAYS_IDLE_THRESHOLD = 365
KEEP_VERSIONS_PER_IMAGE = 5

# Filter to specific image paths (substring match, case-insensitive)
# Set to [] to scan all images in the repo
TARGET_IMAGE_KEYWORDS = ["etime", "etime-dotnet8"]

VERIFY_SSL = False
TIMEOUT_SECONDS = 30

# Output directory (local machine)
BASE_DIR = r"C:\Users\C4387\Desktop\nexus_cleanup"
os.makedirs(BASE_DIR, exist_ok=True)

parsed_url = urlparse(NEXUS_URL)
hostname = parsed_url.hostname or "unknown_host"

timestamp = datetime.datetime.now().strftime("%Y%m%d_%H%M%S")
report_filename = f"cleanup_candidates_{hostname}_{REPO_NAME}_{timestamp}.csv"
CSV_REPORT_FILE = os.path.join(BASE_DIR, report_filename)

requests.packages.urllib3.disable_warnings()


# ============================================================
# Helpers
# ============================================================

def parse_nexus_iso(dt_str):
    """
    Parse Nexus ISO timestamp safely.
    Example values often look like:
      2024-02-11T08:22:33.123+00:00
      2024-02-11T08:22:33Z
    """
    if not dt_str:
        return datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)

    s = str(dt_str).strip()

    # Try Python's fromisoformat after normalizing Z
    try:
        if s.endswith("Z"):
            s = s[:-1] + "+00:00"
        dt = datetime.datetime.fromisoformat(s)
        if dt.tzinfo is None:
            dt = dt.replace(tzinfo=datetime.timezone.utc)
        return dt.astimezone(datetime.timezone.utc)
    except Exception:
        pass

    # Fallback: truncate to seconds
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


def normalize_text(v):
    return (v or "").strip()


def image_name_matches(name, keywords):
    if not keywords:
        return True
    n = (name or "").lower()
    return any(k.lower() in n for k in keywords)


def summarize_asset_paths(assets, max_paths=10):
    """
    Return a semicolon-separated list of Nexus asset paths (or download URLs fallback).
    Limits count to keep CSV readable.
    """
    paths = []
    for a in assets or []:
        p = normalize_text(a.get("path"))
        if not p:
            # fallback to downloadUrl if path is missing
            p = normalize_text(a.get("downloadUrl"))
        if p:
            paths.append(p)

    # de-duplicate while preserving order
    seen = set()
    unique_paths = []
    for p in paths:
        if p not in seen:
            seen.add(p)
            unique_paths.append(p)

    truncated = unique_paths[:max_paths]
    remaining = max(0, len(unique_paths) - len(truncated))

    if remaining > 0:
        truncated.append(f"... ({remaining} more assets)")

    return " ; ".join(truncated)


def analyze_component(component):
    """
    Returns:
      publish_dt, last_used_dt, total_bytes, total_downloads, asset_count, asset_paths_summary
    """
    assets = component.get("assets") or []
    epoch = datetime.datetime(1970, 1, 1, tzinfo=datetime.timezone.utc)

    if not assets:
        return epoch, epoch, 0, 0, 0, ""

    publish_dates = []
    used_dates = []
    total_bytes = 0
    total_downloads = 0

    for a in assets:
        total_bytes += safe_int(a.get("fileSize"), 0)
        total_downloads += safe_int(a.get("downloadCount"), 0)

        # "lastModified" is often the best publish-ish date at asset level
        p_dt = parse_nexus_iso(a.get("lastModified"))
        publish_dates.append(p_dt)

        d_str = a.get("lastDownloaded")
        # If never downloaded, fallback to lastModified so it can still be aged
        used_dates.append(parse_nexus_iso(d_str) if d_str else p_dt)

    asset_paths_summary = summarize_asset_paths(assets)

    return (
        max(publish_dates) if publish_dates else epoch,
        max(used_dates) if used_dates else epoch,
        total_bytes,
        total_downloads,
        len(assets),
        asset_paths_summary,
    )


def fetch_all_components(session):
    components = []
    url = f"{NEXUS_URL}/service/rest/v1/components"
    params = {"repository": REPO_NAME}

    while True:
        resp = session.get(url, params=params, timeout=TIMEOUT_SECONDS, verify=VERIFY_SSL)
        if resp.status_code != 200:
            raise RuntimeError(f"Fetch failed status={resp.status_code} body={resp.text}")

        data = resp.json() or {}
        items = data.get("items") or []
        components.extend(items)

        token = data.get("continuationToken")
        if not token:
            break

        params = {"repository": REPO_NAME, "continuationToken": token}
        print(f"Fetched {len(components)} components so far...")

    return components


# ============================================================
# Main logic
# ============================================================

def run_cleanup_candidate_scan():
    print("Scan started")
    print(f"Nexus URL: {NEXUS_URL}")
    print(f"Repository: {REPO_NAME}")
    print(f"Idle threshold (days): {DAYS_IDLE_THRESHOLD}")
    print(f"Keep newest versions per image: {KEEP_VERSIONS_PER_IMAGE}")
    print(f"Target image keywords: {TARGET_IMAGE_KEYWORDS if TARGET_IMAGE_KEYWORDS else 'ALL'}")
    print(f"Output file: {CSV_REPORT_FILE}")

    if PASSWORD == "CHANGE_ME":
        print("WARNING: Password is not set. Please set NEXUS_PASSWORD environment variable.")

    session = requests.Session()
    session.auth = (USERNAME, PASSWORD)
    session.verify = VERIFY_SSL

    try:
        all_components = fetch_all_components(session)
    except Exception as e:
        print(f"Fetch error: {e}")
        return

    print(f"Total components fetched: {len(all_components)}")

    # Keep only docker-format components and matching target image names
    filtered_components = []
    for comp in all_components:
        fmt = normalize_text(comp.get("format")).lower()
        name = normalize_text(comp.get("name"))

        if fmt != "docker":
            continue
        if not name:
            continue
        if not image_name_matches(name, TARGET_IMAGE_KEYWORDS):
            continue

        filtered_components.append(comp)

    print(f"Filtered docker components (target images): {len(filtered_components)}")

    # Group by image name (path)
    grouped = defaultdict(list)
    for comp in filtered_components:
        grouped[comp.get("name")].append(comp)

    now_utc = datetime.datetime.now(datetime.timezone.utc)
    cutoff_dt = now_utc - datetime.timedelta(days=DAYS_IDLE_THRESHOLD)

    candidates = []
    total_freed_bytes = 0

    for image_name, versions in grouped.items():
        # Analyze each component
        for comp in versions:
            (
                publish_dt,
                used_dt,
                size_bytes,
                total_downloads,
                asset_count,
                asset_paths_summary,
            ) = analyze_component(comp)

            comp["_publish_dt"] = publish_dt
            comp["_used_dt"] = used_dt
            comp["_size_bytes"] = size_bytes
            comp["_total_downloads"] = total_downloads
            comp["_asset_count"] = asset_count
            comp["_asset_paths_summary"] = asset_paths_summary

        # Sort newest first by publish date
        versions.sort(key=lambda x: x["_publish_dt"], reverse=True)

        # Keep newest N, evaluate the rest
        keep_count = min(KEEP_VERSIONS_PER_IMAGE, len(versions))
        keep_versions = versions[:keep_count]
        review_versions = versions[keep_count:]

        # Optional: add "kept" info for debugging (not written to CSV)
        kept_version_names = [normalize_text(v.get("version")) for v in keep_versions]

        for comp in review_versions:
            version = normalize_text(comp.get("version"))

            # Candidate if idle beyond threshold
            # (This is still a "candidate list", not guaranteed deletable space)
            if comp["_used_dt"] < cutoff_dt:
                total_freed_bytes += comp["_size_bytes"]

                age_days = (now_utc - comp["_publish_dt"]).days
                idle_days = (now_utc - comp["_used_dt"]).days

                candidates.append(
                    {
                        "Format": comp.get("format", "docker"),
                        "Repository": REPO_NAME,
                        "Image Path": image_name,  # This is the docker image path/name
                        "Version(Tag)": version,
                        "Component ID": comp.get("id", ""),
                        "Publish Date (UTC)": comp["_publish_dt"].strftime("%Y-%m-%d %H:%M:%S"),
                        "Age (Days)": age_days,
                        "Last Downloaded (UTC)": comp["_used_dt"].strftime("%Y-%m-%d %H:%M:%S"),
                        "Days Idle": idle_days,
                        "Total Downloads": comp["_total_downloads"],
                        "Asset Count": comp["_asset_count"],
                        "Size (MB)": round(comp["_size_bytes"] / (1024 * 1024), 2),
                        "Asset Paths (sample)": comp["_asset_paths_summary"],
                        "Deletion Candidate": "Yes",
                        "Reason": (
                            f"Idle > {DAYS_IDLE_THRESHOLD} days and outside newest "
                            f"{KEEP_VERSIONS_PER_IMAGE} versions"
                        ),
                        "Kept Newest Versions (for reference)": ", ".join(kept_version_names[:10]),
                    }
                )

    # Sort report by size descending, then image path
    candidates.sort(
        key=lambda r: (
            -(float(r.get("Size (MB)", 0) or 0)),
            r.get("Image Path", ""),
            r.get("Version(Tag)", ""),
        )
    )

    total_gb = total_freed_bytes / (1024 * 1024 * 1024)

    print("Scan complete")
    print(f"Target images found: {len(grouped)}")
    print(f"Deletion candidates: {len(candidates)}")
    print(f"Estimated candidate size (GB): {total_gb:.2f}")

    if not candidates:
        print("No candidates found.")
        return

    fieldnames = [
        "Format",
        "Repository",
        "Image Path",
        "Version(Tag)",
        "Component ID",
        "Publish Date (UTC)",
        "Age (Days)",
        "Last Downloaded (UTC)",
        "Days Idle",
        "Total Downloads",
        "Asset Count",
        "Size (MB)",
        "Asset Paths (sample)",
        "Deletion Candidate",
        "Reason",
        "Kept Newest Versions (for reference)",
    ]

    try:
        with open(CSV_REPORT_FILE, mode="w", encoding="utf-8-sig", newline="") as f:
            writer = csv.DictWriter(f, fieldnames=fieldnames)
            writer.writeheader()
            writer.writerows(candidates)

        print(f"Report written: {CSV_REPORT_FILE}")

    except Exception as e:
        print(f"CSV write error: {e}")


if __name__ == "__main__":
    run_cleanup_candidate_scan()
