#!/bin/bash
set -euo pipefail

TODAY="$(date +%Y-%m-%d_%H%M%S)"
ARCHIVE="nexusdb2-${TODAY}.bk"
BACKUP_DIR="/opt/appdata/pgsql/backups"

echo "========================================================"
echo "Starting Nexus PostgreSQL DB Backup"
echo "Timestamp: ${TODAY}"
echo "Output: ${BACKUP_DIR}/${ARCHIVE}"
echo "========================================================"

mkdir -p "${BACKUP_DIR}"
cd "${BACKUP_DIR}"

# Use custom format (-Fc). Add -v if you want verbose output.
# If you need a specific host/port/user/db, set PG* env vars or add -h/-p/-U <db>.
/usr/bin/pg_dump -Fc nexusdb2 > "${ARCHIVE}"

# Prefer least-privilege. Use 0644 unless you truly need world-writable.
chmod 0644 "${ARCHIVE}"

echo "Backup completed: ${ARCHIVE}"
echo "========================================================"
