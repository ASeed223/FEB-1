Step to Resolve
CM Team Pre-tasks:

Download and stage nexus-3.89.0-04-java8-unix.tar.gz on lxpd195. — Done

Extract package and configure system files. — Done

Prepare the Nexus symbolic link (/opt/appdata/nexus/nexus). — ToDo

During Upgrade:

Step 1: Perform system snapshots for lxpd195 and lxpd194 at 8:00 AM. (Owner: Linux Admin)

Step 2: Gracefully shut down Nexus repository and PostgreSQL DB services at 8:15 AM. (Owner: CM Team)

Step 3: Redirect the Nexus symbolic link to the new version directory. (Owner: CM Team)

Step 4: Restart services (PostgreSQL on lxpd194, then Nexus on lxpd195) and perform validation. (Owner: CM Team)

Rollback Plan:

Revert to pre-upgrade snapshots on lxpd195 and lxpd194 to restore the previous environment. (Owner: Linux Admin)
