CM Team pre tasks:
1.  Download and stage nexus-3.68.0-04-java8-unix.tar.gz to lxpd195. - Done
2. Expand and edit configuration files - Done
3. Update the nexus soft-link /opt/appdata/nexus/nexus - ToDo

During Upgrade:
-Snapshot lxpd195 and lxpd194 at 8:00 AM - Linux Admin
-Shutdown Nexus repository and PostgreSQL DB at 8:10 AM- CM Team
-Start PostgreSQL DB Nexus repository , Upgrade-Start Nexus repository& validate at 8:15 AM  - CM Team
Rollback Plan:
 1. Restore snapshots to lxpd195 and lxpd194 - Linux admins.
