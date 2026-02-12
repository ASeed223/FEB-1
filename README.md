Gemini said
Here is the text-only version of the upgrade checklist, formatted for easy copying and pasting into your documentation or notes.

Nexus Repository 3.71.0+ Upgrade Readiness Checklist
1. Java Runtime (Critical) Nexus 3.71.0 and later versions require Java 17. It will not start with Java 8 or 11.

Command: java -version

Target: OpenJDK version "17.x.x"

2. PostgreSQL Version Ensure your database engine is version 13 or higher (15 or 16 is recommended).

Command: psql --version

Alternative (SQL): SELECT version();

Target: PostgreSQL 13.x or higher.

3. JVM Memory Allocation Check your heap settings. With the move to Java 17 and PostgreSQL, ensure the server has enough overhead.

Command: cat bin/nexus.vmoptions | grep -E "Xms|Xmx"

Target: Minimum 4G (e.g., -Xms4G -Xmx4G).

4. Disk Space Verification Verify that the partition hosting your data directory has enough room for temporary upgrade logs and metadata validation.

Command: df -h

Target: Minimum 20% free space on the data volume.

5. Datastore Configuration Confirm that the Postgres datastore is correctly enabled in your properties file.

Command: grep "nexus.datastore.enabled" etc/nexus.properties

Target: nexus.datastore.enabled=true

6. Pre-Upgrade Database Backup Always create a fresh backup of your database immediately before the upgrade.

Command: pg_dump -h <db_host> -U <username> <db_name> > nexus_pre_upgrade.sql
