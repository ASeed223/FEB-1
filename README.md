
[nexus.log](https://github.com/user-attachments/files/25270761/nexus.log)
2026-02-12 00:00:00,013-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Task log cleanup' [tasklog.cleanup] state change WAITING -> RUNNING
2026-02-12 00:00:00,021-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Firewall Ignore Patterns' [firewall.ignore-patterns] state change WAITING -> RUNNING
2026-02-12 00:00:00,031-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Cleaning up log files in /opt/appdata/nexus/sonatype-work/nexus3/log/tasks older than 30 days
2026-02-12 00:00:00,038-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Synchronize Proprietary Names to IQ Server for repository *' [firewall.proprietary.name.sync] state change WAITING -> RUNNING
2026-02-12 00:00:00,045-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 00:00:00,049-0800 INFO  [quartz-10-thread-4]  *SYSTEM com.sonatype.nexus.clm.internal.FirewallIgnorePatternsTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.ignore-patterns-20260212000000032.log
2026-02-12 00:00:00,052-0800 INFO  [quartz-10-thread-13]  *SYSTEM com.sonatype.nexus.clm.internal.proprietary.datastore.DatastoreFirewallProprietaryNameTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260212000000044.log
2026-02-12 00:00:00,084-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 00:00:00,085-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 00:00:00,092-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 00:00:00,105-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 00:00:00,110-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 00:00:00,114-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 00:00:00,119-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 00:00:00,210-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Firewall Ignore Patterns' [firewall.ignore-patterns] state change RUNNING -> WAITING (OK)
2026-02-12 00:00:00,301-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260112001500017.log
2026-02-12 00:00:00,302-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260112220000013.log
2026-02-12 00:00:00,303-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260112180000020.log
2026-02-12 00:00:00,303-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.ignore-patterns-20260112180000030.log
2026-02-12 00:00:00,304-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260112200000019.log
2026-02-12 00:00:00,304-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260112230000018.log
2026-02-12 00:00:00,305-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.ignore-patterns-20260112000000019.log
2026-02-12 00:00:00,305-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260112000000039.log
2026-02-12 00:00:00,305-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/repository.vulnerability.statistics-20260112000400015.log
2026-02-12 00:00:00,305-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260112003000030.log
2026-02-12 00:00:00,305-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260112003000221.log
2026-02-12 00:00:00,305-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260112004500016.log
2026-02-12 00:00:00,305-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260112010000035.log
2026-02-12 00:00:00,306-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/repository.docker.gc-20260112010000048.log
2026-02-12 00:00:00,306-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260112014500014.log
2026-02-12 00:00:00,306-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/repository.rebuild-index-20260112020000014.log
2026-02-12 00:00:00,306-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260112020000021.log
2026-02-12 00:00:00,306-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/usertoken.cleanup-20260112020100032.log
2026-02-12 00:00:00,306-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260112030000016.log
2026-02-12 00:00:00,307-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260112033000013.log
2026-02-12 00:00:00,308-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260112040000018.log
2026-02-12 00:00:00,308-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260112040000023.log
2026-02-12 00:00:00,309-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260112051500015.log
2026-02-12 00:00:00,309-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260112060000011.log
2026-02-12 00:00:00,310-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.ignore-patterns-20260112060000015.log
2026-02-12 00:00:00,310-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260112080000013.log
2026-02-12 00:00:00,310-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/repository.maven.rebuild-metadata-20260112100000013.log
2026-02-12 00:00:00,311-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/repository.maven.publish-dotindex-20260112100000017.log
2026-02-12 00:00:00,311-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260112100000059.log
2026-02-12 00:00:00,311-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260112120000018.log
2026-02-12 00:00:00,311-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.ignore-patterns-20260112120000034.log
2026-02-12 00:00:00,312-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260112140000016.log
2026-02-12 00:00:00,312-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.tasklog.TaskLogCleanup - Removed task log file /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260112160000018.log
2026-02-12 00:00:00,313-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Task log cleanup' [tasklog.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 00:00:01,210-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Synchronize Proprietary Names to IQ Server for repository *' [firewall.proprietary.name.sync] state change RUNNING -> WAITING (OK)
2026-02-12 00:01:00,007-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change WAITING -> RUNNING
2026-02-12 00:01:00,146-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change RUNNING -> WAITING (OK)
2026-02-12 00:04:00,010-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Statistics - recalculate vulnerabilities statistics' [repository.vulnerability.statistics] state change WAITING -> RUNNING
2026-02-12 00:04:00,015-0800 INFO  [quartz-10-thread-6]  *SYSTEM com.sonatype.nexus.vulnerability.internal.log.VulnerabilityStatisticsTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/repository.vulnerability.statistics-20260212000400013.log
2026-02-12 00:04:52,510-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Statistics - recalculate vulnerabilities statistics' [repository.vulnerability.statistics] state change RUNNING -> WAITING (OK)
2026-02-12 00:15:00,008-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Compact  Blob - default' [blobstore.compact] state change WAITING -> RUNNING
2026-02-12 00:15:00,014-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.blobstore.compact.internal.CompactBlobStoreTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260212001500013.log
2026-02-12 00:15:00,018-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - Begin deleted blobs processing
2026-02-12 00:15:00,073-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - ---- Removed 0 empty directories from /opt/appdata/nexus/sonatype-work/nexus3/blobs/default/content/directpath ----
2026-02-12 00:15:00,074-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Compact  Blob - default' [blobstore.compact] state change RUNNING -> WAITING (OK)
2026-02-12 00:30:00,010-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Compact 3rdParty' [blobstore.compact] state change WAITING -> RUNNING
2026-02-12 00:30:00,013-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.blobstore.compact.internal.CompactBlobStoreTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260212003000012.log
2026-02-12 00:30:00,016-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - Begin deleted blobs processing
2026-02-12 00:30:00,017-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task '3. CompactBlob-Docker- Run after Soft Delete' [blobstore.compact] state change WAITING -> RUNNING
2026-02-12 00:30:00,036-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - ---- Removed 0 empty directories from /opt/appdata/nexus/sonatype-work/nexus3/blobs/3rdParty/content/directpath ----
2026-02-12 00:30:00,050-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Compact 3rdParty' [blobstore.compact] state change RUNNING -> WAITING (OK)
2026-02-12 00:30:00,052-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.blobstore.compact.internal.CompactBlobStoreTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260212003000051.log
2026-02-12 00:30:00,056-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - Begin deleted blobs processing
2026-02-12 00:30:00,057-0800 INFO  [quartz-10-thread-9]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task '2. Soft-deleted Docker images - Use this task before Compact Docker Blobs' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 00:30:00,066-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 00:30:00,076-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 00:30:00,093-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 00:30:00,101-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 00:30:00,251-0800 INFO  [quartz-10-thread-9]  *SYSTEM org.sonatype.nexus.repository.content.store.internal.AssetBlobCleanupTask - Deleted 106 unused docker blobs from nexus
2026-02-12 00:30:00,253-0800 INFO  [quartz-10-thread-9]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task '2. Soft-deleted Docker images - Use this task before Compact Docker Blobs' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 00:30:00,262-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 00:30:00,266-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 00:30:00,271-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 00:30:00,274-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 00:30:03,407-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - ---- Removed 179 empty directories from /opt/appdata/nexus/sonatype-work/nexus3/blobs/Docker/content/directpath ----
2026-02-12 00:30:03,410-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task '3. CompactBlob-Docker- Run after Soft Delete' [blobstore.compact] state change RUNNING -> WAITING (OK)
2026-02-12 00:31:32,258-0800 INFO  [qtp1952145369-90777]  SIP_TFStoTower_NP org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Repository Metrics update scheduler' [repository.metrics.update.scheduler] : state=WAITING
2026-02-12 00:31:32,264-0800 INFO  [qtp1952145369-90777]  SIP_TFStoTower_NP org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'Repository Metrics update scheduler' [repository.metrics.update.scheduler] scheduled: once
2026-02-12 00:33:32,264-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Repository Metrics update scheduler' [repository.metrics.update.scheduler] state change WAITING -> RUNNING
2026-02-12 00:33:32,268-0800 INFO  [quartz-10-thread-6]  *SYSTEM com.sonatype.nexus.repository.content.store.metrics.RepositoryMetricsUpdateTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/repository.metrics.update.scheduler-20260212003332267.log
2026-02-12 00:33:32,372-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Repository Metrics update scheduler' [repository.metrics.update.scheduler] state change RUNNING -> OK
2026-02-12 00:45:00,009-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Compact Blob - NuGet' [blobstore.compact] state change WAITING -> RUNNING
2026-02-12 00:45:00,016-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.blobstore.compact.internal.CompactBlobStoreTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260212004500015.log
2026-02-12 00:45:00,021-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - Begin deleted blobs processing
2026-02-12 00:45:00,027-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - ---- Removed 0 empty directories from /opt/appdata/nexus/sonatype-work/nexus3/blobs/nuGet/content/directpath ----
2026-02-12 00:45:00,029-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Compact Blob - NuGet' [blobstore.compact] state change RUNNING -> WAITING (OK)
2026-02-12 00:48:28,150-0800 INFO  [periodic-4-thread-1]  *SYSTEM org.sonatype.nexus.internal.atlas.SystemInformationGeneratorImpl - Generating system information report
2026-02-12 00:59:08,805-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Validating all active sessions...
2026-02-12 00:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Finished session validation.  No sessions were stopped.
2026-02-12 01:00:00,010-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Compact Blob - Release' [blobstore.compact] state change WAITING -> RUNNING
2026-02-12 01:00:00,014-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.blobstore.compact.internal.CompactBlobStoreTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260212010000012.log
2026-02-12 01:00:00,017-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - Begin deleted blobs processing
2026-02-12 01:00:00,019-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused go blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 01:00:00,022-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - ---- Removed 0 empty directories from /opt/appdata/nexus/sonatype-work/nexus3/blobs/release/content/directpath ----
2026-02-12 01:00:00,052-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Compact Blob - Release' [blobstore.compact] state change RUNNING -> WAITING (OK)
2026-02-12 01:00:00,055-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused go blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 01:00:00,056-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused yum blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 01:00:00,060-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused yum blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 01:00:00,066-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused maven2 blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 01:00:00,074-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task '1. SIP_Development Docker Repo - Delete Unused manifests and image task. ' [repository.docker.gc] state change WAITING -> RUNNING
2026-02-12 01:00:00,081-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.repository.docker.tasks.DockerGCTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/repository.docker.gc-20260212010000080.log
2026-02-12 01:00:00,081-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 01:00:00,081-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.repository.docker.internal.datastore.recipe.DockerGCFacetImpl - Garbage collection starting on repository: RepositoryImpl$$EnhancerByGuice$$253e240a{type=hosted, format=docker, name='SIP_Development'}
2026-02-12 01:00:00,089-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 01:00:00,105-0800 INFO  [quartz-10-thread-9]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused npm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 01:00:00,113-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 01:00:00,122-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 01:00:00,737-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.repository.content.store.internal.AssetBlobCleanupTask - Deleted 351 unused maven2 blobs from nexus
2026-02-12 01:00:00,738-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused maven2 blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 01:00:00,746-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 01:00:00,750-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 01:00:00,779-0800 INFO  [quartz-10-thread-9]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused npm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 01:00:00,786-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 01:00:00,790-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 01:01:00,008-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change WAITING -> RUNNING
2026-02-12 01:01:00,235-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change RUNNING -> WAITING (OK)
2026-02-12 01:01:19,432-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][scheduler][T#1]]  *SYSTEM org.elasticsearch.monitor.jvm - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [gc][young][1043926][2287] duration [751ms], collections [1]/[1.2s], total [751ms]/[1.1m], memory [934.3mb]->[720.1mb]/[6gb], all_pools {[young] [156mb]->[0b]/[0b]}{[old] [644.3mb]->[710.1mb]/[6gb]}{[survivor] [134mb]->[10mb]/[0b]}
2026-02-12 01:01:51,375-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Repository Metrics update scheduler' [repository.metrics.update.scheduler] : state=WAITING
2026-02-12 01:01:51,384-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'Repository Metrics update scheduler' [repository.metrics.update.scheduler] scheduled: once
2026-02-12 01:02:28,729-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.repository.docker.internal.datastore.recipe.DockerGCFacetImpl - Garbage collection completed on repository: RepositoryImpl$$EnhancerByGuice$$253e240a{type=hosted, format=docker, name='SIP_Development'}
2026-02-12 01:02:28,732-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task '1. SIP_Development Docker Repo - Delete Unused manifests and image task. ' [repository.docker.gc] state change RUNNING -> WAITING (OK)
2026-02-12 01:03:51,388-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Repository Metrics update scheduler' [repository.metrics.update.scheduler] state change WAITING -> RUNNING
2026-02-12 01:03:51,392-0800 INFO  [quartz-10-thread-4]  *SYSTEM com.sonatype.nexus.repository.content.store.metrics.RepositoryMetricsUpdateTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/repository.metrics.update.scheduler-20260212010351391.log
2026-02-12 01:03:51,476-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Repository Metrics update scheduler' [repository.metrics.update.scheduler] state change RUNNING -> OK
2026-02-12 01:30:00,008-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 01:30:00,022-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 01:30:00,022-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 01:30:00,034-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 01:30:00,035-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 01:30:00,040-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 01:30:00,043-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 01:30:00,052-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 01:45:00,033-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'CompactBlob-OCP-EDR2Docker' [blobstore.compact] state change WAITING -> RUNNING
2026-02-12 01:45:00,042-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.blobstore.compact.internal.CompactBlobStoreTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260212014500040.log
2026-02-12 01:45:00,046-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - Begin deleted blobs processing
2026-02-12 01:45:00,047-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - ---- Removed 0 empty directories from /opt/appdata/nexus/sonatype-work/nexus3/blobs/EDR2-Docker/content/directpath ----
2026-02-12 01:45:00,049-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'CompactBlob-OCP-EDR2Docker' [blobstore.compact] state change RUNNING -> WAITING (OK)
2026-02-12 01:58:28,147-0800 INFO  [periodic-4-thread-1]  *SYSTEM org.sonatype.nexus.internal.atlas.SystemInformationGeneratorImpl - Generating system information report
2026-02-12 01:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Validating all active sessions...
2026-02-12 01:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Finished session validation.  No sessions were stopped.
2026-02-12 02:00:00,009-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task '1. Rebuild all repo Search indexes' [repository.rebuild-index] state change WAITING -> RUNNING
2026-02-12 02:00:00,016-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.search.index.RebuildIndexTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/repository.rebuild-index-20260212020000014.log
2026-02-12 02:00:00,016-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository EDR-OpenCaseDoc
2026-02-12 02:00:00,023-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Synchronize Proprietary Names to IQ Server for repository *' [firewall.proprietary.name.sync] state change WAITING -> RUNNING
2026-02-12 02:00:00,030-0800 INFO  [quartz-10-thread-1]  *SYSTEM com.sonatype.nexus.clm.internal.proprietary.datastore.DatastoreFirewallProprietaryNameTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260212020000029.log
2026-02-12 02:00:00,034-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 02:00:00,041-0800 INFO  [quartz-10-thread-9]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 02:00:00,045-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [8601ea6ba0d25dc1e47639e728b571b2719cd243] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:00:00,046-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 02:00:00,052-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 02:00:00,055-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 02:00:00,056-0800 INFO  [quartz-10-thread-9]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 02:00:00,059-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 02:00:00,065-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[8601ea6ba0d25dc1e47639e728b571b2719cd243][0]] ...]).
2026-02-12 02:00:00,065-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 02:00:00,094-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 21 / 21 EDR-OpenCaseDoc components in 33 ms ----
2026-02-12 02:00:00,094-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository JBossMaven
2026-02-12 02:00:00,096-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [8601ea6ba0d25dc1e47639e728b571b2719cd243] update_mapping [component]
2026-02-12 02:00:00,112-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [a5b2f3b87fe0aa3f05a36d39fb7c7a4e3cf249d3] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:00:00,125-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[a5b2f3b87fe0aa3f05a36d39fb7c7a4e3cf249d3][0]] ...]).
2026-02-12 02:00:00,249-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 48 / 48 JBossMaven components in 124 ms ----
2026-02-12 02:00:00,249-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository olm-ftb
2026-02-12 02:00:00,257-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [a5b2f3b87fe0aa3f05a36d39fb7c7a4e3cf249d3] update_mapping [component]
2026-02-12 02:00:00,265-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [c42bef72c19c56a4a5d01f2772e08cbdb8a56004] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:00:00,279-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository RedHatMaven
2026-02-12 02:00:00,290-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[c42bef72c19c56a4a5d01f2772e08cbdb8a56004][0], [c42bef72c19c56a4a5d01f2772e08cbdb8a56004][0]] ...]).
2026-02-12 02:00:00,298-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [e2fcee496f4eec0f8405ebb55370e388f83ad466] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:00:00,312-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[e2fcee496f4eec0f8405ebb55370e388f83ad466][0]] ...]).
2026-02-12 02:00:01,366-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Synchronize Proprietary Names to IQ Server for repository *' [firewall.proprietary.name.sync] state change RUNNING -> WAITING (OK)
2026-02-12 02:00:03,204-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [e2fcee496f4eec0f8405ebb55370e388f83ad466] update_mapping [component]
2026-02-12 02:00:03,244-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [e2fcee496f4eec0f8405ebb55370e388f83ad466] update_mapping [component]
2026-02-12 02:00:03,257-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [e2fcee496f4eec0f8405ebb55370e388f83ad466] update_mapping [component]
2026-02-12 02:00:03,266-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [e2fcee496f4eec0f8405ebb55370e388f83ad466] update_mapping [component]
2026-02-12 02:00:19,732-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 6546 / 6546 RedHatMaven components in 19386 ms ----
2026-02-12 02:00:19,732-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository IVR_THIRD_PARTY
2026-02-12 02:00:19,742-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [db4107b1eb0bf30e24fc455f71f321d92792261d] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:00:19,756-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[db4107b1eb0bf30e24fc455f71f321d92792261d][0]] ...]).
2026-02-12 02:00:19,913-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 1 / 1 IVR_THIRD_PARTY components in 148 ms ----
2026-02-12 02:00:19,913-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository nuget_org_v2
2026-02-12 02:00:19,923-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [db4107b1eb0bf30e24fc455f71f321d92792261d] update_mapping [component]
2026-02-12 02:00:19,931-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ca0d1c15127cb24671144b696ca5d5177a99cbaf] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:00:19,944-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[ca0d1c15127cb24671144b696ca5d5177a99cbaf][0]] ...]).
2026-02-12 02:00:21,000-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ca0d1c15127cb24671144b696ca5d5177a99cbaf] update_mapping [component]
2026-02-12 02:00:21,020-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ca0d1c15127cb24671144b696ca5d5177a99cbaf] update_mapping [component]
2026-02-12 02:00:21,030-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ca0d1c15127cb24671144b696ca5d5177a99cbaf] update_mapping [component]
2026-02-12 02:00:21,046-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ca0d1c15127cb24671144b696ca5d5177a99cbaf] update_mapping [component]
2026-02-12 02:00:21,069-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ca0d1c15127cb24671144b696ca5d5177a99cbaf] update_mapping [component]
2026-02-12 02:00:21,151-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ca0d1c15127cb24671144b696ca5d5177a99cbaf] update_mapping [component]
2026-02-12 02:00:50,004-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 21025 / 21025 nuget_org_v2 components in 30056 ms ----
2026-02-12 02:00:50,005-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository EDRRELEASE
2026-02-12 02:00:50,043-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [b4c6c1fb756b88a621c48b9750fd43add14a4d7d] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:00:50,061-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[b4c6c1fb756b88a621c48b9750fd43add14a4d7d][0]] ...]).
2026-02-12 02:00:55,054-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [b4c6c1fb756b88a621c48b9750fd43add14a4d7d] update_mapping [component]
2026-02-12 02:00:55,062-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [b4c6c1fb756b88a621c48b9750fd43add14a4d7d] update_mapping [component]
2026-02-12 02:00:55,069-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [b4c6c1fb756b88a621c48b9750fd43add14a4d7d] update_mapping [component]
2026-02-12 02:01:00,009-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change WAITING -> RUNNING
2026-02-12 02:01:00,026-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Admin - Cleanup expired user tokens' [usertoken.cleanup] state change WAITING -> RUNNING
2026-02-12 02:01:00,036-0800 INFO  [quartz-10-thread-16]  *SYSTEM com.sonatype.nexus.usertoken.plugin.internal.task.UserTokenCleanupTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/usertoken.cleanup-20260212020100035.log
2026-02-12 02:01:00,039-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Admin - Cleanup expired user tokens' [usertoken.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 02:01:00,222-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change RUNNING -> WAITING (OK)
2026-02-12 02:01:17,808-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [b4c6c1fb756b88a621c48b9750fd43add14a4d7d] update_mapping [component]
2026-02-12 02:04:37,007-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 41277 / 41277 EDRRELEASE components in 226906 ms ----
2026-02-12 02:04:37,007-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository WebAPI
2026-02-12 02:04:37,020-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3a5f5cf4d8fb661fbd1eebc307a451cc67b94b94] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:04:37,037-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[3a5f5cf4d8fb661fbd1eebc307a451cc67b94b94][0]] ...]).
2026-02-12 02:04:41,650-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3a5f5cf4d8fb661fbd1eebc307a451cc67b94b94] update_mapping [component]
2026-02-12 02:04:41,658-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3a5f5cf4d8fb661fbd1eebc307a451cc67b94b94] update_mapping [component]
2026-02-12 02:04:41,824-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3a5f5cf4d8fb661fbd1eebc307a451cc67b94b94] update_mapping [component]
2026-02-12 02:04:41,862-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3a5f5cf4d8fb661fbd1eebc307a451cc67b94b94] update_mapping [component]
2026-02-12 02:04:50,063-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 2789 / 2789 WebAPI components in 12993 ms ----
2026-02-12 02:04:50,063-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository OCP_Certified
2026-02-12 02:04:50,072-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [15dc31b1530756cc5b836e375c65c8955bda2567] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:04:50,088-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[15dc31b1530756cc5b836e375c65c8955bda2567][0]] ...]).
2026-02-12 02:04:50,099-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository SdsDevelopment
2026-02-12 02:04:50,120-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3d332be2e7b3a2224246a0fd3dd034dfc1a3a81d] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:04:50,133-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[3d332be2e7b3a2224246a0fd3dd034dfc1a3a81d][0]] ...]).
2026-02-12 02:04:50,188-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3a5f5cf4d8fb661fbd1eebc307a451cc67b94b94] update_mapping [component]
2026-02-12 02:04:55,112-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3d332be2e7b3a2224246a0fd3dd034dfc1a3a81d] update_mapping [component]
2026-02-12 02:04:55,120-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3d332be2e7b3a2224246a0fd3dd034dfc1a3a81d] update_mapping [component]
2026-02-12 02:04:55,137-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3d332be2e7b3a2224246a0fd3dd034dfc1a3a81d] update_mapping [component]
2026-02-12 02:04:55,147-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3d332be2e7b3a2224246a0fd3dd034dfc1a3a81d] update_mapping [component]
2026-02-12 02:04:55,169-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3d332be2e7b3a2224246a0fd3dd034dfc1a3a81d] update_mapping [component]
2026-02-12 02:04:55,543-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3d332be2e7b3a2224246a0fd3dd034dfc1a3a81d] update_mapping [component]
2026-02-12 02:04:55,752-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3d332be2e7b3a2224246a0fd3dd034dfc1a3a81d] update_mapping [component]
2026-02-12 02:05:32,936-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 7287 / 7287 SdsDevelopment components in 42791 ms ----
2026-02-12 02:05:32,936-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository maven-snapshots
2026-02-12 02:05:32,945-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [2e9a1e67e8a325bcd6ee9f6790ff6c769e791d56] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:05:32,959-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[2e9a1e67e8a325bcd6ee9f6790ff6c769e791d56][0]] ...]).
2026-02-12 02:05:32,969-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository maven-central
2026-02-12 02:05:32,988-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [73ae44bc066b6a7a33b4435641d8229b9b66495a] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:05:33,002-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[73ae44bc066b6a7a33b4435641d8229b9b66495a][0]] ...]).
2026-02-12 02:05:36,362-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [73ae44bc066b6a7a33b4435641d8229b9b66495a] update_mapping [component]
2026-02-12 02:05:36,373-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [73ae44bc066b6a7a33b4435641d8229b9b66495a] update_mapping [component]
2026-02-12 02:05:36,381-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [73ae44bc066b6a7a33b4435641d8229b9b66495a] update_mapping [component]
2026-02-12 02:06:30,402-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 17627 / 17627 maven-central components in 57357 ms ----
2026-02-12 02:06:30,402-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository FTB_HelmHosted
2026-02-12 02:06:30,412-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [a2e157cc2262c364f0db0eb429c8efc79ba217a2] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:30,430-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[a2e157cc2262c364f0db0eb429c8efc79ba217a2][0]] ...]).
2026-02-12 02:06:30,614-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 3 / 3 FTB_HelmHosted components in 160 ms ----
2026-02-12 02:06:30,614-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository nuget-hosted
2026-02-12 02:06:30,623-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [b2b9b8f06274052a44b61ef3c7e887f0961d99c6] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:30,639-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[b2b9b8f06274052a44b61ef3c7e887f0961d99c6][0]] ...]).
2026-02-12 02:06:30,650-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository FTB_NuGet_3rd_Party
2026-02-12 02:06:30,660-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [6ca0cb6eb06b0d04ceedd4a4b7e40cc0b68f5b6f] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:30,678-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[6ca0cb6eb06b0d04ceedd4a4b7e40cc0b68f5b6f][0]] ...]).
2026-02-12 02:06:30,717-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [a2e157cc2262c364f0db0eb429c8efc79ba217a2] update_mapping [component]
2026-02-12 02:06:30,797-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [6ca0cb6eb06b0d04ceedd4a4b7e40cc0b68f5b6f] update_mapping [component]
2026-02-12 02:06:30,799-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 50 / 50 FTB_NuGet_3rd_Party components in 109 ms ----
2026-02-12 02:06:30,800-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository EDRDevPySpark
2026-02-12 02:06:30,812-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [b4525f2312cdea8d9242849d9e10658350224f20] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:30,824-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [6ca0cb6eb06b0d04ceedd4a4b7e40cc0b68f5b6f] update_mapping [component]
2026-02-12 02:06:30,830-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[b4525f2312cdea8d9242849d9e10658350224f20][0]] ...]).
2026-02-12 02:06:30,834-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [6ca0cb6eb06b0d04ceedd4a4b7e40cc0b68f5b6f] update_mapping [component]
2026-02-12 02:06:32,249-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [b4525f2312cdea8d9242849d9e10658350224f20] update_mapping [component]
2026-02-12 02:06:33,848-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 2027 / 2027 EDRDevPySpark components in 3018 ms ----
2026-02-12 02:06:33,848-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository ocp
2026-02-12 02:06:33,863-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [f014032113c31c6a28cd62c20be832b75305cedc] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:33,896-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[f014032113c31c6a28cd62c20be832b75305cedc][0]] ...]).
2026-02-12 02:06:34,938-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [f014032113c31c6a28cd62c20be832b75305cedc] update_mapping [component]
2026-02-12 02:06:34,940-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 688 / 688 ocp components in 1047 ms ----
2026-02-12 02:06:34,940-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository m2e
2026-02-12 02:06:34,949-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [30c32cbdbed543fe018e47b233150fd82537ebdf] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:34,968-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[30c32cbdbed543fe018e47b233150fd82537ebdf][0]] ...]).
2026-02-12 02:06:34,982-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository WebAPIStaging
2026-02-12 02:06:34,991-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [765ec550c06b8e5934f9d97eaa41fa33bdba6902] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:35,007-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[765ec550c06b8e5934f9d97eaa41fa33bdba6902][0]] ...]).
2026-02-12 02:06:39,430-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [765ec550c06b8e5934f9d97eaa41fa33bdba6902] update_mapping [component]
2026-02-12 02:06:39,439-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [765ec550c06b8e5934f9d97eaa41fa33bdba6902] update_mapping [component]
2026-02-12 02:06:39,530-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [765ec550c06b8e5934f9d97eaa41fa33bdba6902] update_mapping [component]
2026-02-12 02:06:39,631-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 1046 / 1046 WebAPIStaging components in 4595 ms ----
2026-02-12 02:06:39,631-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository maven-releases
2026-02-12 02:06:39,636-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [765ec550c06b8e5934f9d97eaa41fa33bdba6902] update_mapping [component]
2026-02-12 02:06:39,644-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3d781e8165513bfe7db3d7eaab3991b9ebec763b] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:39,662-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[3d781e8165513bfe7db3d7eaab3991b9ebec763b][0]] ...]).
2026-02-12 02:06:39,712-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 1 / 1 maven-releases components in 4 ms ----
2026-02-12 02:06:39,712-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository CDS_Dev
2026-02-12 02:06:39,720-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [dbc173dd13c5618356b959a8804bef130dd87615] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:39,733-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[dbc173dd13c5618356b959a8804bef130dd87615][0]] ...]).
2026-02-12 02:06:39,741-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 4 / 4 CDS_Dev components in 8 ms ----
2026-02-12 02:06:39,741-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository EDRSNAPSHOT
2026-02-12 02:06:39,748-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [d61058dc8c5075cb48e308d33151a956fe9465c7] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:39,763-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[d61058dc8c5075cb48e308d33151a956fe9465c7][0]] ...]).
2026-02-12 02:06:39,865-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 13 / 13 EDRSNAPSHOT components in 76 ms ----
2026-02-12 02:06:39,865-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository EDR2_RELEASE
2026-02-12 02:06:39,872-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [d3631e627dc6651819abe969220be1d4565f4fed] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:39,887-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[d3631e627dc6651819abe969220be1d4565f4fed][0]] ...]).
2026-02-12 02:06:40,063-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [765ec550c06b8e5934f9d97eaa41fa33bdba6902] update_mapping [component]
2026-02-12 02:06:40,118-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 37 / 37 EDR2_RELEASE components in 210 ms ----
2026-02-12 02:06:40,119-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository WebAPIRelease
2026-02-12 02:06:40,128-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [605340fd54e4ea7de995664bda233eaefcd71685] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:40,146-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[605340fd54e4ea7de995664bda233eaefcd71685][0]] ...]).
2026-02-12 02:06:40,202-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3d781e8165513bfe7db3d7eaab3991b9ebec763b] update_mapping [component]
2026-02-12 02:06:40,211-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [dbc173dd13c5618356b959a8804bef130dd87615] update_mapping [component]
2026-02-12 02:06:40,221-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [d61058dc8c5075cb48e308d33151a956fe9465c7] update_mapping [component]
2026-02-12 02:06:40,234-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 12 / 12 WebAPIRelease components in 52 ms ----
2026-02-12 02:06:40,234-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository prisma_proxy
2026-02-12 02:06:40,241-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [e9d4d93b7645c06d62423d457ed4caa633cc9268] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:40,251-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [d3631e627dc6651819abe969220be1d4565f4fed] update_mapping [component]
2026-02-12 02:06:40,257-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[e9d4d93b7645c06d62423d457ed4caa633cc9268][0]] ...]).
2026-02-12 02:06:40,260-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 3 / 3 prisma_proxy components in 8 ms ----
2026-02-12 02:06:40,260-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository VRCMod
2026-02-12 02:06:40,268-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ba2e7a938c6bb448c9985b2dfdd12558e6a83633] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:40,284-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[ba2e7a938c6bb448c9985b2dfdd12558e6a83633][0]] ...]).
2026-02-12 02:06:40,292-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [605340fd54e4ea7de995664bda233eaefcd71685] update_mapping [component]
2026-02-12 02:06:40,301-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [605340fd54e4ea7de995664bda233eaefcd71685] update_mapping [component]
2026-02-12 02:06:40,312-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [605340fd54e4ea7de995664bda233eaefcd71685] update_mapping [component]
2026-02-12 02:06:40,324-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [e9d4d93b7645c06d62423d457ed4caa633cc9268] update_mapping [component]
2026-02-12 02:06:41,044-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ba2e7a938c6bb448c9985b2dfdd12558e6a83633] update_mapping [component]
2026-02-12 02:06:41,044-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 172 / 172 VRCMod components in 760 ms ----
2026-02-12 02:06:41,044-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository pypi_group
2026-02-12 02:06:41,056-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ba2e7a938c6bb448c9985b2dfdd12558e6a83633] update_mapping [component]
2026-02-12 02:06:41,064-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [c309cddb92ba9857e8280769fc0e278fa3cbf5cb] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:41,075-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ba2e7a938c6bb448c9985b2dfdd12558e6a83633] update_mapping [component]
2026-02-12 02:06:41,075-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository EDRPLUGINS
2026-02-12 02:06:41,085-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[c309cddb92ba9857e8280769fc0e278fa3cbf5cb][0], [c309cddb92ba9857e8280769fc0e278fa3cbf5cb][0]] ...]).
2026-02-12 02:06:41,094-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3ac4a5060bec409ba8f6281e8128d3986e600854] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:41,106-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ba2e7a938c6bb448c9985b2dfdd12558e6a83633] update_mapping [component]
2026-02-12 02:06:41,111-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[3ac4a5060bec409ba8f6281e8128d3986e600854][0]] ...]).
2026-02-12 02:06:41,127-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ba2e7a938c6bb448c9985b2dfdd12558e6a83633] update_mapping [component]
2026-02-12 02:06:41,146-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 2 / 2 EDRPLUGINS components in 14 ms ----
2026-02-12 02:06:41,146-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository FTB_GO
2026-02-12 02:06:41,158-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ba2e7a938c6bb448c9985b2dfdd12558e6a83633] update_mapping [component]
2026-02-12 02:06:41,166-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [4d04cc6f418dce8b0611222de578be41bc59a410] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:41,179-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository pypi_hosted
2026-02-12 02:06:41,180-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[4d04cc6f418dce8b0611222de578be41bc59a410][0]] ...]).
2026-02-12 02:06:41,190-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [658dc2e92fa47fcad2c082c8658d983d1a1f5af6] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:41,207-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[658dc2e92fa47fcad2c082c8658d983d1a1f5af6][0]] ...]).
2026-02-12 02:06:41,222-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 6 / 6 pypi_hosted components in 18 ms ----
2026-02-12 02:06:41,222-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository cmtools
2026-02-12 02:06:41,230-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [f96386f7a822fb5e0e33ceed64791ae08e52e65e] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:41,246-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3ac4a5060bec409ba8f6281e8128d3986e600854] update_mapping [component]
2026-02-12 02:06:41,252-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[f96386f7a822fb5e0e33ceed64791ae08e52e65e][0]] ...]).
2026-02-12 02:06:41,258-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [3ac4a5060bec409ba8f6281e8128d3986e600854] update_mapping [component]
2026-02-12 02:06:41,267-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [658dc2e92fa47fcad2c082c8658d983d1a1f5af6] update_mapping [component]
2026-02-12 02:06:41,273-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [658dc2e92fa47fcad2c082c8658d983d1a1f5af6] update_mapping [component]
2026-02-12 02:06:41,279-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [658dc2e92fa47fcad2c082c8658d983d1a1f5af6] update_mapping [component]
2026-02-12 02:06:41,289-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [658dc2e92fa47fcad2c082c8658d983d1a1f5af6] update_mapping [component]
2026-02-12 02:06:41,296-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [658dc2e92fa47fcad2c082c8658d983d1a1f5af6] update_mapping [component]
2026-02-12 02:06:41,427-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 133 / 133 cmtools components in 183 ms ----
2026-02-12 02:06:41,427-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository ECLIPSE
2026-02-12 02:06:41,428-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [f96386f7a822fb5e0e33ceed64791ae08e52e65e] update_mapping [component]
2026-02-12 02:06:41,436-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [f96386f7a822fb5e0e33ceed64791ae08e52e65e] update_mapping [component]
2026-02-12 02:06:41,442-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [8a191ddf653d28b05fbc5397b6d117f967f8fad2] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:41,455-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[8a191ddf653d28b05fbc5397b6d117f967f8fad2][0]] ...]).
2026-02-12 02:06:41,487-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [8a191ddf653d28b05fbc5397b6d117f967f8fad2] update_mapping [component]
2026-02-12 02:06:41,511-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 8 / 8 ECLIPSE components in 32 ms ----
2026-02-12 02:06:41,512-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository FTB_RedHatDockerProxy
2026-02-12 02:06:41,519-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [a0b97c239e242eb46318eb03f657050e28d5b899] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:41,533-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[a0b97c239e242eb46318eb03f657050e28d5b899][0]] ...]).
2026-02-12 02:06:41,608-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 52 / 52 FTB_RedHatDockerProxy components in 78 ms ----
2026-02-12 02:06:41,609-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository confluent-io
2026-02-12 02:06:41,609-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [a0b97c239e242eb46318eb03f657050e28d5b899] update_mapping [component]
2026-02-12 02:06:41,619-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [03dae54b96a731030a685a8173c277e6a81012bf] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:41,630-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [a0b97c239e242eb46318eb03f657050e28d5b899] update_mapping [component]
2026-02-12 02:06:41,636-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[03dae54b96a731030a685a8173c277e6a81012bf][0]] ...]).
2026-02-12 02:06:41,969-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [03dae54b96a731030a685a8173c277e6a81012bf] update_mapping [component]
2026-02-12 02:06:41,977-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [03dae54b96a731030a685a8173c277e6a81012bf] update_mapping [component]
2026-02-12 02:06:41,986-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 114 / 114 confluent-io components in 336 ms ----
2026-02-12 02:06:41,986-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository FTB_DockerHosted
2026-02-12 02:06:41,995-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [11a3b9da6b89c8b96f9bb7c762c7fccb06d16db7] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:42,010-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[11a3b9da6b89c8b96f9bb7c762c7fccb06d16db7][0]] ...]).
2026-02-12 02:06:43,346-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [11a3b9da6b89c8b96f9bb7c762c7fccb06d16db7] update_mapping [component]
2026-02-12 02:06:43,353-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [11a3b9da6b89c8b96f9bb7c762c7fccb06d16db7] update_mapping [component]
2026-02-12 02:06:43,458-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [11a3b9da6b89c8b96f9bb7c762c7fccb06d16db7] update_mapping [component]
2026-02-12 02:06:50,264-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 5450 / 5450 FTB_DockerHosted components in 8248 ms ----
2026-02-12 02:06:50,264-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository JitPack
2026-02-12 02:06:50,273-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [9ec27e8496eee8ad1d2a7c7947c18e43e853fa6f] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:50,287-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[9ec27e8496eee8ad1d2a7c7947c18e43e853fa6f][0]] ...]).
2026-02-12 02:06:50,293-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 1 / 1 JitPack components in 7 ms ----
2026-02-12 02:06:50,293-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository primefaces
2026-02-12 02:06:50,303-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [233a01b2eb58b7b4f7fc483b0ffde9d6235f86f8] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:50,318-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[233a01b2eb58b7b4f7fc483b0ffde9d6235f86f8][0]] ...]).
2026-02-12 02:06:50,367-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [9ec27e8496eee8ad1d2a7c7947c18e43e853fa6f] update_mapping [component]
2026-02-12 02:06:50,653-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 97 / 97 primefaces components in 338 ms ----
2026-02-12 02:06:50,654-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository SIP_Development
2026-02-12 02:06:50,655-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [233a01b2eb58b7b4f7fc483b0ffde9d6235f86f8] update_mapping [component]
2026-02-12 02:06:50,678-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [233a01b2eb58b7b4f7fc483b0ffde9d6235f86f8] update_mapping [component]
2026-02-12 02:06:50,688-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [af88ee085c0e914b8f8ac2e4c0af190a610b6976] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:06:50,705-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[af88ee085c0e914b8f8ac2e4c0af190a610b6976][0]] ...]).
2026-02-12 02:06:50,714-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [233a01b2eb58b7b4f7fc483b0ffde9d6235f86f8] update_mapping [component]
2026-02-12 02:06:52,088-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [af88ee085c0e914b8f8ac2e4c0af190a610b6976] update_mapping [component]
2026-02-12 02:06:52,095-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [af88ee085c0e914b8f8ac2e4c0af190a610b6976] update_mapping [component]
2026-02-12 02:06:52,101-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [af88ee085c0e914b8f8ac2e4c0af190a610b6976] update_mapping [component]
2026-02-12 02:07:54,095-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 42342 / 42342 SIP_Development components in 63382 ms ----
2026-02-12 02:07:54,095-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository FTB_npm_3rdParty
2026-02-12 02:07:54,103-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [fef6ce93887ed383c77de9cfd75057e6165abd26] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:54,114-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository EDRDevBatchClient
2026-02-12 02:07:54,117-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[fef6ce93887ed383c77de9cfd75057e6165abd26][0], [fef6ce93887ed383c77de9cfd75057e6165abd26][0]] ...]).
2026-02-12 02:07:54,124-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [a64f0f7469e1049bd50e65623227a9f92f935755] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:54,148-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[a64f0f7469e1049bd50e65623227a9f92f935755][0]] ...]).
2026-02-12 02:07:54,159-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 12 / 12 EDRDevBatchClient components in 25 ms ----
2026-02-12 02:07:54,159-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository FTB_npm
2026-02-12 02:07:54,160-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [a64f0f7469e1049bd50e65623227a9f92f935755] update_mapping [component]
2026-02-12 02:07:54,170-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [055332df6818e88bf8319c0f90ee28422ae7ad68] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:54,179-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository Pega-EKL
2026-02-12 02:07:54,184-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[055332df6818e88bf8319c0f90ee28422ae7ad68][0], [055332df6818e88bf8319c0f90ee28422ae7ad68][0]] ...]).
2026-02-12 02:07:54,190-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [5e5365b678c283f9259fb69b893c852434109696] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:54,205-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[5e5365b678c283f9259fb69b893c852434109696][0]] ...]).
2026-02-12 02:07:54,235-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 23 / 23 Pega-EKL components in 34 ms ----
2026-02-12 02:07:54,235-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [5e5365b678c283f9259fb69b893c852434109696] update_mapping [component]
2026-02-12 02:07:54,235-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository AnsibleResources
2026-02-12 02:07:54,249-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [1e5485754715e7a9ecec1ed9fe34e824080b9a5a] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:54,263-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[1e5485754715e7a9ecec1ed9fe34e824080b9a5a][0]] ...]).
2026-02-12 02:07:54,504-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [1e5485754715e7a9ecec1ed9fe34e824080b9a5a] update_mapping [component]
2026-02-12 02:07:54,506-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 136 / 136 AnsibleResources components in 242 ms ----
2026-02-12 02:07:54,506-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository nuget.org-proxy
2026-02-12 02:07:54,513-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [1e5485754715e7a9ecec1ed9fe34e824080b9a5a] update_mapping [component]
2026-02-12 02:07:54,521-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [51196dce51055df9247e1973e443b68c84549dd9] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:54,538-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository EDRProdPySpark
2026-02-12 02:07:54,545-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [117544595d702f33acbe27d39447e462161dd562] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:54,565-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository EDRSTAGING
2026-02-12 02:07:54,573-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[117544595d702f33acbe27d39447e462161dd562][0]] ...]).
2026-02-12 02:07:54,583-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [362fc0e43f4a87a8bc4d39d84ecb681fbd8d4408] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:54,597-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[362fc0e43f4a87a8bc4d39d84ecb681fbd8d4408][0]] ...]).
2026-02-12 02:07:54,630-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [362fc0e43f4a87a8bc4d39d84ecb681fbd8d4408] update_mapping [component]
2026-02-12 02:07:54,632-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 4 / 4 EDRSTAGING components in 26 ms ----
2026-02-12 02:07:54,633-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository TST1
2026-02-12 02:07:54,642-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [45bb476ab80ca37e6f6e1bfed4d5df4a1b4aa227] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:54,655-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [362fc0e43f4a87a8bc4d39d84ecb681fbd8d4408] update_mapping [component]
2026-02-12 02:07:54,659-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[45bb476ab80ca37e6f6e1bfed4d5df4a1b4aa227][0]] ...]).
2026-02-12 02:07:54,661-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository TST2
2026-02-12 02:07:54,674-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [66d3cf0d0339bbadc408723200dd48935abd910b] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:54,687-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository EDR-Online-Help
2026-02-12 02:07:54,691-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[66d3cf0d0339bbadc408723200dd48935abd910b][0], [66d3cf0d0339bbadc408723200dd48935abd910b][0]] ...]).
2026-02-12 02:07:54,697-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [b410df80ee9b9aef6191839987e7bfd6a9752960] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:54,710-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[b410df80ee9b9aef6191839987e7bfd6a9752960][0]] ...]).
2026-02-12 02:07:55,246-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [b410df80ee9b9aef6191839987e7bfd6a9752960] update_mapping [component]
2026-02-12 02:07:55,248-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 365 / 365 EDR-Online-Help components in 532 ms ----
2026-02-12 02:07:55,248-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository EDRDevMDMHubConfig
2026-02-12 02:07:55,256-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [75cf8d732260dcef8f3a9a57cb6ca0b2b0460cb8] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:55,266-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [b410df80ee9b9aef6191839987e7bfd6a9752960] update_mapping [component]
2026-02-12 02:07:55,271-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 1 / 1 EDRDevMDMHubConfig components in 3 ms ----
2026-02-12 02:07:55,271-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[75cf8d732260dcef8f3a9a57cb6ca0b2b0460cb8][0]] ...]).
2026-02-12 02:07:55,271-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository CDS_Certified
2026-02-12 02:07:55,284-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [694ab3ed6ed1b6a599c63e06f2e01e2cde02e951] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:55,300-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[694ab3ed6ed1b6a599c63e06f2e01e2cde02e951][0]] ...]).
2026-02-12 02:07:55,309-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 3 / 3 CDS_Certified components in 10 ms ----
2026-02-12 02:07:55,309-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository ECOM
2026-02-12 02:07:55,309-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [75cf8d732260dcef8f3a9a57cb6ca0b2b0460cb8] update_mapping [component]
2026-02-12 02:07:55,320-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [f84ae9034a6f5d26936817dbcd220107fd63eeb0] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:55,330-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [694ab3ed6ed1b6a599c63e06f2e01e2cde02e951] update_mapping [component]
2026-02-12 02:07:55,335-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[f84ae9034a6f5d26936817dbcd220107fd63eeb0][0]] ...]).
2026-02-12 02:07:55,346-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 8 / 8 ECOM components in 14 ms ----
2026-02-12 02:07:55,347-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository FTB_NuGet
2026-02-12 02:07:55,347-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [f84ae9034a6f5d26936817dbcd220107fd63eeb0] update_mapping [component]
2026-02-12 02:07:55,356-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [f84ae9034a6f5d26936817dbcd220107fd63eeb0] update_mapping [component]
2026-02-12 02:07:55,365-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [4be119a9243774bb9de5ab70d6c8172995ea3e5b] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:55,380-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[4be119a9243774bb9de5ab70d6c8172995ea3e5b][0]] ...]).
2026-02-12 02:07:55,407-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 13 / 13 FTB_NuGet components in 30 ms ----
2026-02-12 02:07:55,407-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository EDR3RDPARTY
2026-02-12 02:07:55,408-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [4be119a9243774bb9de5ab70d6c8172995ea3e5b] update_mapping [component]
2026-02-12 02:07:55,423-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [4be119a9243774bb9de5ab70d6c8172995ea3e5b] update_mapping [component]
2026-02-12 02:07:55,433-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ce88290bbe1a23bb8246768699fb92948092c0b1] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:07:55,443-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [4be119a9243774bb9de5ab70d6c8172995ea3e5b] update_mapping [component]
2026-02-12 02:07:55,447-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[ce88290bbe1a23bb8246768699fb92948092c0b1][0]] ...]).
2026-02-12 02:07:59,441-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ce88290bbe1a23bb8246768699fb92948092c0b1] update_mapping [component]
2026-02-12 02:07:59,454-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ce88290bbe1a23bb8246768699fb92948092c0b1] update_mapping [component]
2026-02-12 02:07:59,491-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [ce88290bbe1a23bb8246768699fb92948092c0b1] update_mapping [component]
2026-02-12 02:08:01,008-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 1245 / 1245 EDR3RDPARTY components in 5560 ms ----
2026-02-12 02:08:01,008-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository Jenkins
2026-02-12 02:08:01,015-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [0e3d3bba37ad416794f22c8990ee4ae1c5abca01] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:01,025-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository FTB_YUM
2026-02-12 02:08:01,029-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[0e3d3bba37ad416794f22c8990ee4ae1c5abca01][0], [0e3d3bba37ad416794f22c8990ee4ae1c5abca01][0]] ...]).
2026-02-12 02:08:01,037-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [5997c4ed0f28f3b95d66f7396d6094d5cd81febd] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:01,050-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[5997c4ed0f28f3b95d66f7396d6094d5cd81febd][0]] ...]).
2026-02-12 02:08:01,055-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 1 / 1 FTB_YUM components in 7 ms ----
2026-02-12 02:08:01,055-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository pypi_proxy
2026-02-12 02:08:01,062-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [4e8241f1b79bdee2b3210f53980621bf23208ea4] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:01,074-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository CDSTestApp
2026-02-12 02:08:01,078-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[4e8241f1b79bdee2b3210f53980621bf23208ea4][0], [4e8241f1b79bdee2b3210f53980621bf23208ea4][0]] ...]).
2026-02-12 02:08:01,086-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [2c70f2be2c010e23b89e7ca710f372ca3f111807] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:01,096-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository FTB_RedHatDockerHosted
2026-02-12 02:08:01,101-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[2c70f2be2c010e23b89e7ca710f372ca3f111807][0], [2c70f2be2c010e23b89e7ca710f372ca3f111807][0]] ...]).
2026-02-12 02:08:01,108-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [a3737e24d8c2695c303e9a80b530e488c28462e5] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:01,119-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository FTB_DockerProxy
2026-02-12 02:08:01,127-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [2cc98e98b91137faf9e176981836055e0f2960bf] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:01,142-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[2cc98e98b91137faf9e176981836055e0f2960bf][0]] ...]).
2026-02-12 02:08:01,181-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 28 / 28 FTB_DockerProxy components in 42 ms ----
2026-02-12 02:08:01,181-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository SdsRelease
2026-02-12 02:08:01,188-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [09c4361e55ba4c36c249ac8bc813e419e4d741fe] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:01,202-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [5997c4ed0f28f3b95d66f7396d6094d5cd81febd] update_mapping [component]
2026-02-12 02:08:01,206-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[09c4361e55ba4c36c249ac8bc813e419e4d741fe][0]] ...]).
2026-02-12 02:08:01,211-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [2cc98e98b91137faf9e176981836055e0f2960bf] update_mapping [component]
2026-02-12 02:08:06,226-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [09c4361e55ba4c36c249ac8bc813e419e4d741fe] update_mapping [component]
2026-02-12 02:08:06,232-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [09c4361e55ba4c36c249ac8bc813e419e4d741fe] update_mapping [component]
2026-02-12 02:08:06,238-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [09c4361e55ba4c36c249ac8bc813e419e4d741fe] update_mapping [component]
2026-02-12 02:08:06,242-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [09c4361e55ba4c36c249ac8bc813e419e4d741fe] update_mapping [component]
2026-02-12 02:08:06,278-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [09c4361e55ba4c36c249ac8bc813e419e4d741fe] update_mapping [component]
2026-02-12 02:08:06,320-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [09c4361e55ba4c36c249ac8bc813e419e4d741fe] update_mapping [component]
2026-02-12 02:08:06,467-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [09c4361e55ba4c36c249ac8bc813e419e4d741fe] update_mapping [component]
2026-02-12 02:08:08,481-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 1327 / 1327 SdsRelease components in 7261 ms ----
2026-02-12 02:08:08,481-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository UIT2
2026-02-12 02:08:08,511-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [a6894dfcf28dd64ca7526c5a54cd5817e650cbbd] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:08,525-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[a6894dfcf28dd64ca7526c5a54cd5817e650cbbd][0]] ...]).
2026-02-12 02:08:08,529-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository UIT1
2026-02-12 02:08:08,538-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [7c8838956cebb6663906263343dec26fd28e8f73] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:08,551-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository OCP_Dev
2026-02-12 02:08:08,556-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[7c8838956cebb6663906263343dec26fd28e8f73][0]] ...]).
2026-02-12 02:08:08,565-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [f297dcdb904bb7180643f31c00f9098b192c166d] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:08,580-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[f297dcdb904bb7180643f31c00f9098b192c166d][0]] ...]).
2026-02-12 02:08:08,581-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository Adobe
2026-02-12 02:08:08,590-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [e3643a741ac27679dcbee196e29d8fdaace03a2d] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:08,611-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[e3643a741ac27679dcbee196e29d8fdaace03a2d][0]] ...]).
2026-02-12 02:08:08,774-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [e3643a741ac27679dcbee196e29d8fdaace03a2d] update_mapping [component]
2026-02-12 02:08:08,777-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 21 / 21 Adobe components in 151 ms ----
2026-02-12 02:08:08,777-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository olm-mirror
2026-02-12 02:08:08,782-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [e3643a741ac27679dcbee196e29d8fdaace03a2d] update_mapping [component]
2026-02-12 02:08:08,788-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [bb89faf52994f79b6d2dabfe9440c7c7bd4b784a] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:08,796-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [e3643a741ac27679dcbee196e29d8fdaace03a2d] update_mapping [component]
2026-02-12 02:08:08,801-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[bb89faf52994f79b6d2dabfe9440c7c7bd4b784a][0]] ...]).
2026-02-12 02:08:08,852-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [bb89faf52994f79b6d2dabfe9440c7c7bd4b784a] update_mapping [component]
2026-02-12 02:08:08,854-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 21 / 21 olm-mirror components in 52 ms ----
2026-02-12 02:08:08,855-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository npm_proxy
2026-02-12 02:08:08,863-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [7f67737afdadc58a7e85319a79bf730779090032] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:08,874-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [bb89faf52994f79b6d2dabfe9440c7c7bd4b784a] update_mapping [component]
2026-02-12 02:08:08,879-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[7f67737afdadc58a7e85319a79bf730779090032][0]] ...]).
2026-02-12 02:08:10,758-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [7f67737afdadc58a7e85319a79bf730779090032] update_mapping [component]
2026-02-12 02:08:10,766-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [7f67737afdadc58a7e85319a79bf730779090032] update_mapping [component]
2026-02-12 02:08:10,781-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [7f67737afdadc58a7e85319a79bf730779090032] update_mapping [component]
2026-02-12 02:08:10,828-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [7f67737afdadc58a7e85319a79bf730779090032] update_mapping [component]
2026-02-12 02:08:10,913-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [7f67737afdadc58a7e85319a79bf730779090032] update_mapping [component]
2026-02-12 02:08:10,986-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [7f67737afdadc58a7e85319a79bf730779090032] update_mapping [component]
2026-02-12 02:08:13,144-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [7f67737afdadc58a7e85319a79bf730779090032] update_mapping [component]
2026-02-12 02:08:15,235-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [7f67737afdadc58a7e85319a79bf730779090032] update_mapping [component]
2026-02-12 02:08:17,230-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 3983 / 3983 npm_proxy components in 8351 ms ----
2026-02-12 02:08:17,230-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository SIP_Quarantine
2026-02-12 02:08:17,238-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [103ad6b8864a35ba852c611833a7045ac34f3443] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:17,251-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[103ad6b8864a35ba852c611833a7045ac34f3443][0]] ...]).
2026-02-12 02:08:17,740-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [103ad6b8864a35ba852c611833a7045ac34f3443] update_mapping [component]
2026-02-12 02:08:17,743-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 220 / 220 SIP_Quarantine components in 485 ms ----
2026-02-12 02:08:17,743-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository CCPIVRAppRepository
2026-02-12 02:08:17,748-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [103ad6b8864a35ba852c611833a7045ac34f3443] update_mapping [component]
2026-02-12 02:08:17,756-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [1f3b9551ab8f3b82d0eb488a9e95c64ccfc3a10e] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:17,770-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[1f3b9551ab8f3b82d0eb488a9e95c64ccfc3a10e][0]] ...]).
2026-02-12 02:08:17,809-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [1f3b9551ab8f3b82d0eb488a9e95c64ccfc3a10e] update_mapping [component]
2026-02-12 02:08:17,812-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 3 / 3 CCPIVRAppRepository components in 26 ms ----
2026-02-12 02:08:17,812-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - Rebuilding index of repository FTB_RedHatQuay
2026-02-12 02:08:17,819-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [bbb2509b4ce3e1a58e98477dd2508e9fe28ff169] creating index, cause [api], templates [], shards [1]/[0], mappings [component]
2026-02-12 02:08:17,829-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [1f3b9551ab8f3b82d0eb488a9e95c64ccfc3a10e] update_mapping [component]
2026-02-12 02:08:17,836-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.routing.allocation - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] Cluster health status changed from [RED] to [GREEN] (reason: [shards started [[bbb2509b4ce3e1a58e98477dd2508e9fe28ff169][0]] ...]).
2026-02-12 02:08:17,841-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.repository.content.search.elasticsearch.SearchFacetImpl - ---- Indexed 1 / 1 FTB_RedHatQuay components in 7 ms ----
2026-02-12 02:08:17,842-0800 INFO  [elasticsearch[CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585][clusterService#updateTask][T#1]]  *SYSTEM org.elasticsearch.cluster.metadata - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] [bbb2509b4ce3e1a58e98477dd2508e9fe28ff169] update_mapping [component]
2026-02-12 02:08:17,847-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task '1. Rebuild all repo Search indexes' [repository.rebuild-index] state change RUNNING -> WAITING (OK)
2026-02-12 02:30:00,009-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Rebuild npm metadata' [repository.npm.rebuild-metadata] state change WAITING -> RUNNING
2026-02-12 02:30:00,015-0800 INFO  [quartz-10-thread-19]  *SYSTEM com.sonatype.nexus.repository.npm.internal.tasks.datastore.RebuildNpmMetadataTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/repository.npm.rebuild-metadata-20260212023000014.log
2026-02-12 02:30:00,021-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 02:30:00,023-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Rebuild npm metadata' [repository.npm.rebuild-metadata] state change RUNNING -> WAITING (OK)
2026-02-12 02:30:00,025-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 02:30:00,034-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 02:30:00,042-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 02:30:00,047-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 02:30:00,053-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 02:30:00,055-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 02:30:00,060-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 02:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Validating all active sessions...
2026-02-12 02:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Finished session validation.  No sessions were stopped.
2026-02-12 03:00:00,010-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Compact Blob WebApi RAW' [blobstore.compact] state change WAITING -> RUNNING
2026-02-12 03:00:00,026-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Compact NPM' [blobstore.compact] state change WAITING -> RUNNING
2026-02-12 03:00:00,028-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.blobstore.compact.internal.CompactBlobStoreTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260212030000018.log
2026-02-12 03:00:00,034-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - Begin deleted blobs processing
2026-02-12 03:00:00,036-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - ---- Removed 0 empty directories from /opt/appdata/nexus/sonatype-work/nexus3/blobs/webapi_raw/content/directpath ----
2026-02-12 03:00:00,036-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 03:00:00,037-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Compact Blob WebApi RAW' [blobstore.compact] state change RUNNING -> WAITING (OK)
2026-02-12 03:00:00,039-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.blobstore.compact.internal.CompactBlobStoreTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260212030000039.log
2026-02-12 03:00:00,040-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 03:00:00,043-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - Begin deleted blobs processing
2026-02-12 03:00:00,049-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - ---- Removed 0 empty directories from /opt/appdata/nexus/sonatype-work/nexus3/blobs/npm/content/directpath ----
2026-02-12 03:00:00,052-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Compact NPM' [blobstore.compact] state change RUNNING -> WAITING (OK)
2026-02-12 03:00:00,052-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 03:00:00,058-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 03:00:00,060-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 03:00:00,068-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 03:00:00,074-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 03:00:00,077-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 03:01:00,008-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change WAITING -> RUNNING
2026-02-12 03:01:00,229-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change RUNNING -> WAITING (OK)
2026-02-12 03:08:28,142-0800 INFO  [periodic-4-thread-1]  *SYSTEM org.sonatype.nexus.internal.atlas.SystemInformationGeneratorImpl - Generating system information report
2026-02-12 03:30:00,008-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'CompactBlobWebApiMaven' [blobstore.compact] state change WAITING -> RUNNING
2026-02-12 03:30:00,015-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 03:30:00,020-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.blobstore.compact.internal.CompactBlobStoreTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260212033000017.log
2026-02-12 03:30:00,023-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 03:30:00,026-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - Begin deleted blobs processing
2026-02-12 03:30:00,027-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 03:30:00,059-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - ---- Removed 0 empty directories from /opt/appdata/nexus/sonatype-work/nexus3/blobs/webapi_maven/content/directpath ----
2026-02-12 03:30:00,060-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 03:30:00,062-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'CompactBlobWebApiMaven' [blobstore.compact] state change RUNNING -> WAITING (OK)
2026-02-12 03:30:00,066-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 03:30:00,075-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 03:30:00,077-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 03:30:00,084-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 03:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Validating all active sessions...
2026-02-12 03:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Finished session validation.  No sessions were stopped.
2026-02-12 04:00:00,012-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'CompactBlob-SDS' [blobstore.compact] state change WAITING -> RUNNING
2026-02-12 04:00:00,017-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.blobstore.compact.internal.CompactBlobStoreTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/blobstore.compact-20260212040000015.log
2026-02-12 04:00:00,018-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Synchronize Proprietary Names to IQ Server for repository *' [firewall.proprietary.name.sync] state change WAITING -> RUNNING
2026-02-12 04:00:00,020-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - Begin deleted blobs processing
2026-02-12 04:00:00,022-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.blobstore.file.FileBlobStore - ---- Removed 0 empty directories from /opt/appdata/nexus/sonatype-work/nexus3/blobs/ServicesDevelopmentSection/content/directpath ----
2026-02-12 04:00:00,023-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'CompactBlob-SDS' [blobstore.compact] state change RUNNING -> WAITING (OK)
2026-02-12 04:00:00,026-0800 INFO  [quartz-10-thread-19]  *SYSTEM com.sonatype.nexus.clm.internal.proprietary.datastore.DatastoreFirewallProprietaryNameTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260212040000025.log
2026-02-12 04:00:00,028-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 04:00:00,038-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 04:00:00,038-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 04:00:00,043-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 04:00:00,055-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 04:00:00,062-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 04:00:00,063-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 04:00:00,071-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 04:00:01,177-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Synchronize Proprietary Names to IQ Server for repository *' [firewall.proprietary.name.sync] state change RUNNING -> WAITING (OK)
2026-02-12 04:01:00,008-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change WAITING -> RUNNING
2026-02-12 04:01:00,159-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change RUNNING -> WAITING (OK)
2026-02-12 04:18:28,146-0800 INFO  [periodic-4-thread-1]  *SYSTEM org.sonatype.nexus.internal.atlas.SystemInformationGeneratorImpl - Generating system information report
2026-02-12 04:30:00,009-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 04:30:00,022-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 04:30:00,025-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 04:30:00,035-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 04:30:00,046-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 04:30:00,050-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 04:30:00,054-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 04:30:00,058-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 04:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Validating all active sessions...
2026-02-12 04:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Finished session validation.  No sessions were stopped.
2026-02-12 05:00:00,009-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 05:00:00,021-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 05:00:00,022-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 05:00:00,030-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 05:00:00,035-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 05:00:00,038-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 05:00:00,042-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 05:00:00,046-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 05:01:00,011-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change WAITING -> RUNNING
2026-02-12 05:01:00,170-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change RUNNING -> WAITING (OK)
2026-02-12 05:28:28,140-0800 INFO  [periodic-4-thread-1]  *SYSTEM org.sonatype.nexus.internal.atlas.SystemInformationGeneratorImpl - Generating system information report
2026-02-12 05:30:00,008-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 05:30:00,021-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 05:30:00,022-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 05:30:00,031-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 05:30:00,035-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 05:30:00,039-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 05:30:00,040-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 05:30:00,047-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 05:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Validating all active sessions...
2026-02-12 05:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Finished session validation.  No sessions were stopped.
2026-02-12 06:00:00,008-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Firewall Ignore Patterns' [firewall.ignore-patterns] state change WAITING -> RUNNING
2026-02-12 06:00:00,013-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Synchronize Proprietary Names to IQ Server for repository *' [firewall.proprietary.name.sync] state change WAITING -> RUNNING
2026-02-12 06:00:00,013-0800 INFO  [quartz-10-thread-19]  *SYSTEM com.sonatype.nexus.clm.internal.FirewallIgnorePatternsTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.ignore-patterns-20260212060000010.log
2026-02-12 06:00:00,020-0800 INFO  [quartz-10-thread-4]  *SYSTEM com.sonatype.nexus.clm.internal.proprietary.datastore.DatastoreFirewallProprietaryNameTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260212060000019.log
2026-02-12 06:00:00,029-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 06:00:00,041-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 06:00:00,047-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 06:00:00,055-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 06:00:00,064-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 06:00:00,068-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 06:00:00,072-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 06:00:00,077-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 06:00:00,154-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Firewall Ignore Patterns' [firewall.ignore-patterns] state change RUNNING -> WAITING (OK)
2026-02-12 06:00:01,153-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Synchronize Proprietary Names to IQ Server for repository *' [firewall.proprietary.name.sync] state change RUNNING -> WAITING (OK)
2026-02-12 06:01:00,008-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change WAITING -> RUNNING
2026-02-12 06:01:00,159-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change RUNNING -> WAITING (OK)
2026-02-12 06:24:43,537-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: JBossMaven' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:24:44,037-0800 WARN  [quartz-10-thread-4]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:24:44,268-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: JBossMaven' [healthcheck] scheduled: hourly
2026-02-12 06:24:44,269-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: JBossMaven' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:24:54,258-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: JBossMaven' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:24:55,178-0800 INFO  [quartz-10-thread-4]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository JBossMaven
2026-02-12 06:24:55,190-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: JBossMaven' [healthcheck] scheduled: hourly
2026-02-12 06:24:55,192-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: JBossMaven' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:30:00,011-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 06:30:00,021-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 06:30:00,022-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 06:30:00,029-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 06:30:00,034-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 06:30:00,038-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 06:30:00,042-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 06:30:00,046-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 06:31:58,049-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: RedHatMaven' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:31:58,155-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_RedHatQuay' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:31:58,619-0800 WARN  [quartz-10-thread-19]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:31:59,092-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_DockerProxy' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:32:10,079-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: RedHatMaven' [healthcheck] scheduled: hourly
2026-02-12 06:32:10,080-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: RedHatMaven' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:32:10,347-0800 WARN  [quartz-10-thread-16]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:32:11,176-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: FTB_RedHatQuay' [healthcheck] scheduled: hourly
2026-02-12 06:32:11,178-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_RedHatQuay' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:32:11,433-0800 WARN  [quartz-10-thread-4]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:32:12,573-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: FTB_DockerProxy' [healthcheck] scheduled: hourly
2026-02-12 06:32:12,574-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_DockerProxy' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:32:20,070-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: RedHatMaven' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:32:20,474-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: RedHatMaven' [healthcheck] scheduled: hourly
2026-02-12 06:32:20,476-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: RedHatMaven' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:32:21,164-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_RedHatQuay' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:32:22,315-0800 INFO  [quartz-10-thread-16]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository FTB_RedHatQuay
2026-02-12 06:32:22,330-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: FTB_RedHatQuay' [healthcheck] scheduled: hourly
2026-02-12 06:32:22,331-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_RedHatQuay' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:32:22,566-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_DockerProxy' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:32:23,621-0800 INFO  [quartz-10-thread-16]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository FTB_DockerProxy
2026-02-12 06:32:23,634-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: FTB_DockerProxy' [healthcheck] scheduled: hourly
2026-02-12 06:32:23,636-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_DockerProxy' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:32:25,467-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: RedHatMaven' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:32:26,299-0800 INFO  [quartz-10-thread-16]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository RedHatMaven
2026-02-12 06:32:26,315-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: RedHatMaven' [healthcheck] scheduled: hourly
2026-02-12 06:32:26,317-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: RedHatMaven' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:38:28,137-0800 INFO  [periodic-4-thread-1]  *SYSTEM org.sonatype.nexus.internal.atlas.SystemInformationGeneratorImpl - Generating system information report
2026-02-12 06:46:00,640-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: maven-central' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:01,071-0800 WARN  [quartz-10-thread-16]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:46:01,077-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: nuget.org-proxy' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:01,962-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: Adobe' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:05,828-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: nuget_org_v2' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:06,603-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: pypi_proxy' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:06,796-0800 INFO  [quartz-10-thread-9]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: confluent-io' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:07,796-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: prisma_proxy' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:07,917-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: JitPack' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:08,139-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: m2e' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:32,496-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: maven-central' [healthcheck] scheduled: hourly
2026-02-12 06:46:32,498-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: maven-central' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:46:32,774-0800 WARN  [quartz-10-thread-4]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:46:33,574-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: nuget.org-proxy' [healthcheck] scheduled: hourly
2026-02-12 06:46:33,576-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: nuget.org-proxy' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:46:33,851-0800 WARN  [quartz-10-thread-8]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:46:34,604-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: m2e' [healthcheck] scheduled: hourly
2026-02-12 06:46:34,605-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: m2e' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:46:34,872-0800 WARN  [quartz-10-thread-13]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:46:35,622-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: JitPack' [healthcheck] scheduled: hourly
2026-02-12 06:46:35,623-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: JitPack' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:46:35,892-0800 WARN  [quartz-10-thread-6]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:46:36,476-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: primefaces' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:36,673-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: prisma_proxy' [healthcheck] scheduled: hourly
2026-02-12 06:46:36,675-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: prisma_proxy' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:46:37,185-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_RedHatDockerProxy' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:37,490-0800 WARN  [quartz-10-thread-20]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:46:38,332-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: Adobe' [healthcheck] scheduled: hourly
2026-02-12 06:46:38,333-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: Adobe' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:46:38,570-0800 WARN  [quartz-10-thread-13]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:46:39,127-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: Jenkins' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:43,569-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: nuget.org-proxy' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:44,596-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: m2e' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:45,617-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: JitPack' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:46,604-0800 INFO  [quartz-10-thread-14]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: npm_proxy' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:46,667-0800 INFO  [quartz-10-thread-15]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: prisma_proxy' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:48,328-0800 INFO  [quartz-10-thread-7]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: Adobe' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:49,493-0800 INFO  [quartz-10-thread-18]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: maven-central' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:46:58,459-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: primefaces' [healthcheck] scheduled: hourly
2026-02-12 06:46:58,463-0800 INFO  [quartz-10-thread-13]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: primefaces' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:46:58,711-0800 WARN  [quartz-10-thread-6]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:46:59,704-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: FTB_RedHatDockerProxy' [healthcheck] scheduled: hourly
2026-02-12 06:46:59,705-0800 INFO  [quartz-10-thread-6]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_RedHatDockerProxy' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:01,259-0800 INFO  [quartz-10-thread-18]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository maven-central
2026-02-12 06:47:01,276-0800 INFO  [quartz-10-thread-18]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: maven-central' [healthcheck] scheduled: hourly
2026-02-12 06:47:01,278-0800 INFO  [quartz-10-thread-18]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: maven-central' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:01,662-0800 WARN  [quartz-10-thread-19]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:47:04,702-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: nuget_org_v2' [healthcheck] scheduled: hourly
2026-02-12 06:47:04,703-0800 INFO  [quartz-10-thread-19]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: nuget_org_v2' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:05,812-0800 INFO  [quartz-10-thread-7]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository Adobe
2026-02-12 06:47:05,827-0800 INFO  [quartz-10-thread-7]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: Adobe' [healthcheck] scheduled: hourly
2026-02-12 06:47:05,828-0800 INFO  [quartz-10-thread-7]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: Adobe' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:06,003-0800 WARN  [quartz-10-thread-1]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:47:06,238-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: pypi_proxy' [healthcheck] scheduled: hourly
2026-02-12 06:47:06,239-0800 INFO  [quartz-10-thread-1]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: pypi_proxy' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:07,417-0800 INFO  [quartz-10-thread-15]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository prisma_proxy
2026-02-12 06:47:07,429-0800 INFO  [quartz-10-thread-15]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: prisma_proxy' [healthcheck] scheduled: hourly
2026-02-12 06:47:07,430-0800 INFO  [quartz-10-thread-15]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: prisma_proxy' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:07,610-0800 WARN  [quartz-10-thread-9]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:47:08,059-0800 INFO  [quartz-10-thread-9]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: confluent-io' [healthcheck] scheduled: hourly
2026-02-12 06:47:08,060-0800 INFO  [quartz-10-thread-9]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: confluent-io' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:08,246-0800 WARN  [quartz-10-thread-14]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:47:08,445-0800 INFO  [quartz-10-thread-9]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: primefaces' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:47:09,696-0800 INFO  [quartz-10-thread-15]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_RedHatDockerProxy' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:47:11,025-0800 INFO  [quartz-10-thread-14]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: npm_proxy' [healthcheck] scheduled: hourly
2026-02-12 06:47:11,027-0800 INFO  [quartz-10-thread-14]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: npm_proxy' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:11,110-0800 WARN  [quartz-10-thread-20]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 06:47:11,346-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: Jenkins' [healthcheck] scheduled: hourly
2026-02-12 06:47:11,348-0800 INFO  [quartz-10-thread-20]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: Jenkins' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:12,501-0800 INFO  [quartz-10-thread-15]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository FTB_RedHatDockerProxy
2026-02-12 06:47:12,514-0800 INFO  [quartz-10-thread-15]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: FTB_RedHatDockerProxy' [healthcheck] scheduled: hourly
2026-02-12 06:47:12,515-0800 INFO  [quartz-10-thread-15]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_RedHatDockerProxy' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:13,580-0800 INFO  [quartz-10-thread-8]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository nuget.org-proxy
2026-02-12 06:47:13,595-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: nuget.org-proxy' [healthcheck] scheduled: hourly
2026-02-12 06:47:13,596-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: nuget.org-proxy' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:14,693-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: nuget_org_v2' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:47:14,742-0800 INFO  [quartz-10-thread-9]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository primefaces
2026-02-12 06:47:14,779-0800 INFO  [quartz-10-thread-9]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: primefaces' [healthcheck] scheduled: hourly
2026-02-12 06:47:14,780-0800 INFO  [quartz-10-thread-9]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: primefaces' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:15,644-0800 INFO  [quartz-10-thread-4]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository m2e
2026-02-12 06:47:15,656-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: m2e' [healthcheck] scheduled: hourly
2026-02-12 06:47:15,657-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: m2e' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:16,237-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: pypi_proxy' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:47:16,642-0800 INFO  [quartz-10-thread-8]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository nuget_org_v2
2026-02-12 06:47:16,656-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: nuget_org_v2' [healthcheck] scheduled: hourly
2026-02-12 06:47:16,657-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: nuget_org_v2' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:17,790-0800 INFO  [quartz-10-thread-16]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository JitPack
2026-02-12 06:47:17,802-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: JitPack' [healthcheck] scheduled: hourly
2026-02-12 06:47:17,803-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: JitPack' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:18,052-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: confluent-io' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:47:18,570-0800 INFO  [quartz-10-thread-4]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository pypi_proxy
2026-02-12 06:47:18,583-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: pypi_proxy' [healthcheck] scheduled: hourly
2026-02-12 06:47:18,585-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: pypi_proxy' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:19,557-0800 INFO  [quartz-10-thread-16]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository confluent-io
2026-02-12 06:47:19,567-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: confluent-io' [healthcheck] scheduled: hourly
2026-02-12 06:47:19,568-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: confluent-io' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:21,020-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: npm_proxy' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:47:21,339-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: Jenkins' [healthcheck] state change WAITING -> RUNNING
2026-02-12 06:47:21,724-0800 INFO  [quartz-10-thread-16]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository npm_proxy
2026-02-12 06:47:21,735-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: npm_proxy' [healthcheck] scheduled: hourly
2026-02-12 06:47:21,736-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: npm_proxy' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:47:22,379-0800 INFO  [quartz-10-thread-4]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository Jenkins
2026-02-12 06:47:22,390-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: Jenkins' [healthcheck] scheduled: hourly
2026-02-12 06:47:22,391-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: Jenkins' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 06:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Validating all active sessions...
2026-02-12 06:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Finished session validation.  No sessions were stopped.
2026-02-12 07:00:00,010-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 07:00:00,023-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 07:00:00,024-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 07:00:00,032-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 07:00:00,035-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 07:00:00,039-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 07:00:00,043-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 07:00:00,046-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 07:01:00,007-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change WAITING -> RUNNING
2026-02-12 07:01:00,230-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change RUNNING -> WAITING (OK)
2026-02-12 07:08:18,677-0800 WARN  [qtp1952145369-93662]  M4879 org.sonatype.nexus.content.maven.internal.recipe.MavenProxyFacet - Unable to resolve url. Reason: Illegal character in path at index 42: gov/ca/ftb/app/itf/shared/SharedAppUIPom/${version.shared}/SharedAppUIPom-${version.shared}.pom
2026-02-12 07:08:18,678-0800 WARN  [qtp1952145369-93662]  M4879 org.sonatype.nexus.repository.httpbridge.internal.ViewServlet - Bad request. Reason: Invalid repository path
2026-02-12 07:08:18,709-0800 WARN  [qtp1952145369-93706]  M4879 org.sonatype.nexus.content.maven.internal.recipe.MavenProxyFacet - Unable to resolve url. Reason: Illegal character in path at index 42: gov/ca/ftb/app/itf/shared/SharedAppUIPom/${version.shared}/SharedAppUIPom-${version.shared}.pom
2026-02-12 07:08:18,710-0800 WARN  [qtp1952145369-93706]  M4879 org.sonatype.nexus.repository.httpbridge.internal.ViewServlet - Bad request. Reason: Invalid repository path
2026-02-12 07:08:18,785-0800 WARN  [qtp1952145369-93662]  M4879 org.sonatype.nexus.content.maven.internal.recipe.MavenProxyFacet - Unable to resolve url. Reason: Illegal character in path at index 42: gov/ca/ftb/app/itf/shared/SharedAppUIPom/${version.shared}/SharedAppUIPom-${version.shared}.pom
2026-02-12 07:08:18,785-0800 WARN  [qtp1952145369-93662]  M4879 org.sonatype.nexus.repository.httpbridge.internal.ViewServlet - Bad request. Reason: Invalid repository path
2026-02-12 07:28:53,596-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_GO' [healthcheck] state change WAITING -> RUNNING
2026-02-12 07:28:54,050-0800 WARN  [quartz-10-thread-8]  *SYSTEM com.sonatype.insight.scan.client.ClientScanner - Could not locate client info descriptor
2026-02-12 07:28:54,849-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: FTB_GO' [healthcheck] scheduled: hourly
2026-02-12 07:28:54,851-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_GO' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 07:29:04,840-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_GO' [healthcheck] state change WAITING -> RUNNING
2026-02-12 07:29:05,951-0800 INFO  [quartz-10-thread-8]  *SYSTEM com.sonatype.nexus.plugins.healthcheck.task.HealthCheckTask - Received health check report for repository FTB_GO
2026-02-12 07:29:05,963-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.scheduling.TaskSchedulerImpl - Task 'System - Repository Health Check: FTB_GO' [healthcheck] scheduled: hourly
2026-02-12 07:29:05,965-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'System - Repository Health Check: FTB_GO' [healthcheck] state change RUNNING -> WAITING (OK)
2026-02-12 07:30:00,009-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 07:30:00,021-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 07:30:00,021-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 07:30:00,031-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 07:30:00,035-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 07:30:00,039-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 07:30:00,042-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 07:30:00,045-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 07:48:28,138-0800 INFO  [periodic-4-thread-1]  *SYSTEM org.sonatype.nexus.internal.atlas.SystemInformationGeneratorImpl - Generating system information report
2026-02-12 07:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Validating all active sessions...
2026-02-12 07:59:08,806-0800 INFO  [SessionValidationThread-1]  *UNKNOWN org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Finished session validation.  No sessions were stopped.
2026-02-12 08:00:00,009-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Synchronize Proprietary Names to IQ Server for repository *' [firewall.proprietary.name.sync] state change WAITING -> RUNNING
2026-02-12 08:00:00,016-0800 INFO  [quartz-10-thread-4]  *SYSTEM com.sonatype.nexus.clm.internal.proprietary.datastore.DatastoreFirewallProprietaryNameTask - Task log: /opt/appdata/nexus/sonatype-work/nexus3/log/tasks/firewall.proprietary.name.sync-20260212080000015.log
2026-02-12 08:00:00,047-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 08:00:00,056-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 08:00:00,058-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused raw blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 08:00:00,066-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused nuget blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 08:00:00,070-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 08:00:00,074-0800 INFO  [quartz-10-thread-16]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused pypi blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 08:00:00,077-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change WAITING -> RUNNING
2026-02-12 08:00:00,081-0800 INFO  [quartz-10-thread-8]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Cleanup unused helm blobs from nexus' [assetBlob.cleanup] state change RUNNING -> WAITING (OK)
2026-02-12 08:00:01,159-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Synchronize Proprietary Names to IQ Server for repository *' [firewall.proprietary.name.sync] state change RUNNING -> WAITING (OK)
2026-02-12 08:01:00,006-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change WAITING -> RUNNING
2026-02-12 08:01:00,153-0800 INFO  [quartz-10-thread-4]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Metric aggregation' [content.usage.aggregation] state change RUNNING -> WAITING (OK)
2026-02-12 08:27:16,077-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@25c489f0{SSL, (ssl, http/1.1)}{0.0.0.0:8444}
2026-02-12 08:27:16,083-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@58210b27{SSL, (ssl, http/1.1)}{0.0.0.0:18090}
2026-02-12 08:27:16,092-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@14dbad50{SSL, (ssl, http/1.1)}{0.0.0.0:18083}
2026-02-12 08:27:16,093-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@6d15b9fa{SSL, (ssl, http/1.1)}{0.0.0.0:13444}
2026-02-12 08:27:16,099-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@3b5f9917{SSL, (ssl, http/1.1)}{0.0.0.0:18079}
2026-02-12 08:27:16,099-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@566ff36e{SSL, (ssl, http/1.1)}{0.0.0.0:13443}
2026-02-12 08:27:16,105-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@26fe7ab1{SSL, (ssl, http/1.1)}{0.0.0.0:18092}
2026-02-12 08:27:16,110-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@268b8f25{SSL, (ssl, http/1.1)}{0.0.0.0:18084}
2026-02-12 08:27:16,120-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@483516b1{SSL, (ssl, http/1.1)}{0.0.0.0:18080}
2026-02-12 08:27:16,126-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@49563a62{SSL, (ssl, http/1.1)}{0.0.0.0:18076}
2026-02-12 08:27:16,132-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@78b63e8a{SSL, (ssl, http/1.1)}{0.0.0.0:18082}
2026-02-12 08:27:16,138-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@30eb63df{SSL, (ssl, http/1.1)}{0.0.0.0:18091}
2026-02-12 08:27:16,145-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@6d552336{SSL, (ssl, http/1.1)}{0.0.0.0:18077}
2026-02-12 08:27:16,150-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@7983cbd4{SSL, (ssl, http/1.1)}{0.0.0.0:18078}
2026-02-12 08:27:16,156-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@1b4315b4{SSL, (ssl, http/1.1)}{0.0.0.0:18081}
2026-02-12 08:27:16,161-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@378e1eb{SSL, (ssl, http/1.1)}{0.0.0.0:18086}
2026-02-12 08:27:16,166-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.AbstractConnector - Stopped ServerConnector@5b7538fd{SSL, (ssl, http/1.1)}{0.0.0.0:18085}
2026-02-12 08:27:16,166-0800 INFO  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.server.session - node0 Stopped scavenging
2026-02-12 08:27:16,171-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.repository.httpbridge.internal.ViewServlet - Destroyed
2026-02-12 08:27:16,171-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.repository.httpbridge.internal.ViewServlet - Destroyed
2026-02-12 08:27:16,172-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.siesta.SiestaServlet - Destroyed
2026-02-12 08:27:16,173-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.bootstrap.osgi.BootstrapListener - Destroying
2026-02-12 08:27:16,189-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.extender.NexusContextListener - Uptime: 297 hours, 29 minutes, 14 seconds and 872 milliseconds (nexus-pro-edition/3.70.1.02)
2026-02-12 08:27:16,189-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Shutting down
2026-02-12 08:27:16,190-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop TASKS
2026-02-12 08:27:16,200-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.quartz.internal.datastore.DatastoreQuartzSchedulerSPI - Scheduler put into stand-by mode
2026-02-12 08:27:16,204-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop CAPABILITIES
2026-02-12 08:27:16,213-0800 INFO  [JettyShutdownThread]  *SYSTEM com.sonatype.nexus.migration.assistant.datastore.MigrationAssistantImpl - Resetting
2026-02-12 08:27:16,217-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.repository.content.browse.BrowseEventHandler - BrowseNode event processing has been resumed
2026-02-12 08:27:16,219-0800 INFO  [JettyShutdownThread]  *SYSTEM com.sonatype.nexus.migration.assistant.datastore.MigrationAssistantImpl - Reset
2026-02-12 08:27:16,224-0800 INFO  [JettyShutdownThread]  *SYSTEM com.sonatype.nexus.clm.internal.capability.FirewallAuditCapability - Deactivating auditing capability on repository: npm_proxy, Nexus Active: false
2026-02-12 08:27:16,227-0800 INFO  [JettyShutdownThread]  *SYSTEM com.sonatype.nexus.clm.internal.capability.FirewallAuditCapability - Deactivating auditing capability on repository: maven-central, Nexus Active: false
2026-02-12 08:27:16,240-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.quartz.internal.task.QuartzTaskInfo - Task 'Statistics - recalculate vulnerabilities statistics' [repository.vulnerability.statistics] removed
2026-02-12 08:27:16,242-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop REPOSITORIES
2026-02-12 08:27:16,251-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=olm-ftb, scheme=https, port=18092}
2026-02-12 08:27:16,253-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=OCP_CertifiedGroup, scheme=https, port=18085}
2026-02-12 08:27:16,257-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=ocp, scheme=https, port=18090}
2026-02-12 08:27:16,258-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=CDS_Dev, scheme=https, port=18082}
2026-02-12 08:27:16,260-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=FTB_RedHatDockerProxy, scheme=https, port=18076}
2026-02-12 08:27:16,261-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=FTB_DockerHosted, scheme=https, port=18080}
2026-02-12 08:27:16,262-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=SIP_Development, scheme=https, port=13443}
2026-02-12 08:27:16,263-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=FTB_RedHatDockerGroup, scheme=https, port=18078}
2026-02-12 08:27:16,264-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=OCP_DevGroup, scheme=https, port=18084}
2026-02-12 08:27:16,265-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=CDS_Certified, scheme=https, port=18083}
2026-02-12 08:27:16,267-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=FTB_RedHatDockerHosted, scheme=https, port=18077}
2026-02-12 08:27:16,268-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=FTB_DockerProxy, scheme=https, port=18081}
2026-02-12 08:27:16,269-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=olm-mirror, scheme=https, port=18091}
2026-02-12 08:27:16,269-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=FTB_DockerGroup, scheme=https, port=18079}
2026-02-12 08:27:16,270-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=SIP_Quarantine, scheme=https, port=13444}
2026-02-12 08:27:16,271-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.internal.jetty.ConnectorRegistrarImpl - Removing connector configuration DockerConnectorConfiguration{repositoryName=FTB_RedHatQuay, scheme=https, port=18086}
2026-02-12 08:27:16,276-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop SERVICES
2026-02-12 08:27:16,287-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'SYSTEM_INFORMATION' removed from EhcacheManager.
2026-02-12 08:27:16,288-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'SYSTEM_INFORMATION' successfully destroyed in EhcacheManager.
2026-02-12 08:27:16,301-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop SECURITY
2026-02-12 08:27:16,302-0800 INFO  [JettyShutdownThread]  *SYSTEM org.apache.shiro.session.mgt.AbstractValidatingSessionManager - Disabled session validation scheduler.
2026-02-12 08:27:16,303-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop EVENTS
2026-02-12 08:27:16,303-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop SCHEMAS
2026-02-12 08:27:16,303-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop UPGRADE
2026-02-12 08:27:16,305-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop RESTORE
2026-02-12 08:27:16,305-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop STORAGE
2026-02-12 08:27:16,308-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'enterprise-ldap' removed from EhcacheManager.
2026-02-12 08:27:16,308-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'SelectorManager' removed from EhcacheManager.
2026-02-12 08:27:16,308-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'NexusAuthorizingRealm.authorizationCache' removed from EhcacheManager.
2026-02-12 08:27:16,309-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'nuget_org_v2#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,309-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'RedHatMaven#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,309-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'nuget.org-proxy#odata-query-cache' removed from EhcacheManager.
2026-02-12 08:27:16,309-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'pypi_proxy#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,310-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'nuget_org_v2#odata-query-cache' removed from EhcacheManager.
2026-02-12 08:27:16,310-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'JBossMaven#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,310-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'confluent-io#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,310-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'npm_proxynpm-audit-data' removed from EhcacheManager.
2026-02-12 08:27:16,310-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'NexusAuthenticatingRealm.authenticationCache' removed from EhcacheManager.
2026-02-12 08:27:16,310-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'primefaces#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,311-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'Adobe#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,311-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'FTB_RedHatDockerProxy#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,311-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'FTB_RedHatQuay#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,311-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'FTB_npm_Groupnpm-audit-data' removed from EhcacheManager.
2026-02-12 08:27:16,311-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'FTB_DockerProxy#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,312-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'npm_proxy#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,312-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'Jenkins#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,312-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'nuget.org-proxy#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,312-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'prisma_proxy#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,313-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'DockerToken.authenticationCache' removed from EhcacheManager.
2026-02-12 08:27:16,313-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'FTB_NuGet_Group#odata-query-cache' removed from EhcacheManager.
2026-02-12 08:27:16,313-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'm2e#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,313-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'nuget-group#odata-query-cache' removed from EhcacheManager.
2026-02-12 08:27:16,313-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'JitPack#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,314-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'shiro-activeSessionCache' removed from EhcacheManager.
2026-02-12 08:27:16,314-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'LdapRealm.authorizationCache' removed from EhcacheManager.
2026-02-12 08:27:16,314-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'maven-central#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,314-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'FTB_GO#negative-cache' removed from EhcacheManager.
2026-02-12 08:27:16,314-0800 INFO  [JettyShutdownThread]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'FIREWALL.ONBOARDING.SYNCHRONIZATION.TASK' removed from EhcacheManager.
2026-02-12 08:27:16,376-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.cache.internal.ehcache.EhCacheManagerProvider - Cache-manager closed
2026-02-12 08:27:16,377-0800 INFO  [JettyShutdownThread]  *SYSTEM org.elasticsearch.node - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] stopping ...
2026-02-12 08:27:16,414-0800 INFO  [JettyShutdownThread]  *SYSTEM org.elasticsearch.node - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] stopped
2026-02-12 08:27:16,414-0800 INFO  [JettyShutdownThread]  *SYSTEM org.elasticsearch.node - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] closing ...
2026-02-12 08:27:16,424-0800 INFO  [JettyShutdownThread]  *SYSTEM org.elasticsearch.node - [CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585] closed
2026-02-12 08:27:16,429-0800 INFO  [JettyShutdownThread]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Shutdown initiated...
2026-02-12 08:27:16,449-0800 INFO  [JettyShutdownThread]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Shutdown completed.
2026-02-12 08:27:16,449-0800 INFO  [JettyShutdownThread]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop KERNEL
2026-02-12 09:47:19,860-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.configuration.NexusProperties - nexus.properties: {ssl.etc=/opt/appdata/nexus/sonatype-work/nexus3/etc/ssl, nexus-edition=nexus-pro-edition, java.specification.version=21, nexus-db-feature=nexus-datastore-mybatis, javax.net.ssl.trustStorePassword=edrcmadm, sun.jnu.encoding=UTF-8, nexus.view.exhaustForAgents=Apache-Maven.*|libwww-perl.*, sun.arch.data.model=64, java.vendor.url=https://adoptium.net/, nexus.session.enabled=true, nexus.scripts.allowCreation=true, sun.boot.library.path=/opt/appdata/nexus/nexus-3.89.0-09/jdk/temurin_21.0.9_10_linux_x86_64/jdk-21.0.9+10/lib, sun.java.command=/opt/appdata/nexus/nexus-3.89.0-09/bin/sonatype-nexus-repository-3.89.0-09.jar, logging.register-shutdown-hook=false, jdk.debug=release, java.specification.vendor=Oracle Corporation, java.version.date=2025-10-21, java.home=/opt/appdata/nexus/nexus-3.89.0-09/jdk/temurin_21.0.9_10_linux_x86_64/jdk-21.0.9+10, logging.config=etc/logback/logback.xml, nexus-features=nexus-pro-feature, file.separator=/, java.vm.compressedOopsMode=Zero based, line.separator=
, nexus.onboarding.enabled=true, java.vm.specification.vendor=Oracle Corporation, java.specification.name=Java Platform API Specification, spring.config.location=etc/default-application.properties, application-host=0.0.0.0, javax.net.ssl.trustStore=/opt/appdata/nexus/sonatype-work/nexus3/etc/ssl/nexusrepo.jks, jdk.tls.ephemeralDHKeySize=2048, nexus-context-path=/, java.util.logging.config.file=etc/spring/java.util.logging.properties, java.protocol.handler.pkgs=org.springframework.boot.loader.net.protocol, sun.management.compiler=HotSpot 64-Bit Tiered Compilers, karaf.home=., java.runtime.version=21.0.9+10-LTS, user.name=nexus, nexus.jwt.enabled=false, file.encoding=UTF-8, java.vendor.version=Temurin-21.0.9+10, java.io.tmpdir=/opt/appdata/nexus/sonatype-work/nexus3/tmp, logback.etc=/opt/appdata/nexus/nexus-3.89.0-09/etc/logback, java.version=21.0.9, fabric.etc=/opt/appdata/nexus/nexus-3.89.0-09/etc/fabric, java.vm.specification.name=Java Virtual Machine Specification, PID=2203498, nexus.change.repo.blobstore.task.enabled=true, CONSOLE_LOG_CHARSET=UTF-8, native.encoding=UTF-8, java.library.path=/usr/java/packages/lib:/usr/lib64:/lib64:/lib:/usr/lib, stderr.encoding=UTF-8, java.vendor=Eclipse Adoptium, karaf.base=/opt/appdata/nexus/nexus-3.89.0-09, sun.io.unicode.encoding=UnicodeLittle, karaf.log=/opt/appdata/nexus/sonatype-work/nexus3/log, java.class.path=/opt/appdata/nexus/nexus-3.89.0-09/bin/sonatype-nexus-repository-3.89.0-09.jar, karaf.etc=/opt/appdata/nexus/nexus-3.89.0-09/etc/karaf, nexus.assetdownloads.enabled=true, java.vm.vendor=Eclipse Adoptium, nexus.installer.type=linux-x86-64, user.timezone=America/Los_Angeles, org.jboss.logging.provider=slf4j, application-port=8081, java.vm.specification.version=21, os.name=Linux, sun.java.launcher=SUN_STANDARD, user.country=US, karaf.data=/opt/appdata/nexus/sonatype-work/nexus3, nexus.zero.downtime.enabled=false, karaf.instances=/opt/appdata/nexus/sonatype-work/nexus3/instances, sun.cpu.endian=little, user.home=/home/nexus, user.language=en, javax.net.ssl.keyStorePassword=edrcmadm, jetty.etc=/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty, FILE_LOG_CHARSET=UTF-8, java.awt.headless=true, nexus.http.denyframe.enabled=true, java.net.preferIPv4Stack=true, nexus.datastore.enabled=true, stdout.encoding=UTF-8, path.separator=:, os.version=4.18.0-553.89.1.el8_10.x86_64, java.runtime.name=OpenJDK Runtime Environment, nexus-args=/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty/jetty.xml,/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty/jetty-https.xml,/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty/jetty-requestlog.xml, nexus.quartz.jobstore.jdbc=true, java.vm.name=OpenJDK 64-Bit Server VM, javax.net.ssl.keyStore=/opt/appdata/nexus/sonatype-work/nexus3/etc/ssl/nexusrepo.jks, java.vendor.url.bug=https://github.com/adoptium/adoptium-support/issues, nexus.security.oauth2.enabled=false, org.sonatype.nexus.repository.httpbridge.internal.HttpBridgeModule.legacy=true, user.dir=/opt/appdata/nexus/nexus-3.89.0-09, os.arch=amd64, java.vm.info=mixed mode, sharing, java.vm.version=21.0.9+10-LTS, application-port-ssl=8444, java.class.version=65.0}
2026-02-12 09:47:19,868-0800 INFO  [main]  *SYSTEM com.sonatype.nexus.bootstrap.entrypoint.pro.SonatypeNexusRepositoryApplication - Starting SonatypeNexusRepositoryApplication v3.89.0-09 using Java 21.0.9 with PID 2203498 (/opt/appdata/nexus/nexus-3.89.0-09/bin/sonatype-nexus-repository-3.89.0-09.jar started by nexus in /opt/appdata/nexus/nexus-3.89.0-09)
2026-02-12 09:47:19,869-0800 INFO  [main]  *SYSTEM com.sonatype.nexus.bootstrap.entrypoint.pro.SonatypeNexusRepositoryApplication - No active profile set, falling back to 1 default profile: "default"
2026-02-12 09:47:21,941-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.ApplicationLauncher - Starting nexus with edition PRO
2026-02-12 09:47:22,275-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.SpringComponentScan - Scanning for components in packages: [org.sonatype.nexus, com.sonatype.nexus]
2026-02-12 09:47:33,151-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.quartz.internal.QuartzSchedulerProvider - Thread-pool size: 20, Thread-pool priority: 5
2026-02-12 09:47:33,505-0800 INFO  [main]  *SYSTEM org.opensaml.core.config.InitializationService - Initializing OpenSAML using the Java Services API
2026-02-12 09:47:35,840-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.log.overrides.file.LogbackLoggerOverrides - File: /opt/appdata/nexus/sonatype-work/nexus3/etc/logback/logback-overrides.xml
2026-02-12 09:47:35,882-0800 INFO  [main]  *SYSTEM org.apache.shiro.nexus.NexusWebSessionManager - Global session timeout: 1800000 ms
2026-02-12 09:47:35,883-0800 INFO  [main]  *SYSTEM org.apache.shiro.nexus.NexusWebSessionManager - Session-cookie prototype: name=NXSESSIONID, secure=true
2026-02-12 09:47:37,290-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle - UI plugin descriptors:
2026-02-12 09:47:37,290-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-rapture
2026-02-12 09:47:37,290-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-coreui-plugin
2026-02-12 09:47:37,290-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle - ExtJS UI plugin descriptors:
2026-02-12 09:47:37,290-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-rapture
2026-02-12 09:47:37,290-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-rutauth-plugin
2026-02-12 09:47:37,290-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-proximanova-plugin
2026-02-12 09:47:37,290-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-coreui-plugin
2026-02-12 09:47:37,290-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-proui-plugin
2026-02-12 09:47:37,290-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-cargo
2026-02-12 09:47:37,290-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-composer
2026-02-12 09:47:37,291-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-onboarding-plugin
2026-02-12 09:47:37,291-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-maven
2026-02-12 09:47:37,291-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-docker
2026-02-12 09:47:37,291-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-rubygems
2026-02-12 09:47:37,291-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-npm
2026-02-12 09:47:37,291-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-nuget
2026-02-12 09:47:37,291-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-pypi
2026-02-12 09:47:37,291-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-saml-plugin
2026-02-12 09:47:37,291-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-analytics-plugin
2026-02-12 09:47:37,312-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.webresources.WebResourceServlet - Max-age: 30 days (2592000 seconds)
2026-02-12 09:47:37,319-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.wonderland.DownloadServiceImpl - Downloads directory: /opt/appdata/nexus/sonatype-work/nexus3/downloads
2026-02-12 09:47:37,596-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.atlas.SupportZipGeneratorImpl - Maximum included file size: 30 megabytes
2026-02-12 09:47:37,597-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.atlas.SupportZipGeneratorImpl - Maximum ZIP file size: 50 megabytes
2026-02-12 09:47:38,114-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.script.ScriptEngineManagerProvider - Detected 1 engine-factories
2026-02-12 09:47:38,116-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.script.ScriptEngineManagerProvider - Engine-factory: Groovy Scripting Engine v2.0; language=Groovy, version=3.0.19, names=[groovy, Groovy], mime-types=[application/x-groovy], extensions=[groovy]
2026-02-12 09:47:38,116-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.script.ScriptEngineManagerProvider - Default language: groovy
2026-02-12 09:47:38,540-0800 INFO  [main]  *SYSTEM org.hibernate.validator.internal.util.Version - HV000001: Hibernate Validator 6.2.0.Final
2026-02-12 09:47:39,170-0800 INFO  [main]  *SYSTEM com.sonatype.nexus.common.configuration.ConfigurationService - ConfigurationSources ordered: [RoutingRuleConfigurationSource, BlobStoreConfigurationSource, CleanupPolicyConfigurationSource, HttpClientConfigurationSource, PrivilegeConfigurationSource, RoleConfigurationSource, RealmConfigurationSource, AnonymousConfigurationSource, SelectorConfigurationSource, RepositoryConfigurationSource, CapabilityConfigurationSource, TaskConfigurationSource, EmailConfigurationSource, ScriptConfigurationSource, LdapConfigurationSource, FirewallIgnorePatternsConfigurationSource, RepositoryHealthCheckConfigurationSource, NodeHeartbeatConfigurationSource, ChangeRepositoryBlobStoreConfigurationSource, SamlConfigurationSource, SamlUserConfigurationSource, TagConfigurationSource]
2026-02-12 09:47:39,448-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.cache.internal.ehcache.EhCacheManagerProvider - Creating cache-manager with configuration: file:/opt/appdata/nexus/nexus-3.89.0-09/etc/fabric/ehcache.xml
2026-02-12 09:47:39,993-0800 INFO  [main]  *SYSTEM org.ehcache.jsr107.ConfigurationMerger - Configuration of cache MALICIOUS_RISK_ON_DISK_CACHE will be supplemented by template nexus-default
2026-02-12 09:47:40,075-0800 INFO  [main]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'MALICIOUS_RISK_ON_DISK_CACHE' created in EhcacheManager.
2026-02-12 09:47:40,090-0800 INFO  [main]  *SYSTEM org.ehcache.jsr107.Eh107CacheManager - Registering Ehcache MBean javax.cache:type=CacheConfiguration,CacheManager=file./opt/appdata/nexus/nexus-3.89.0-09/etc/fabric/ehcache.xml,Cache=MALICIOUS_RISK_ON_DISK_CACHE
2026-02-12 09:47:40,092-0800 INFO  [main]  *SYSTEM org.ehcache.jsr107.Eh107CacheManager - Registering Ehcache MBean javax.cache:type=CacheStatistics,CacheManager=file./opt/appdata/nexus/nexus-3.89.0-09/etc/fabric/ehcache.xml,Cache=MALICIOUS_RISK_ON_DISK_CACHE
2026-02-12 09:47:40,096-0800 INFO  [main]  *SYSTEM org.ehcache.jsr107.ConfigurationMerger - Configuration of cache ENABLED_REGISTRIES will be supplemented by template nexus-default
2026-02-12 09:47:40,099-0800 INFO  [main]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'ENABLED_REGISTRIES' created in EhcacheManager.
2026-02-12 09:47:40,099-0800 INFO  [main]  *SYSTEM org.ehcache.jsr107.Eh107CacheManager - Registering Ehcache MBean javax.cache:type=CacheConfiguration,CacheManager=file./opt/appdata/nexus/nexus-3.89.0-09/etc/fabric/ehcache.xml,Cache=ENABLED_REGISTRIES
2026-02-12 09:47:40,100-0800 INFO  [main]  *SYSTEM org.ehcache.jsr107.Eh107CacheManager - Registering Ehcache MBean javax.cache:type=CacheStatistics,CacheManager=file./opt/appdata/nexus/nexus-3.89.0-09/etc/fabric/ehcache.xml,Cache=ENABLED_REGISTRIES
2026-02-12 09:47:40,376-0800 INFO  [main]  *SYSTEM com.sonatype.nexus.repository.swift.internal.provider.SwiftProviderRegistry - Registered 1 Git providers: [github]
2026-02-12 09:47:40,625-0800 INFO  [main]  *SYSTEM org.springframework.beans.factory.annotation.AutowiredAnnotationBeanPostProcessor - Inconsistent constructor declaration on bean with name 'maliciousRiskOnDiskAnalytics': single autowire-marked constructor flagged as optional - this constructor is effectively required since there is no default constructor to fall back to: public com.sonatype.analytics.internal.MaliciousRiskOnDiskAnalytics(com.sonatype.nexus.risk.visualizer.MaliciousRiskService,java.lang.Boolean)
2026-02-12 09:47:40,915-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Starting jetty
2026-02-12 09:47:40,931-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Applying configuration: file:/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty/jetty.xml
2026-02-12 09:47:41,456-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Applying configuration: file:/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty/jetty-https.xml
2026-02-12 09:47:41,543-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Applying configuration: file:/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty/jetty-requestlog.xml
2026-02-12 09:47:41,611-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Starting: oejs.Server@7cf22ec3{STOPPED}[12.0.17,sto=5000]
2026-02-12 09:47:41,617-0800 INFO  [jetty-main-1]  *SYSTEM org.eclipse.jetty.server.Server - jetty-12.0.17; built: 2025-03-03T13:15:05.903Z; git: 14d19c268e4cb09afc312b5255a4cbb7a95c5cb6; jvm 21.0.9+10-LTS
2026-02-12 09:47:41,956-0800 INFO  [jetty-main-1]  *SYSTEM org.eclipse.jetty.session.DefaultSessionIdManager - Session workerName=node0
2026-02-12 09:47:41,981-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.internal.NexusServletContextListener - Running lifecycle phases [KERNEL, STORAGE, RESTORE, UPGRADE, SCHEMAS, EVENTS, SECURITY, SERVICES, REPOSITORIES, CAPABILITIES, TASKS]
2026-02-12 09:47:42,085-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Indexing lifecycle managed components up to phase TASKS
2026-02-12 09:47:42,086-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start KERNEL
2026-02-12 09:47:42,089-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.internal.log.LogbackLogManager - Configuring
2026-02-12 09:47:42,099-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start STORAGE
2026-02-12 09:47:42,111-0800 INFO  [jetty-main-1]  *SYSTEM com.sonatype.nexus.self.hosted.datastore.DataStoreConfigurationFileSource - Loaded 'nexus' data store configuration from properties file (postgresql)
2026-02-12 09:47:42,133-0800 WARN  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - Database directory contains unsupported legacy database files; remove legacy files as soon as possible.
2026-02-12 09:47:42,144-0800 INFO  [jetty-main-1]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Starting...
2026-02-12 09:47:42,272-0800 INFO  [jetty-main-1]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Start completed.
2026-02-12 09:47:42,274-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Loading MyBatis configuration from /opt/appdata/nexus/nexus-3.89.0-09/etc/fabric/mybatis.xml
2026-02-12 09:47:42,374-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - MyBatis databaseId: PostgreSQL
2026-02-12 09:47:42,526-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DeploymentIdDAO
2026-02-12 09:47:42,568-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NodeIdDAO
2026-02-12 09:47:42,587-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AnonymousConfigurationDAO
2026-02-12 09:47:42,606-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CPrivilegeDAO
2026-02-12 09:47:42,618-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CRoleDAO
2026-02-12 09:47:42,632-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CUserRoleMappingDAO
2026-02-12 09:47:42,645-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CUserDAO
2026-02-12 09:47:42,657-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RealmConfigurationDAO
2026-02-12 09:47:42,669-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SecretsDAO
2026-02-12 09:47:42,923-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SoftDeletedBlobsDAO
2026-02-12 09:47:42,935-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CleanupPolicyDAO
2026-02-12 09:47:42,951-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CapabilityStorageItemDAO
2026-02-12 09:47:42,964-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for EmailConfigurationDAO
2026-02-12 09:47:42,976-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HttpClientConfigurationDAO
2026-02-12 09:47:42,991-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ApiKeyDAO
2026-02-12 09:47:43,006-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ApiKeyV2DAO
2026-02-12 09:47:43,117-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SelectorConfigurationDAO
2026-02-12 09:47:43,130-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NexusKeyValueDAO
2026-02-12 09:47:43,143-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for QuartzDAO
2026-02-12 09:47:43,160-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConfigurationDAO
2026-02-12 09:47:43,174-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for BlobStoreConfigurationDAO
2026-02-12 09:47:43,241-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RoutingRuleDAO
2026-02-12 09:47:43,253-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for BlobStoreMetricsDAO
2026-02-12 09:47:43,265-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for UpgradeTaskDAO
2026-02-12 09:47:43,277-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ScriptDAO
2026-02-12 09:47:43,311-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SearchTableDAO
2026-02-12 09:47:43,486-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for LdapConfigurationDAO
2026-02-12 09:47:43,498-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for KeyStoreDAO
2026-02-12 09:47:43,511-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TrustedSSLCertificateDAO
2026-02-12 09:47:43,606-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComponentApplicationScanScheduleDAO
2026-02-12 09:47:43,619-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComponentApplicationScanDAO
2026-02-12 09:47:43,632-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ReconcilePlanDetailsDAO
2026-02-12 09:47:43,759-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ReconcilePlanDAO
2026-02-12 09:47:43,899-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DistributedEventDAO
2026-02-12 09:47:44,011-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CacheDAO
2026-02-12 09:47:44,121-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SupportZipInfoDAO
2026-02-12 09:47:44,245-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DistributedAuthTicketCacheDAO
2026-02-12 09:47:44,317-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for FirewallIgnorePatternsDAO
2026-02-12 09:47:44,327-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RepositoryHealthCheckConfigurationDAO
2026-02-12 09:47:44,337-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for MalwareRemediatorTaskDAO
2026-02-12 09:47:44,458-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RepositoryMetricsDAO
2026-02-12 09:47:44,473-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NodeHeartbeatDAO
2026-02-12 09:47:44,573-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ChangeRepositoryBlobstoreDAO
2026-02-12 09:47:44,583-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SamlAuthenticationRequestDAO
2026-02-12 09:47:44,683-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SamlConfigurationDAO
2026-02-12 09:47:44,695-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SamlUserDAO
2026-02-12 09:47:44,708-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TagDAO
2026-02-12 09:47:44,720-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for UserTokenRecordDAO
2026-02-12 09:47:44,732-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AggregatedMetricsDAO
2026-02-12 09:47:44,745-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for MetricDAO
2026-02-12 09:47:44,763-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SwiftComponentTagDAO
2026-02-12 09:47:44,886-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptContentRepositoryDAO
2026-02-12 09:47:44,916-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptComponentDAO
2026-02-12 09:47:44,933-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptAssetBlobDAO
2026-02-12 09:47:44,955-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptAssetDAO
2026-02-12 09:47:44,971-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptBrowseNodeDAO
2026-02-12 09:47:44,985-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptKeyValueDAO
2026-02-12 09:47:44,997-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2ContentRepositoryDAO
2026-02-12 09:47:45,019-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2ComponentDAO
2026-02-12 09:47:45,034-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2AssetBlobDAO
2026-02-12 09:47:45,054-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2AssetDAO
2026-02-12 09:47:45,068-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2BrowseNodeDAO
2026-02-12 09:47:45,080-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawContentRepositoryDAO
2026-02-12 09:47:45,096-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawComponentDAO
2026-02-12 09:47:45,110-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawAssetBlobDAO
2026-02-12 09:47:45,128-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawAssetDAO
2026-02-12 09:47:45,142-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawBrowseNodeDAO
2026-02-12 09:47:45,153-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoContentRepositoryDAO
2026-02-12 09:47:45,325-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoComponentDAO
2026-02-12 09:47:45,476-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoAssetBlobDAO
2026-02-12 09:47:45,608-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoAssetDAO
2026-02-12 09:47:45,780-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoBrowseNodeDAO
2026-02-12 09:47:45,960-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsContentRepositoryDAO
2026-02-12 09:47:45,976-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsComponentDAO
2026-02-12 09:47:45,991-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsAssetBlobDAO
2026-02-12 09:47:46,009-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsAssetDAO
2026-02-12 09:47:46,023-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsBrowseNodeDAO
2026-02-12 09:47:46,034-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComposerContentRepositoryDAO
2026-02-12 09:47:46,170-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComposerComponentDAO
2026-02-12 09:47:46,353-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComposerAssetBlobDAO
2026-02-12 09:47:46,491-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComposerAssetDAO
2026-02-12 09:47:46,673-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComposerBrowseNodeDAO
2026-02-12 09:47:46,857-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanContentRepositoryDAO
2026-02-12 09:47:46,874-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanComponentDAO
2026-02-12 09:47:46,889-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanAssetBlobDAO
2026-02-12 09:47:46,906-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanAssetDAO
2026-02-12 09:47:46,920-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanBrowseNodeDAO
2026-02-12 09:47:46,933-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaContentRepositoryDAO
2026-02-12 09:47:46,949-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaComponentDAO
2026-02-12 09:47:46,963-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaAssetBlobDAO
2026-02-12 09:47:46,981-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaAssetDAO
2026-02-12 09:47:46,995-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaBrowseNodeDAO
2026-02-12 09:47:47,007-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerContentRepositoryDAO
2026-02-12 09:47:47,022-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerComponentDAO
2026-02-12 09:47:47,037-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerAssetBlobDAO
2026-02-12 09:47:47,053-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerAssetDAO
2026-02-12 09:47:47,067-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerBrowseNodeDAO
2026-02-12 09:47:47,077-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerForeignLayersDAO
2026-02-12 09:47:47,087-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsContentRepositoryDAO
2026-02-12 09:47:47,102-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsComponentDAO
2026-02-12 09:47:47,115-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsAssetBlobDAO
2026-02-12 09:47:47,131-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsAssetDAO
2026-02-12 09:47:47,144-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsBrowseNodeDAO
2026-02-12 09:47:47,155-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoContentRepositoryDAO
2026-02-12 09:47:47,169-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoComponentDAO
2026-02-12 09:47:47,183-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoAssetBlobDAO
2026-02-12 09:47:47,199-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoAssetDAO
2026-02-12 09:47:47,211-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoBrowseNodeDAO
2026-02-12 09:47:47,223-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmContentRepositoryDAO
2026-02-12 09:47:47,237-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmComponentDAO
2026-02-12 09:47:47,251-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmAssetBlobDAO
2026-02-12 09:47:47,268-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmAssetDAO
2026-02-12 09:47:47,281-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmBrowseNodeDAO
2026-02-12 09:47:47,293-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmKeyValueDAO
2026-02-12 09:47:47,304-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HuggingFaceContentRepositoryDAO
2026-02-12 09:47:47,438-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HuggingFaceComponentDAO
2026-02-12 09:47:47,584-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HuggingFaceAssetBlobDAO
2026-02-12 09:47:47,712-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HuggingFaceAssetDAO
2026-02-12 09:47:47,878-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HuggingFaceBrowseNodeDAO
2026-02-12 09:47:48,074-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmContentRepositoryDAO
2026-02-12 09:47:48,088-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmComponentDAO
2026-02-12 09:47:48,101-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmAssetBlobDAO
2026-02-12 09:47:48,117-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmAssetDAO
2026-02-12 09:47:48,129-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmBrowseNodeDAO
2026-02-12 09:47:48,141-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmKeyValueDAO
2026-02-12 09:47:48,260-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetContentRepositoryDAO
2026-02-12 09:47:48,275-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetComponentDAO
2026-02-12 09:47:48,289-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetAssetBlobDAO
2026-02-12 09:47:48,306-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetAssetDAO
2026-02-12 09:47:48,319-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetBrowseNodeDAO
2026-02-12 09:47:48,330-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2ContentRepositoryDAO
2026-02-12 09:47:48,345-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2ComponentDAO
2026-02-12 09:47:48,359-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2AssetBlobDAO
2026-02-12 09:47:48,376-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2AssetDAO
2026-02-12 09:47:48,389-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2BrowseNodeDAO
2026-02-12 09:47:48,403-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiContentRepositoryDAO
2026-02-12 09:47:48,420-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiComponentDAO
2026-02-12 09:47:48,435-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiAssetBlobDAO
2026-02-12 09:47:48,452-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiAssetDAO
2026-02-12 09:47:48,465-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiBrowseNodeDAO
2026-02-12 09:47:48,477-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiKeyValueDAO
2026-02-12 09:47:48,588-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RContentRepositoryDAO
2026-02-12 09:47:48,602-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RComponentDAO
2026-02-12 09:47:48,615-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RAssetBlobDAO
2026-02-12 09:47:48,630-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RAssetDAO
2026-02-12 09:47:48,643-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RBrowseNodeDAO
2026-02-12 09:47:48,655-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsContentRepositoryDAO
2026-02-12 09:47:48,670-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsComponentDAO
2026-02-12 09:47:48,685-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsAssetBlobDAO
2026-02-12 09:47:48,703-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsAssetDAO
2026-02-12 09:47:48,716-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsBrowseNodeDAO
2026-02-12 09:47:48,729-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SwiftContentRepositoryDAO
2026-02-12 09:47:48,854-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SwiftComponentDAO
2026-02-12 09:47:49,019-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SwiftAssetBlobDAO
2026-02-12 09:47:49,149-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SwiftAssetDAO
2026-02-12 09:47:49,333-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SwiftBrowseNodeDAO
2026-02-12 09:47:49,519-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TerraformContentRepositoryDAO
2026-02-12 09:47:49,655-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TerraformComponentDAO
2026-02-12 09:47:49,806-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TerraformAssetBlobDAO
2026-02-12 09:47:49,943-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TerraformAssetDAO
2026-02-12 09:47:50,110-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TerraformBrowseNodeDAO
2026-02-12 09:47:50,310-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumContentRepositoryDAO
2026-02-12 09:47:50,324-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumComponentDAO
2026-02-12 09:47:50,337-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumAssetBlobDAO
2026-02-12 09:47:50,352-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumAssetDAO
2026-02-12 09:47:50,364-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumBrowseNodeDAO
2026-02-12 09:47:50,374-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumKeyValueDAO
2026-02-12 09:47:50,384-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptComponentTagDAO
2026-02-12 09:47:50,394-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoComponentTagDAO
2026-02-12 09:47:50,499-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsComponentTagDAO
2026-02-12 09:47:50,509-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComposerComponentTagDAO
2026-02-12 09:47:50,616-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanComponentTagDAO
2026-02-12 09:47:50,627-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaComponentTagDAO
2026-02-12 09:47:50,637-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerComponentTagDAO
2026-02-12 09:47:50,647-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsComponentTagDAO
2026-02-12 09:47:50,656-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoComponentTagDAO
2026-02-12 09:47:50,665-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmComponentTagDAO
2026-02-12 09:47:50,674-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HuggingFaceComponentTagDAO
2026-02-12 09:47:50,791-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2ComponentTagDAO
2026-02-12 09:47:50,802-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmComponentTagDAO
2026-02-12 09:47:50,812-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetComponentTagDAO
2026-02-12 09:47:50,821-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2ComponentTagDAO
2026-02-12 09:47:50,831-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiComponentTagDAO
2026-02-12 09:47:50,841-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RComponentTagDAO
2026-02-12 09:47:50,851-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawComponentTagDAO
2026-02-12 09:47:50,860-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsComponentTagDAO
2026-02-12 09:47:50,869-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TerraformComponentTagDAO
2026-02-12 09:47:50,986-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumComponentTagDAO
2026-02-12 09:47:51,020-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.internal.node.datastore.LocalNodeAccess - ID: CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585
2026-02-12 09:47:51,059-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Restoring 26 BlobStores
2026-02-12 09:47:51,073-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Starting 26 BlobStores
2026-02-12 09:47:51,095-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,097-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,099-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,100-0800 INFO  [ForkJoinPool.commonPool-worker-3]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,101-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,102-0800 INFO  [ForkJoinPool.commonPool-worker-3]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,103-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,103-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,105-0800 INFO  [ForkJoinPool.commonPool-worker-3]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,107-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,107-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,108-0800 INFO  [ForkJoinPool.commonPool-worker-3]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,109-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,111-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,111-0800 INFO  [ForkJoinPool.commonPool-worker-2]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,112-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,112-0800 INFO  [ForkJoinPool.commonPool-worker-3]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,113-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,114-0800 INFO  [ForkJoinPool.commonPool-worker-3]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,116-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,116-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,116-0800 INFO  [ForkJoinPool.commonPool-worker-3]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,119-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,121-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,124-0800 INFO  [ForkJoinPool.commonPool-worker-2]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,124-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,124-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:47:51,138-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start RESTORE
2026-02-12 09:47:51,139-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start UPGRADE
2026-02-12 09:47:53,120-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.upgrades.BrowseNodeMigrationStep_1_38 - Created 22 out of 22 browse_node parent_id indexes
2026-02-12 09:47:53,263-0800 WARN  [jetty-main-1]  *SYSTEM com.sonatype.nexus.ssl.plugin.internal.keystore.KeyStoreManagerImpl - Trusted key-store should have been empty when initialized but was not
2026-02-12 09:47:53,449-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.upgrades.SoftDeletedBlobsByBlobStoreIndexMigrationStep_2_7 - Creating index idx_soft_deleted_blobs_by_source_blob_store_name_record_id
2026-02-12 09:47:53,818-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.upgrades.SoftDeletedBlobsByBlobStoreIndexMigrationStep_2_7 - Index idx_soft_deleted_blobs_by_source_blob_store_name_record_id created successfully in 0.369 seconds.
2026-02-12 09:47:53,883-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.upgrades.CoordinateMigrationStep_2_13 - Scheduling CreateComponentIndexTask to run after upgrade is completed.
2026-02-12 09:47:53,898-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.upgrade.datastore.internal.steps.RemoveLog4JVisualizer_2_15 - Dropping capabilities entries related to log4j visualizer
2026-02-12 09:47:53,902-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.upgrade.datastore.internal.steps.RemoveLog4JVisualizer_2_15 - Dropping the log4j-visualizer table
2026-02-12 09:47:53,939-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Searching for repositories that need a search index update
2026-02-12 09:47:53,946-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking nuget-hosted repository for search index update
2026-02-12 09:47:53,948-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking Adobe repository for search index update
2026-02-12 09:47:53,949-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking EDRSNAPSHOT repository for search index update
2026-02-12 09:47:53,950-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking AnsibleResources repository for search index update
2026-02-12 09:47:53,952-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking m2e repository for search index update
2026-02-12 09:47:53,953-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking WebAPIStaging repository for search index update
2026-02-12 09:47:53,953-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking ECOM repository for search index update
2026-02-12 09:47:53,955-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking FTB_DockerHosted repository for search index update
2026-02-12 09:47:53,955-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking SdsDevelopment repository for search index update
2026-02-12 09:47:53,956-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking JitPack repository for search index update
2026-02-12 09:47:53,959-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking pypi_hosted repository for search index update
2026-02-12 09:47:53,960-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking VRCMod repository for search index update
2026-02-12 09:47:53,961-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking CDS_Dev repository for search index update
2026-02-12 09:47:53,962-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking IVR_THIRD_PARTY repository for search index update
2026-02-12 09:47:53,962-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking CCPIVRAppRepository repository for search index update
2026-02-12 09:47:53,963-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking CDSTestApp repository for search index update
2026-02-12 09:47:53,964-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking EDR2_RELEASE repository for search index update
2026-02-12 09:47:53,964-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking OCP_Dev repository for search index update
2026-02-12 09:47:53,965-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking ocp repository for search index update
2026-02-12 09:47:53,966-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking olm-mirror repository for search index update
2026-02-12 09:47:53,967-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking EDRPLUGINS repository for search index update
2026-02-12 09:47:53,968-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking TST2 repository for search index update
2026-02-12 09:47:53,969-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking WebAPI repository for search index update
2026-02-12 09:47:53,971-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking FTB_npm repository for search index update
2026-02-12 09:47:53,972-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking FTB_DockerProxy repository for search index update
2026-02-12 09:47:53,974-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking cmtools repository for search index update
2026-02-12 09:47:53,976-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking SdsRelease repository for search index update
2026-02-12 09:47:53,976-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking CDS_Certified repository for search index update
2026-02-12 09:47:53,977-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking OCP_Certified repository for search index update
2026-02-12 09:47:53,980-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking FTB_GO repository for search index update
2026-02-12 09:47:53,981-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking olm-ftb repository for search index update
2026-02-12 09:47:53,982-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking ECLIPSE repository for search index update
2026-02-12 09:47:53,983-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking Jenkins repository for search index update
2026-02-12 09:47:53,983-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking FTB_NuGet repository for search index update
2026-02-12 09:47:53,984-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking UIT1 repository for search index update
2026-02-12 09:47:53,985-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking TST1 repository for search index update
2026-02-12 09:47:53,985-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking WebAPIRelease repository for search index update
2026-02-12 09:47:53,986-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking FTB_npm_3rdParty repository for search index update
2026-02-12 09:47:53,986-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking EDRSTAGING repository for search index update
2026-02-12 09:47:53,987-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking SIP_Development repository for search index update
2026-02-12 09:47:53,988-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking EDR3RDPARTY repository for search index update
2026-02-12 09:47:53,989-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking primefaces repository for search index update
2026-02-12 09:47:53,989-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking FTB_NuGet_3rd_Party repository for search index update
2026-02-12 09:47:53,990-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking UIT2 repository for search index update
2026-02-12 09:47:53,993-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking FTB_YUM repository for search index update
2026-02-12 09:47:53,995-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking FTB_RedHatDockerHosted repository for search index update
2026-02-12 09:47:53,995-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking SIP_Quarantine repository for search index update
2026-02-12 09:47:53,996-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking EDRRELEASE repository for search index update
2026-02-12 09:47:53,997-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking maven-releases repository for search index update
2026-02-12 09:47:53,997-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking maven-snapshots repository for search index update
2026-02-12 09:47:53,998-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking maven-central repository for search index update
2026-02-12 09:47:53,998-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking EDRDevPySpark repository for search index update
2026-02-12 09:47:53,999-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking EDRProdPySpark repository for search index update
2026-02-12 09:47:54,000-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking FTB_RedHatDockerProxy repository for search index update
2026-02-12 09:47:54,001-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking nuget.org-proxy repository for search index update
2026-02-12 09:47:54,004-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking EDRDevBatchClient repository for search index update
2026-02-12 09:47:54,004-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking confluent-io repository for search index update
2026-02-12 09:47:54,005-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking EDR-Online-Help repository for search index update
2026-02-12 09:47:54,007-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking pypi_proxy repository for search index update
2026-02-12 09:47:54,007-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking EDR-OpenCaseDoc repository for search index update
2026-02-12 09:47:54,009-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking FTB_RedHatQuay repository for search index update
2026-02-12 09:47:54,009-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking prisma_proxy repository for search index update
2026-02-12 09:47:54,011-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking FTB_HelmHosted repository for search index update
2026-02-12 09:47:54,013-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking Pega-EKL repository for search index update
2026-02-12 09:47:54,015-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking nuget_org_v2 repository for search index update
2026-02-12 09:47:54,016-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking npm_proxy repository for search index update
2026-02-12 09:47:54,016-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking EDRDevMDMHubConfig repository for search index update
2026-02-12 09:47:54,018-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking JBossMaven repository for search index update
2026-02-12 09:47:54,019-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.search.capability.SearchCapabilityStep_2_16 - Marking RedHatMaven repository for search index update
2026-02-12 09:47:54,026-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.ssl.plugin.upgrades.TrustedCertificatesMigrationStep_2_17 - Scheduling TrustedCertificatesMigrationTask.
2026-02-12 09:47:54,037-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.upgrades.ConanCleanupMigrationStep_2_18 - Removing outdated indexes and columns from conan_component.
2026-02-12 09:47:54,054-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.upgrades.ConanCleanupMigrationStep_2_18 - Successfully completed correcting the state of the conan_component table.
2026-02-12 09:47:54,059-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.upgrades.AssetBlobMigrationStep_2_18_1 - AssetBlobMigrationStep_2_18_1 is now a no-op. Index creation is handled by scheduled task.
2026-02-12 09:47:54,063-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.upgrades.AssetBlobMigrationStep_2_18_2 - Scheduling asset blob index creation task
2026-02-12 09:47:59,045-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.content.upgrades.PrivilegeNxRM2UpgradeStep_2_74 - Scheduling PrivilegeNxRM2UpgradeTask.
2026-02-12 09:47:59,057-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.repository.search.sql.store.upgrade.RemoveOrphanedSearchRecordsMigrationStep_2_76 - scheduling cleanup for search orphaned records
2026-02-12 09:47:59,205-0800 ERROR [jetty-main-1]  *SYSTEM org.flywaydb.core.internal.command.DbMigrate - Migration of schema "public" to version "2.77 - SearchTableIndexesMigrationStep_2_77" failed! Changes successfully rolled back.
2026-02-12 09:47:59,217-0800 ERROR [jetty-main-1]  *SYSTEM org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl - Failed transition: NEW -> STARTED
org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:102)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:68)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start_aroundBody0(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport$AjcClosure1.run(StateGuardLifecycleSupport.java:1)
	at org.aspectj.runtime.reflect.JoinPointImpl.proceed(JoinPointImpl.java:164)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.lambda$0(TransitionsAspect.java:57)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:217)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.aroundTransitionsMethod(TransitionsAspect.java:55)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:68)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:150)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:106)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.moveToPhase(NexusServletContextListener.java:120)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:75)
	at org.eclipse.jetty.ee8.nested.ContextHandler.callContextInitialized(ContextHandler.java:786)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.callContextInitialized(ServletContextHandler.java:516)
	at org.eclipse.jetty.ee8.nested.ContextHandler.contextInitialized(ContextHandler.java:735)
	at org.eclipse.jetty.ee8.servlet.ServletHandler.initialize(ServletHandler.java:629)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.startContext(ServletContextHandler.java:311)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startWebapp(WebAppContext.java:1195)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startContext(WebAppContext.java:1165)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStartInContext(ContextHandler.java:626)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1450)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStart(ContextHandler.java:615)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.doStart(ServletContextHandler.java:243)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.doStart(WebAppContext.java:502)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:113)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$doStart$0(ContextHandler.java:757)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1456)
	at org.eclipse.jetty.server.handler.ContextHandler.doStart(ContextHandler.java:757)
	at org.eclipse.jetty.ee8.nested.ContextHandler$CoreContextHandler.doStart(ContextHandler.java:2290)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at io.dropwizard.metrics.jetty12.AbstractInstrumentedHandler.doStart(AbstractInstrumentedHandler.java:149)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.server.Server.start(Server.java:641)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.Server.doStart(Server.java:582)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer$JettyMainThread.run(JettyServer.java:369)
Caused by: org.flywaydb.core.internal.command.DbMigrate$FlywayMigrateException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:388)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$applyMigrations$1(DbMigrate.java:275)
	at org.flywaydb.core.internal.jdbc.TransactionalExecutionTemplate.execute(TransactionalExecutionTemplate.java:55)
	at org.flywaydb.core.internal.command.DbMigrate.applyMigrations(DbMigrate.java:274)
	at org.flywaydb.core.internal.command.DbMigrate.migrateGroup(DbMigrate.java:247)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$migrateAll$0(DbMigrate.java:141)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLAdvisoryLockTemplate.execute(PostgreSQLAdvisoryLockTemplate.java:69)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLConnection.lock(PostgreSQLConnection.java:99)
	at org.flywaydb.core.internal.schemahistory.JdbcTableSchemaHistory.lock(JdbcTableSchemaHistory.java:139)
	at org.flywaydb.core.internal.command.DbMigrate.migrateAll(DbMigrate.java:141)
	at org.flywaydb.core.internal.command.DbMigrate.migrate(DbMigrate.java:98)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:172)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:124)
	at org.flywaydb.core.FlywayExecutor.execute(FlywayExecutor.java:205)
	at org.flywaydb.core.Flyway.migrate(Flyway.java:124)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:98)
	... 46 common frames omitted
Caused by: org.postgresql.util.PSQLException: ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement
	at org.postgresql.core.v3.QueryExecutorImpl.receiveErrorResponse(QueryExecutorImpl.java:2725)
	at org.postgresql.core.v3.QueryExecutorImpl.processResults(QueryExecutorImpl.java:2412)
	at org.postgresql.core.v3.QueryExecutorImpl.execute(QueryExecutorImpl.java:371)
	at org.postgresql.jdbc.PgStatement.executeInternal(PgStatement.java:502)
	at org.postgresql.jdbc.PgStatement.execute(PgStatement.java:419)
	at org.postgresql.jdbc.PgPreparedStatement.executeWithFlags(PgPreparedStatement.java:194)
	at org.postgresql.jdbc.PgPreparedStatement.execute(PgPreparedStatement.java:180)
	at com.zaxxer.hikari.pool.ProxyPreparedStatement.execute(ProxyPreparedStatement.java:44)
	at com.zaxxer.hikari.pool.HikariProxyPreparedStatement.execute(HikariProxyPreparedStatement.java)
	at org.sonatype.nexus.upgrade.datastore.DatabaseMigrationStep.runStatement(DatabaseMigrationStep.java:56)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPgTrgmIndexIfSupported(SearchTableIndexesMigrationStep_2_77.java:226)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPostgreSQLSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:85)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:60)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.migrate(SearchTableIndexesMigrationStep_2_77.java:51)
	at org.sonatype.nexus.upgrade.datastore.internal.NexusJavaMigration.migrate(NexusJavaMigration.java:96)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.executeOnce(JavaMigrationExecutor.java:55)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.lambda$execute$0(JavaMigrationExecutor.java:48)
	at org.flywaydb.core.internal.database.DefaultExecutionStrategy.execute(DefaultExecutionStrategy.java:27)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.execute(JavaMigrationExecutor.java:47)
	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:377)
	... 61 common frames omitted
2026-02-12 09:47:59,221-0800 ERROR [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.internal.NexusServletContextListener - Failed to initialize context
org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:102)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:68)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start_aroundBody0(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport$AjcClosure1.run(StateGuardLifecycleSupport.java:1)
	at org.aspectj.runtime.reflect.JoinPointImpl.proceed(JoinPointImpl.java:164)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.lambda$0(TransitionsAspect.java:57)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:217)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.aroundTransitionsMethod(TransitionsAspect.java:55)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:68)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:150)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:106)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.moveToPhase(NexusServletContextListener.java:120)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:75)
	at org.eclipse.jetty.ee8.nested.ContextHandler.callContextInitialized(ContextHandler.java:786)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.callContextInitialized(ServletContextHandler.java:516)
	at org.eclipse.jetty.ee8.nested.ContextHandler.contextInitialized(ContextHandler.java:735)
	at org.eclipse.jetty.ee8.servlet.ServletHandler.initialize(ServletHandler.java:629)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.startContext(ServletContextHandler.java:311)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startWebapp(WebAppContext.java:1195)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startContext(WebAppContext.java:1165)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStartInContext(ContextHandler.java:626)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1450)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStart(ContextHandler.java:615)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.doStart(ServletContextHandler.java:243)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.doStart(WebAppContext.java:502)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:113)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$doStart$0(ContextHandler.java:757)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1456)
	at org.eclipse.jetty.server.handler.ContextHandler.doStart(ContextHandler.java:757)
	at org.eclipse.jetty.ee8.nested.ContextHandler$CoreContextHandler.doStart(ContextHandler.java:2290)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at io.dropwizard.metrics.jetty12.AbstractInstrumentedHandler.doStart(AbstractInstrumentedHandler.java:149)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.server.Server.start(Server.java:641)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.Server.doStart(Server.java:582)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer$JettyMainThread.run(JettyServer.java:369)
Caused by: org.flywaydb.core.internal.command.DbMigrate$FlywayMigrateException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:388)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$applyMigrations$1(DbMigrate.java:275)
	at org.flywaydb.core.internal.jdbc.TransactionalExecutionTemplate.execute(TransactionalExecutionTemplate.java:55)
	at org.flywaydb.core.internal.command.DbMigrate.applyMigrations(DbMigrate.java:274)
	at org.flywaydb.core.internal.command.DbMigrate.migrateGroup(DbMigrate.java:247)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$migrateAll$0(DbMigrate.java:141)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLAdvisoryLockTemplate.execute(PostgreSQLAdvisoryLockTemplate.java:69)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLConnection.lock(PostgreSQLConnection.java:99)
	at org.flywaydb.core.internal.schemahistory.JdbcTableSchemaHistory.lock(JdbcTableSchemaHistory.java:139)
	at org.flywaydb.core.internal.command.DbMigrate.migrateAll(DbMigrate.java:141)
	at org.flywaydb.core.internal.command.DbMigrate.migrate(DbMigrate.java:98)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:172)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:124)
	at org.flywaydb.core.FlywayExecutor.execute(FlywayExecutor.java:205)
	at org.flywaydb.core.Flyway.migrate(Flyway.java:124)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:98)
	... 46 common frames omitted
Caused by: org.postgresql.util.PSQLException: ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement
	at org.postgresql.core.v3.QueryExecutorImpl.receiveErrorResponse(QueryExecutorImpl.java:2725)
	at org.postgresql.core.v3.QueryExecutorImpl.processResults(QueryExecutorImpl.java:2412)
	at org.postgresql.core.v3.QueryExecutorImpl.execute(QueryExecutorImpl.java:371)
	at org.postgresql.jdbc.PgStatement.executeInternal(PgStatement.java:502)
	at org.postgresql.jdbc.PgStatement.execute(PgStatement.java:419)
	at org.postgresql.jdbc.PgPreparedStatement.executeWithFlags(PgPreparedStatement.java:194)
	at org.postgresql.jdbc.PgPreparedStatement.execute(PgPreparedStatement.java:180)
	at com.zaxxer.hikari.pool.ProxyPreparedStatement.execute(ProxyPreparedStatement.java:44)
	at com.zaxxer.hikari.pool.HikariProxyPreparedStatement.execute(HikariProxyPreparedStatement.java)
	at org.sonatype.nexus.upgrade.datastore.DatabaseMigrationStep.runStatement(DatabaseMigrationStep.java:56)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPgTrgmIndexIfSupported(SearchTableIndexesMigrationStep_2_77.java:226)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPostgreSQLSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:85)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:60)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.migrate(SearchTableIndexesMigrationStep_2_77.java:51)
	at org.sonatype.nexus.upgrade.datastore.internal.NexusJavaMigration.migrate(NexusJavaMigration.java:96)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.executeOnce(JavaMigrationExecutor.java:55)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.lambda$execute$0(JavaMigrationExecutor.java:48)
	at org.flywaydb.core.internal.database.DefaultExecutionStrategy.execute(DefaultExecutionStrategy.java:27)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.execute(JavaMigrationExecutor.java:47)
	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:377)
	... 61 common frames omitted
2026-02-12 09:47:59,222-0800 WARN  [jetty-main-1]  *SYSTEM org.eclipse.jetty.ee8.webapp.WebAppContext - Failed startup of context oeje8w.WebAppContext@fb504f4{Sonatype Nexus,/,null,false}
java.lang.RuntimeException: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:79)
	at org.eclipse.jetty.ee8.nested.ContextHandler.callContextInitialized(ContextHandler.java:786)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.callContextInitialized(ServletContextHandler.java:516)
	at org.eclipse.jetty.ee8.nested.ContextHandler.contextInitialized(ContextHandler.java:735)
	at org.eclipse.jetty.ee8.servlet.ServletHandler.initialize(ServletHandler.java:629)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.startContext(ServletContextHandler.java:311)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startWebapp(WebAppContext.java:1195)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startContext(WebAppContext.java:1165)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStartInContext(ContextHandler.java:626)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1450)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStart(ContextHandler.java:615)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.doStart(ServletContextHandler.java:243)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.doStart(WebAppContext.java:502)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:113)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$doStart$0(ContextHandler.java:757)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1456)
	at org.eclipse.jetty.server.handler.ContextHandler.doStart(ContextHandler.java:757)
	at org.eclipse.jetty.ee8.nested.ContextHandler$CoreContextHandler.doStart(ContextHandler.java:2290)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at io.dropwizard.metrics.jetty12.AbstractInstrumentedHandler.doStart(AbstractInstrumentedHandler.java:149)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.server.Server.start(Server.java:641)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.Server.doStart(Server.java:582)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer$JettyMainThread.run(JettyServer.java:369)
Caused by: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:102)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:68)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start_aroundBody0(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport$AjcClosure1.run(StateGuardLifecycleSupport.java:1)
	at org.aspectj.runtime.reflect.JoinPointImpl.proceed(JoinPointImpl.java:164)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.lambda$0(TransitionsAspect.java:57)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:217)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.aroundTransitionsMethod(TransitionsAspect.java:55)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:68)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:150)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:106)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.moveToPhase(NexusServletContextListener.java:120)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:75)
	... 33 common frames omitted
Caused by: org.flywaydb.core.internal.command.DbMigrate$FlywayMigrateException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:388)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$applyMigrations$1(DbMigrate.java:275)
	at org.flywaydb.core.internal.jdbc.TransactionalExecutionTemplate.execute(TransactionalExecutionTemplate.java:55)
	at org.flywaydb.core.internal.command.DbMigrate.applyMigrations(DbMigrate.java:274)
	at org.flywaydb.core.internal.command.DbMigrate.migrateGroup(DbMigrate.java:247)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$migrateAll$0(DbMigrate.java:141)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLAdvisoryLockTemplate.execute(PostgreSQLAdvisoryLockTemplate.java:69)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLConnection.lock(PostgreSQLConnection.java:99)
	at org.flywaydb.core.internal.schemahistory.JdbcTableSchemaHistory.lock(JdbcTableSchemaHistory.java:139)
	at org.flywaydb.core.internal.command.DbMigrate.migrateAll(DbMigrate.java:141)
	at org.flywaydb.core.internal.command.DbMigrate.migrate(DbMigrate.java:98)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:172)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:124)
	at org.flywaydb.core.FlywayExecutor.execute(FlywayExecutor.java:205)
	at org.flywaydb.core.Flyway.migrate(Flyway.java:124)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:98)
	... 46 common frames omitted
Caused by: org.postgresql.util.PSQLException: ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement
	at org.postgresql.core.v3.QueryExecutorImpl.receiveErrorResponse(QueryExecutorImpl.java:2725)
	at org.postgresql.core.v3.QueryExecutorImpl.processResults(QueryExecutorImpl.java:2412)
	at org.postgresql.core.v3.QueryExecutorImpl.execute(QueryExecutorImpl.java:371)
	at org.postgresql.jdbc.PgStatement.executeInternal(PgStatement.java:502)
	at org.postgresql.jdbc.PgStatement.execute(PgStatement.java:419)
	at org.postgresql.jdbc.PgPreparedStatement.executeWithFlags(PgPreparedStatement.java:194)
	at org.postgresql.jdbc.PgPreparedStatement.execute(PgPreparedStatement.java:180)
	at com.zaxxer.hikari.pool.ProxyPreparedStatement.execute(ProxyPreparedStatement.java:44)
	at com.zaxxer.hikari.pool.HikariProxyPreparedStatement.execute(HikariProxyPreparedStatement.java)
	at org.sonatype.nexus.upgrade.datastore.DatabaseMigrationStep.runStatement(DatabaseMigrationStep.java:56)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPgTrgmIndexIfSupported(SearchTableIndexesMigrationStep_2_77.java:226)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPostgreSQLSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:85)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:60)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.migrate(SearchTableIndexesMigrationStep_2_77.java:51)
	at org.sonatype.nexus.upgrade.datastore.internal.NexusJavaMigration.migrate(NexusJavaMigration.java:96)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.executeOnce(JavaMigrationExecutor.java:55)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.lambda$execute$0(JavaMigrationExecutor.java:48)
	at org.flywaydb.core.internal.database.DefaultExecutionStrategy.execute(DefaultExecutionStrategy.java:27)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.execute(JavaMigrationExecutor.java:47)
	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:377)
	... 61 common frames omitted
2026-02-12 09:47:59,225-0800 ERROR [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Failed to start
java.lang.RuntimeException: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:79)
	at org.eclipse.jetty.ee8.nested.ContextHandler.callContextInitialized(ContextHandler.java:786)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.callContextInitialized(ServletContextHandler.java:516)
	at org.eclipse.jetty.ee8.nested.ContextHandler.contextInitialized(ContextHandler.java:735)
	at org.eclipse.jetty.ee8.servlet.ServletHandler.initialize(ServletHandler.java:629)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.startContext(ServletContextHandler.java:311)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startWebapp(WebAppContext.java:1195)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startContext(WebAppContext.java:1165)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStartInContext(ContextHandler.java:626)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1450)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStart(ContextHandler.java:615)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.doStart(ServletContextHandler.java:243)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.doStart(WebAppContext.java:502)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:113)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$doStart$0(ContextHandler.java:757)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1456)
	at org.eclipse.jetty.server.handler.ContextHandler.doStart(ContextHandler.java:757)
	at org.eclipse.jetty.ee8.nested.ContextHandler$CoreContextHandler.doStart(ContextHandler.java:2290)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at io.dropwizard.metrics.jetty12.AbstractInstrumentedHandler.doStart(AbstractInstrumentedHandler.java:149)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.server.Server.start(Server.java:641)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.Server.doStart(Server.java:582)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer$JettyMainThread.run(JettyServer.java:369)
Caused by: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:102)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:68)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start_aroundBody0(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport$AjcClosure1.run(StateGuardLifecycleSupport.java:1)
	at org.aspectj.runtime.reflect.JoinPointImpl.proceed(JoinPointImpl.java:164)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.lambda$0(TransitionsAspect.java:57)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:217)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.aroundTransitionsMethod(TransitionsAspect.java:55)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:68)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:150)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:106)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.moveToPhase(NexusServletContextListener.java:120)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:75)
	... 33 common frames omitted
Caused by: org.flywaydb.core.internal.command.DbMigrate$FlywayMigrateException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:388)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$applyMigrations$1(DbMigrate.java:275)
	at org.flywaydb.core.internal.jdbc.TransactionalExecutionTemplate.execute(TransactionalExecutionTemplate.java:55)
	at org.flywaydb.core.internal.command.DbMigrate.applyMigrations(DbMigrate.java:274)
	at org.flywaydb.core.internal.command.DbMigrate.migrateGroup(DbMigrate.java:247)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$migrateAll$0(DbMigrate.java:141)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLAdvisoryLockTemplate.execute(PostgreSQLAdvisoryLockTemplate.java:69)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLConnection.lock(PostgreSQLConnection.java:99)
	at org.flywaydb.core.internal.schemahistory.JdbcTableSchemaHistory.lock(JdbcTableSchemaHistory.java:139)
	at org.flywaydb.core.internal.command.DbMigrate.migrateAll(DbMigrate.java:141)
	at org.flywaydb.core.internal.command.DbMigrate.migrate(DbMigrate.java:98)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:172)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:124)
	at org.flywaydb.core.FlywayExecutor.execute(FlywayExecutor.java:205)
	at org.flywaydb.core.Flyway.migrate(Flyway.java:124)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:98)
	... 46 common frames omitted
Caused by: org.postgresql.util.PSQLException: ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement
	at org.postgresql.core.v3.QueryExecutorImpl.receiveErrorResponse(QueryExecutorImpl.java:2725)
	at org.postgresql.core.v3.QueryExecutorImpl.processResults(QueryExecutorImpl.java:2412)
	at org.postgresql.core.v3.QueryExecutorImpl.execute(QueryExecutorImpl.java:371)
	at org.postgresql.jdbc.PgStatement.executeInternal(PgStatement.java:502)
	at org.postgresql.jdbc.PgStatement.execute(PgStatement.java:419)
	at org.postgresql.jdbc.PgPreparedStatement.executeWithFlags(PgPreparedStatement.java:194)
	at org.postgresql.jdbc.PgPreparedStatement.execute(PgPreparedStatement.java:180)
	at com.zaxxer.hikari.pool.ProxyPreparedStatement.execute(ProxyPreparedStatement.java:44)
	at com.zaxxer.hikari.pool.HikariProxyPreparedStatement.execute(HikariProxyPreparedStatement.java)
	at org.sonatype.nexus.upgrade.datastore.DatabaseMigrationStep.runStatement(DatabaseMigrationStep.java:56)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPgTrgmIndexIfSupported(SearchTableIndexesMigrationStep_2_77.java:226)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPostgreSQLSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:85)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:60)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.migrate(SearchTableIndexesMigrationStep_2_77.java:51)
	at org.sonatype.nexus.upgrade.datastore.internal.NexusJavaMigration.migrate(NexusJavaMigration.java:96)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.executeOnce(JavaMigrationExecutor.java:55)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.lambda$execute$0(JavaMigrationExecutor.java:48)
	at org.flywaydb.core.internal.database.DefaultExecutionStrategy.execute(DefaultExecutionStrategy.java:27)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.execute(JavaMigrationExecutor.java:47)
	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:377)
	... 61 common frames omitted
2026-02-12 09:47:59,226-0800 ERROR [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Start failed
java.lang.RuntimeException: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:79)
	at org.eclipse.jetty.ee8.nested.ContextHandler.callContextInitialized(ContextHandler.java:786)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.callContextInitialized(ServletContextHandler.java:516)
	at org.eclipse.jetty.ee8.nested.ContextHandler.contextInitialized(ContextHandler.java:735)
	at org.eclipse.jetty.ee8.servlet.ServletHandler.initialize(ServletHandler.java:629)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.startContext(ServletContextHandler.java:311)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startWebapp(WebAppContext.java:1195)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startContext(WebAppContext.java:1165)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStartInContext(ContextHandler.java:626)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1450)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStart(ContextHandler.java:615)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.doStart(ServletContextHandler.java:243)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.doStart(WebAppContext.java:502)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:113)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$doStart$0(ContextHandler.java:757)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1456)
	at org.eclipse.jetty.server.handler.ContextHandler.doStart(ContextHandler.java:757)
	at org.eclipse.jetty.ee8.nested.ContextHandler$CoreContextHandler.doStart(ContextHandler.java:2290)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at io.dropwizard.metrics.jetty12.AbstractInstrumentedHandler.doStart(AbstractInstrumentedHandler.java:149)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.server.Server.start(Server.java:641)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.Server.doStart(Server.java:582)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer$JettyMainThread.run(JettyServer.java:369)
Caused by: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:102)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:68)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start_aroundBody0(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport$AjcClosure1.run(StateGuardLifecycleSupport.java:1)
	at org.aspectj.runtime.reflect.JoinPointImpl.proceed(JoinPointImpl.java:164)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.lambda$0(TransitionsAspect.java:57)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:217)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.aroundTransitionsMethod(TransitionsAspect.java:55)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:68)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:150)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:106)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.moveToPhase(NexusServletContextListener.java:120)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:75)
	... 33 common frames omitted
Caused by: org.flywaydb.core.internal.command.DbMigrate$FlywayMigrateException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:388)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$applyMigrations$1(DbMigrate.java:275)
	at org.flywaydb.core.internal.jdbc.TransactionalExecutionTemplate.execute(TransactionalExecutionTemplate.java:55)
	at org.flywaydb.core.internal.command.DbMigrate.applyMigrations(DbMigrate.java:274)
	at org.flywaydb.core.internal.command.DbMigrate.migrateGroup(DbMigrate.java:247)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$migrateAll$0(DbMigrate.java:141)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLAdvisoryLockTemplate.execute(PostgreSQLAdvisoryLockTemplate.java:69)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLConnection.lock(PostgreSQLConnection.java:99)
	at org.flywaydb.core.internal.schemahistory.JdbcTableSchemaHistory.lock(JdbcTableSchemaHistory.java:139)
	at org.flywaydb.core.internal.command.DbMigrate.migrateAll(DbMigrate.java:141)
	at org.flywaydb.core.internal.command.DbMigrate.migrate(DbMigrate.java:98)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:172)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:124)
	at org.flywaydb.core.FlywayExecutor.execute(FlywayExecutor.java:205)
	at org.flywaydb.core.Flyway.migrate(Flyway.java:124)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:98)
	... 46 common frames omitted
Caused by: org.postgresql.util.PSQLException: ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement
	at org.postgresql.core.v3.QueryExecutorImpl.receiveErrorResponse(QueryExecutorImpl.java:2725)
	at org.postgresql.core.v3.QueryExecutorImpl.processResults(QueryExecutorImpl.java:2412)
	at org.postgresql.core.v3.QueryExecutorImpl.execute(QueryExecutorImpl.java:371)
	at org.postgresql.jdbc.PgStatement.executeInternal(PgStatement.java:502)
	at org.postgresql.jdbc.PgStatement.execute(PgStatement.java:419)
	at org.postgresql.jdbc.PgPreparedStatement.executeWithFlags(PgPreparedStatement.java:194)
	at org.postgresql.jdbc.PgPreparedStatement.execute(PgPreparedStatement.java:180)
	at com.zaxxer.hikari.pool.ProxyPreparedStatement.execute(ProxyPreparedStatement.java:44)
	at com.zaxxer.hikari.pool.HikariProxyPreparedStatement.execute(HikariProxyPreparedStatement.java)
	at org.sonatype.nexus.upgrade.datastore.DatabaseMigrationStep.runStatement(DatabaseMigrationStep.java:56)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPgTrgmIndexIfSupported(SearchTableIndexesMigrationStep_2_77.java:226)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPostgreSQLSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:85)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:60)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.migrate(SearchTableIndexesMigrationStep_2_77.java:51)
	at org.sonatype.nexus.upgrade.datastore.internal.NexusJavaMigration.migrate(NexusJavaMigration.java:96)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.executeOnce(JavaMigrationExecutor.java:55)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.lambda$execute$0(JavaMigrationExecutor.java:48)
	at org.flywaydb.core.internal.database.DefaultExecutionStrategy.execute(DefaultExecutionStrategy.java:27)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.execute(JavaMigrationExecutor.java:47)
	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:377)
	... 61 common frames omitted
2026-02-12 09:47:59,229-0800 WARN  [main]  *SYSTEM org.springframework.context.annotation.AnnotationConfigApplicationContext - Exception encountered during context initialization - cancelling refresh attempt: org.springframework.context.ApplicationContextException: Failed to start bean 'org.sonatype.nexus.bootstrap.jetty.ManagedJetty'
2026-02-12 09:47:59,230-0800 WARN  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.util.component.ContainerLifeCycle - Unable to destroy
java.lang.IllegalStateException: !STOPPED
	at org.eclipse.jetty.ee8.nested.HandlerWrapper.destroy(HandlerWrapper.java:119)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.destroy(WebAppContext.java:548)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.destroy(ContainerLifeCycle.java:228)
	at org.eclipse.jetty.server.Handler$Abstract.destroy(Handler.java:507)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$destroy$2(ContextHandler.java:1018)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.run(ContextHandler.java:1517)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.run(ContextHandler.java:1504)
	at org.eclipse.jetty.server.handler.ContextHandler.destroy(ContextHandler.java:1018)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.destroy(ContainerLifeCycle.java:228)
	at org.eclipse.jetty.server.Handler$Abstract.destroy(Handler.java:507)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.destroy(ContainerLifeCycle.java:228)
	at org.eclipse.jetty.server.Handler$Abstract.destroy(Handler.java:507)
	at org.eclipse.jetty.util.thread.ShutdownThread.run(ShutdownThread.java:142)
2026-02-12 09:47:59,316-0800 WARN  [main]  *SYSTEM org.springframework.context.annotation.AnnotationConfigApplicationContext - Exception encountered during context initialization - cancelling refresh attempt: java.lang.RuntimeException: Failed to configure application
2026-02-12 09:47:59,317-0800 ERROR [main]  *SYSTEM org.springframework.boot.SpringApplication - Application run failed
java.lang.RuntimeException: Failed to configure application
	at org.sonatype.nexus.bootstrap.entrypoint.ApplicationLauncher.onContextRefreshed(ApplicationLauncher.java:112)
	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:103)
	at java.base/java.lang.reflect.Method.invoke(Method.java:580)
	at org.springframework.context.event.ApplicationListenerMethodAdapter.doInvoke(ApplicationListenerMethodAdapter.java:383)
	at org.springframework.context.event.ApplicationListenerMethodAdapter.processEvent(ApplicationListenerMethodAdapter.java:255)
	at org.springframework.context.event.ApplicationListenerMethodAdapter.onApplicationEvent(ApplicationListenerMethodAdapter.java:174)
	at org.springframework.context.event.SimpleApplicationEventMulticaster.doInvokeListener(SimpleApplicationEventMulticaster.java:185)
	at org.springframework.context.event.SimpleApplicationEventMulticaster.invokeListener(SimpleApplicationEventMulticaster.java:178)
	at org.springframework.context.event.SimpleApplicationEventMulticaster.multicastEvent(SimpleApplicationEventMulticaster.java:156)
	at org.springframework.context.support.AbstractApplicationContext.publishEvent(AbstractApplicationContext.java:454)
	at org.springframework.context.support.AbstractApplicationContext.publishEvent(AbstractApplicationContext.java:387)
	at org.springframework.context.support.AbstractApplicationContext.finishRefresh(AbstractApplicationContext.java:1009)
	at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:630)
	at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:755)
	at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:456)
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:335)
	at org.springframework.boot.builder.SpringApplicationBuilder.run(SpringApplicationBuilder.java:149)
	at com.sonatype.nexus.bootstrap.entrypoint.pro.SonatypeNexusRepositoryApplication.main(SonatypeNexusRepositoryApplication.java:44)
	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:103)
	at java.base/java.lang.reflect.Method.invoke(Method.java:580)
	at org.springframework.boot.loader.launch.Launcher.launch(Launcher.java:102)
	at org.springframework.boot.loader.launch.Launcher.launch(Launcher.java:64)
	at org.springframework.boot.loader.launch.JarLauncher.main(JarLauncher.java:40)
Caused by: org.springframework.context.ApplicationContextException: Failed to start bean 'org.sonatype.nexus.bootstrap.jetty.ManagedJetty'
	at org.springframework.context.support.DefaultLifecycleProcessor.doStart(DefaultLifecycleProcessor.java:408)
	at org.springframework.context.support.DefaultLifecycleProcessor.doStart(DefaultLifecycleProcessor.java:394)
	at org.springframework.context.support.DefaultLifecycleProcessor$LifecycleGroup.start(DefaultLifecycleProcessor.java:586)
	at java.base/java.lang.Iterable.forEach(Iterable.java:75)
	at org.springframework.context.support.DefaultLifecycleProcessor.startBeans(DefaultLifecycleProcessor.java:364)
	at org.springframework.context.support.DefaultLifecycleProcessor.onRefresh(DefaultLifecycleProcessor.java:310)
	at org.springframework.context.support.AbstractApplicationContext.finishRefresh(AbstractApplicationContext.java:1006)
	at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:630)
	at org.sonatype.nexus.bootstrap.entrypoint.SpringComponentScan.finishBootstrapComponentScanning(SpringComponentScan.java:87)
	at org.sonatype.nexus.bootstrap.entrypoint.ApplicationLauncher.onContextRefreshed(ApplicationLauncher.java:109)
	... 22 common frames omitted
Caused by: java.lang.RuntimeException: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:79)
	at org.eclipse.jetty.ee8.nested.ContextHandler.callContextInitialized(ContextHandler.java:786)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.callContextInitialized(ServletContextHandler.java:516)
	at org.eclipse.jetty.ee8.nested.ContextHandler.contextInitialized(ContextHandler.java:735)
	at org.eclipse.jetty.ee8.servlet.ServletHandler.initialize(ServletHandler.java:629)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.startContext(ServletContextHandler.java:311)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startWebapp(WebAppContext.java:1195)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startContext(WebAppContext.java:1165)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStartInContext(ContextHandler.java:626)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1450)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStart(ContextHandler.java:615)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.doStart(ServletContextHandler.java:243)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.doStart(WebAppContext.java:502)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:113)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$doStart$0(ContextHandler.java:757)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1456)
	at org.eclipse.jetty.server.handler.ContextHandler.doStart(ContextHandler.java:757)
	at org.eclipse.jetty.ee8.nested.ContextHandler$CoreContextHandler.doStart(ContextHandler.java:2290)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at io.dropwizard.metrics.jetty12.AbstractInstrumentedHandler.doStart(AbstractInstrumentedHandler.java:149)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.server.Server.start(Server.java:641)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.Server.doStart(Server.java:582)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer$JettyMainThread.run(JettyServer.java:369)
Caused by: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:102)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:68)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start_aroundBody0(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport$AjcClosure1.run(StateGuardLifecycleSupport.java:1)
	at org.aspectj.runtime.reflect.JoinPointImpl.proceed(JoinPointImpl.java:164)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.lambda$0(TransitionsAspect.java:57)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:217)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.aroundTransitionsMethod(TransitionsAspect.java:55)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:68)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:150)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:106)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.moveToPhase(NexusServletContextListener.java:120)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:75)
	... 33 common frames omitted
Caused by: org.flywaydb.core.internal.command.DbMigrate$FlywayMigrateException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:388)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$applyMigrations$1(DbMigrate.java:275)
	at org.flywaydb.core.internal.jdbc.TransactionalExecutionTemplate.execute(TransactionalExecutionTemplate.java:55)
	at org.flywaydb.core.internal.command.DbMigrate.applyMigrations(DbMigrate.java:274)
	at org.flywaydb.core.internal.command.DbMigrate.migrateGroup(DbMigrate.java:247)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$migrateAll$0(DbMigrate.java:141)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLAdvisoryLockTemplate.execute(PostgreSQLAdvisoryLockTemplate.java:69)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLConnection.lock(PostgreSQLConnection.java:99)
	at org.flywaydb.core.internal.schemahistory.JdbcTableSchemaHistory.lock(JdbcTableSchemaHistory.java:139)
	at org.flywaydb.core.internal.command.DbMigrate.migrateAll(DbMigrate.java:141)
	at org.flywaydb.core.internal.command.DbMigrate.migrate(DbMigrate.java:98)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:172)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:124)
	at org.flywaydb.core.FlywayExecutor.execute(FlywayExecutor.java:205)
	at org.flywaydb.core.Flyway.migrate(Flyway.java:124)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:98)
	... 46 common frames omitted
Caused by: org.postgresql.util.PSQLException: ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement
	at org.postgresql.core.v3.QueryExecutorImpl.receiveErrorResponse(QueryExecutorImpl.java:2725)
	at org.postgresql.core.v3.QueryExecutorImpl.processResults(QueryExecutorImpl.java:2412)
	at org.postgresql.core.v3.QueryExecutorImpl.execute(QueryExecutorImpl.java:371)
	at org.postgresql.jdbc.PgStatement.executeInternal(PgStatement.java:502)
	at org.postgresql.jdbc.PgStatement.execute(PgStatement.java:419)
	at org.postgresql.jdbc.PgPreparedStatement.executeWithFlags(PgPreparedStatement.java:194)
	at org.postgresql.jdbc.PgPreparedStatement.execute(PgPreparedStatement.java:180)
	at com.zaxxer.hikari.pool.ProxyPreparedStatement.execute(ProxyPreparedStatement.java:44)
	at com.zaxxer.hikari.pool.HikariProxyPreparedStatement.execute(HikariProxyPreparedStatement.java)
	at org.sonatype.nexus.upgrade.datastore.DatabaseMigrationStep.runStatement(DatabaseMigrationStep.java:56)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPgTrgmIndexIfSupported(SearchTableIndexesMigrationStep_2_77.java:226)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPostgreSQLSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:85)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:60)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.migrate(SearchTableIndexesMigrationStep_2_77.java:51)
	at org.sonatype.nexus.upgrade.datastore.internal.NexusJavaMigration.migrate(NexusJavaMigration.java:96)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.executeOnce(JavaMigrationExecutor.java:55)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.lambda$execute$0(JavaMigrationExecutor.java:48)
	at org.flywaydb.core.internal.database.DefaultExecutionStrategy.execute(DefaultExecutionStrategy.java:27)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.execute(JavaMigrationExecutor.java:47)
	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:377)
	... 61 common frames omitted
2026-02-12 09:48:54,996-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.configuration.NexusProperties - nexus.properties: {ssl.etc=/opt/appdata/nexus/sonatype-work/nexus3/etc/ssl, nexus-edition=nexus-pro-edition, java.specification.version=21, nexus-db-feature=nexus-datastore-mybatis, javax.net.ssl.trustStorePassword=edrcmadm, sun.jnu.encoding=UTF-8, nexus.view.exhaustForAgents=Apache-Maven.*|libwww-perl.*, sun.arch.data.model=64, java.vendor.url=https://adoptium.net/, nexus.session.enabled=true, nexus.scripts.allowCreation=true, sun.boot.library.path=/opt/appdata/nexus/nexus-3.89.0-09/jdk/temurin_21.0.9_10_linux_x86_64/jdk-21.0.9+10/lib, sun.java.command=/opt/appdata/nexus/nexus-3.89.0-09/bin/sonatype-nexus-repository-3.89.0-09.jar, logging.register-shutdown-hook=false, jdk.debug=release, java.specification.vendor=Oracle Corporation, java.version.date=2025-10-21, java.home=/opt/appdata/nexus/nexus-3.89.0-09/jdk/temurin_21.0.9_10_linux_x86_64/jdk-21.0.9+10, logging.config=etc/logback/logback.xml, nexus-features=nexus-pro-feature, file.separator=/, java.vm.compressedOopsMode=Zero based, line.separator=
, nexus.onboarding.enabled=true, java.vm.specification.vendor=Oracle Corporation, java.specification.name=Java Platform API Specification, spring.config.location=etc/default-application.properties, application-host=0.0.0.0, javax.net.ssl.trustStore=/opt/appdata/nexus/sonatype-work/nexus3/etc/ssl/nexusrepo.jks, jdk.tls.ephemeralDHKeySize=2048, nexus-context-path=/, java.util.logging.config.file=etc/spring/java.util.logging.properties, java.protocol.handler.pkgs=org.springframework.boot.loader.net.protocol, sun.management.compiler=HotSpot 64-Bit Tiered Compilers, karaf.home=., java.runtime.version=21.0.9+10-LTS, user.name=nexus, nexus.jwt.enabled=false, file.encoding=UTF-8, java.vendor.version=Temurin-21.0.9+10, java.io.tmpdir=/opt/appdata/nexus/sonatype-work/nexus3/tmp, logback.etc=/opt/appdata/nexus/nexus-3.89.0-09/etc/logback, java.version=21.0.9, fabric.etc=/opt/appdata/nexus/nexus-3.89.0-09/etc/fabric, java.vm.specification.name=Java Virtual Machine Specification, PID=2204049, nexus.change.repo.blobstore.task.enabled=true, CONSOLE_LOG_CHARSET=UTF-8, native.encoding=UTF-8, java.library.path=/usr/java/packages/lib:/usr/lib64:/lib64:/lib:/usr/lib, stderr.encoding=UTF-8, java.vendor=Eclipse Adoptium, karaf.base=/opt/appdata/nexus/nexus-3.89.0-09, sun.io.unicode.encoding=UnicodeLittle, karaf.log=/opt/appdata/nexus/sonatype-work/nexus3/log, java.class.path=/opt/appdata/nexus/nexus-3.89.0-09/bin/sonatype-nexus-repository-3.89.0-09.jar, karaf.etc=/opt/appdata/nexus/nexus-3.89.0-09/etc/karaf, nexus.assetdownloads.enabled=true, java.vm.vendor=Eclipse Adoptium, nexus.installer.type=linux-x86-64, user.timezone=America/Los_Angeles, org.jboss.logging.provider=slf4j, application-port=8081, java.vm.specification.version=21, os.name=Linux, sun.java.launcher=SUN_STANDARD, user.country=US, karaf.data=/opt/appdata/nexus/sonatype-work/nexus3, nexus.zero.downtime.enabled=false, karaf.instances=/opt/appdata/nexus/sonatype-work/nexus3/instances, sun.cpu.endian=little, user.home=/home/nexus, user.language=en, javax.net.ssl.keyStorePassword=edrcmadm, jetty.etc=/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty, FILE_LOG_CHARSET=UTF-8, java.awt.headless=true, nexus.http.denyframe.enabled=true, java.net.preferIPv4Stack=true, nexus.datastore.enabled=true, stdout.encoding=UTF-8, path.separator=:, os.version=4.18.0-553.89.1.el8_10.x86_64, java.runtime.name=OpenJDK Runtime Environment, nexus-args=/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty/jetty.xml,/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty/jetty-https.xml,/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty/jetty-requestlog.xml, nexus.quartz.jobstore.jdbc=true, java.vm.name=OpenJDK 64-Bit Server VM, javax.net.ssl.keyStore=/opt/appdata/nexus/sonatype-work/nexus3/etc/ssl/nexusrepo.jks, java.vendor.url.bug=https://github.com/adoptium/adoptium-support/issues, nexus.security.oauth2.enabled=false, org.sonatype.nexus.repository.httpbridge.internal.HttpBridgeModule.legacy=true, user.dir=/opt/appdata/nexus/nexus-3.89.0-09, os.arch=amd64, java.vm.info=mixed mode, sharing, java.vm.version=21.0.9+10-LTS, application-port-ssl=8444, java.class.version=65.0}
2026-02-12 09:48:55,003-0800 INFO  [main]  *SYSTEM com.sonatype.nexus.bootstrap.entrypoint.pro.SonatypeNexusRepositoryApplication - Starting SonatypeNexusRepositoryApplication v3.89.0-09 using Java 21.0.9 with PID 2204049 (/opt/appdata/nexus/nexus-3.89.0-09/bin/sonatype-nexus-repository-3.89.0-09.jar started by nexus in /opt/appdata/nexus/nexus-3.89.0-09)
2026-02-12 09:48:55,004-0800 INFO  [main]  *SYSTEM com.sonatype.nexus.bootstrap.entrypoint.pro.SonatypeNexusRepositoryApplication - No active profile set, falling back to 1 default profile: "default"
2026-02-12 09:48:57,033-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.ApplicationLauncher - Starting nexus with edition PRO
2026-02-12 09:48:57,375-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.SpringComponentScan - Scanning for components in packages: [org.sonatype.nexus, com.sonatype.nexus]
2026-02-12 09:49:08,424-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.quartz.internal.QuartzSchedulerProvider - Thread-pool size: 20, Thread-pool priority: 5
2026-02-12 09:49:08,781-0800 INFO  [main]  *SYSTEM org.opensaml.core.config.InitializationService - Initializing OpenSAML using the Java Services API
2026-02-12 09:49:11,261-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.log.overrides.file.LogbackLoggerOverrides - File: /opt/appdata/nexus/sonatype-work/nexus3/etc/logback/logback-overrides.xml
2026-02-12 09:49:11,310-0800 INFO  [main]  *SYSTEM org.apache.shiro.nexus.NexusWebSessionManager - Global session timeout: 1800000 ms
2026-02-12 09:49:11,311-0800 INFO  [main]  *SYSTEM org.apache.shiro.nexus.NexusWebSessionManager - Session-cookie prototype: name=NXSESSIONID, secure=true
2026-02-12 09:49:13,048-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle - UI plugin descriptors:
2026-02-12 09:49:13,049-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-rapture
2026-02-12 09:49:13,049-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-coreui-plugin
2026-02-12 09:49:13,049-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle - ExtJS UI plugin descriptors:
2026-02-12 09:49:13,049-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-rapture
2026-02-12 09:49:13,049-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-rutauth-plugin
2026-02-12 09:49:13,049-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-proximanova-plugin
2026-02-12 09:49:13,049-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-coreui-plugin
2026-02-12 09:49:13,049-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-proui-plugin
2026-02-12 09:49:13,049-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-cargo
2026-02-12 09:49:13,049-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-composer
2026-02-12 09:49:13,050-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-onboarding-plugin
2026-02-12 09:49:13,050-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-maven
2026-02-12 09:49:13,050-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-docker
2026-02-12 09:49:13,050-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-rubygems
2026-02-12 09:49:13,050-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-npm
2026-02-12 09:49:13,050-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-nuget
2026-02-12 09:49:13,050-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-repository-pypi
2026-02-12 09:49:13,050-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-saml-plugin
2026-02-12 09:49:13,050-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.rapture.internal.RaptureWebResourceBundle -   nexus-analytics-plugin
2026-02-12 09:49:13,074-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.webresources.WebResourceServlet - Max-age: 30 days (2592000 seconds)
2026-02-12 09:49:13,082-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.wonderland.DownloadServiceImpl - Downloads directory: /opt/appdata/nexus/sonatype-work/nexus3/downloads
2026-02-12 09:49:13,328-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.atlas.SupportZipGeneratorImpl - Maximum included file size: 30 megabytes
2026-02-12 09:49:13,329-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.atlas.SupportZipGeneratorImpl - Maximum ZIP file size: 50 megabytes
2026-02-12 09:49:13,936-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.script.ScriptEngineManagerProvider - Detected 1 engine-factories
2026-02-12 09:49:13,938-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.script.ScriptEngineManagerProvider - Engine-factory: Groovy Scripting Engine v2.0; language=Groovy, version=3.0.19, names=[groovy, Groovy], mime-types=[application/x-groovy], extensions=[groovy]
2026-02-12 09:49:13,938-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.internal.script.ScriptEngineManagerProvider - Default language: groovy
2026-02-12 09:49:14,351-0800 INFO  [main]  *SYSTEM org.hibernate.validator.internal.util.Version - HV000001: Hibernate Validator 6.2.0.Final
2026-02-12 09:49:15,015-0800 INFO  [main]  *SYSTEM com.sonatype.nexus.common.configuration.ConfigurationService - ConfigurationSources ordered: [RoutingRuleConfigurationSource, BlobStoreConfigurationSource, CleanupPolicyConfigurationSource, HttpClientConfigurationSource, PrivilegeConfigurationSource, RoleConfigurationSource, RealmConfigurationSource, AnonymousConfigurationSource, SelectorConfigurationSource, RepositoryConfigurationSource, CapabilityConfigurationSource, TaskConfigurationSource, EmailConfigurationSource, ScriptConfigurationSource, LdapConfigurationSource, FirewallIgnorePatternsConfigurationSource, RepositoryHealthCheckConfigurationSource, NodeHeartbeatConfigurationSource, ChangeRepositoryBlobStoreConfigurationSource, SamlConfigurationSource, SamlUserConfigurationSource, TagConfigurationSource]
2026-02-12 09:49:15,321-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.cache.internal.ehcache.EhCacheManagerProvider - Creating cache-manager with configuration: file:/opt/appdata/nexus/nexus-3.89.0-09/etc/fabric/ehcache.xml
2026-02-12 09:49:15,904-0800 INFO  [main]  *SYSTEM org.ehcache.jsr107.ConfigurationMerger - Configuration of cache MALICIOUS_RISK_ON_DISK_CACHE will be supplemented by template nexus-default
2026-02-12 09:49:15,989-0800 INFO  [main]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'MALICIOUS_RISK_ON_DISK_CACHE' created in EhcacheManager.
2026-02-12 09:49:16,001-0800 INFO  [main]  *SYSTEM org.ehcache.jsr107.Eh107CacheManager - Registering Ehcache MBean javax.cache:type=CacheConfiguration,CacheManager=file./opt/appdata/nexus/nexus-3.89.0-09/etc/fabric/ehcache.xml,Cache=MALICIOUS_RISK_ON_DISK_CACHE
2026-02-12 09:49:16,003-0800 INFO  [main]  *SYSTEM org.ehcache.jsr107.Eh107CacheManager - Registering Ehcache MBean javax.cache:type=CacheStatistics,CacheManager=file./opt/appdata/nexus/nexus-3.89.0-09/etc/fabric/ehcache.xml,Cache=MALICIOUS_RISK_ON_DISK_CACHE
2026-02-12 09:49:16,008-0800 INFO  [main]  *SYSTEM org.ehcache.jsr107.ConfigurationMerger - Configuration of cache ENABLED_REGISTRIES will be supplemented by template nexus-default
2026-02-12 09:49:16,011-0800 INFO  [main]  *SYSTEM org.ehcache.core.EhcacheManager - Cache 'ENABLED_REGISTRIES' created in EhcacheManager.
2026-02-12 09:49:16,012-0800 INFO  [main]  *SYSTEM org.ehcache.jsr107.Eh107CacheManager - Registering Ehcache MBean javax.cache:type=CacheConfiguration,CacheManager=file./opt/appdata/nexus/nexus-3.89.0-09/etc/fabric/ehcache.xml,Cache=ENABLED_REGISTRIES
2026-02-12 09:49:16,012-0800 INFO  [main]  *SYSTEM org.ehcache.jsr107.Eh107CacheManager - Registering Ehcache MBean javax.cache:type=CacheStatistics,CacheManager=file./opt/appdata/nexus/nexus-3.89.0-09/etc/fabric/ehcache.xml,Cache=ENABLED_REGISTRIES
2026-02-12 09:49:16,311-0800 INFO  [main]  *SYSTEM com.sonatype.nexus.repository.swift.internal.provider.SwiftProviderRegistry - Registered 1 Git providers: [github]
2026-02-12 09:49:16,637-0800 INFO  [main]  *SYSTEM org.springframework.beans.factory.annotation.AutowiredAnnotationBeanPostProcessor - Inconsistent constructor declaration on bean with name 'maliciousRiskOnDiskAnalytics': single autowire-marked constructor flagged as optional - this constructor is effectively required since there is no default constructor to fall back to: public com.sonatype.analytics.internal.MaliciousRiskOnDiskAnalytics(com.sonatype.nexus.risk.visualizer.MaliciousRiskService,java.lang.Boolean)
2026-02-12 09:49:16,884-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Starting jetty
2026-02-12 09:49:16,899-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Applying configuration: file:/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty/jetty.xml
2026-02-12 09:49:17,440-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Applying configuration: file:/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty/jetty-https.xml
2026-02-12 09:49:17,517-0800 INFO  [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Applying configuration: file:/opt/appdata/nexus/nexus-3.89.0-09/etc/jetty/jetty-requestlog.xml
2026-02-12 09:49:17,577-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Starting: oejs.Server@65433a3a{STOPPED}[12.0.17,sto=5000]
2026-02-12 09:49:17,584-0800 INFO  [jetty-main-1]  *SYSTEM org.eclipse.jetty.server.Server - jetty-12.0.17; built: 2025-03-03T13:15:05.903Z; git: 14d19c268e4cb09afc312b5255a4cbb7a95c5cb6; jvm 21.0.9+10-LTS
2026-02-12 09:49:17,893-0800 INFO  [jetty-main-1]  *SYSTEM org.eclipse.jetty.session.DefaultSessionIdManager - Session workerName=node0
2026-02-12 09:49:17,920-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.internal.NexusServletContextListener - Running lifecycle phases [KERNEL, STORAGE, RESTORE, UPGRADE, SCHEMAS, EVENTS, SECURITY, SERVICES, REPOSITORIES, CAPABILITIES, TASKS]
2026-02-12 09:49:18,056-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Indexing lifecycle managed components up to phase TASKS
2026-02-12 09:49:18,057-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start KERNEL
2026-02-12 09:49:18,060-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.internal.log.LogbackLogManager - Configuring
2026-02-12 09:49:18,069-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start STORAGE
2026-02-12 09:49:18,081-0800 INFO  [jetty-main-1]  *SYSTEM com.sonatype.nexus.self.hosted.datastore.DataStoreConfigurationFileSource - Loaded 'nexus' data store configuration from properties file (postgresql)
2026-02-12 09:49:18,106-0800 WARN  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - Database directory contains unsupported legacy database files; remove legacy files as soon as possible.
2026-02-12 09:49:18,119-0800 INFO  [jetty-main-1]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Starting...
2026-02-12 09:49:18,268-0800 INFO  [jetty-main-1]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Start completed.
2026-02-12 09:49:18,270-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Loading MyBatis configuration from /opt/appdata/nexus/nexus-3.89.0-09/etc/fabric/mybatis.xml
2026-02-12 09:49:18,370-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - MyBatis databaseId: PostgreSQL
2026-02-12 09:49:18,523-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DeploymentIdDAO
2026-02-12 09:49:18,565-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NodeIdDAO
2026-02-12 09:49:18,586-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AnonymousConfigurationDAO
2026-02-12 09:49:18,612-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CPrivilegeDAO
2026-02-12 09:49:18,628-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CRoleDAO
2026-02-12 09:49:18,644-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CUserRoleMappingDAO
2026-02-12 09:49:18,657-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CUserDAO
2026-02-12 09:49:18,670-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RealmConfigurationDAO
2026-02-12 09:49:18,684-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SecretsDAO
2026-02-12 09:49:18,774-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SoftDeletedBlobsDAO
2026-02-12 09:49:18,788-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CleanupPolicyDAO
2026-02-12 09:49:18,805-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CapabilityStorageItemDAO
2026-02-12 09:49:18,817-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for EmailConfigurationDAO
2026-02-12 09:49:18,831-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HttpClientConfigurationDAO
2026-02-12 09:49:18,848-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ApiKeyDAO
2026-02-12 09:49:18,863-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ApiKeyV2DAO
2026-02-12 09:49:18,877-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SelectorConfigurationDAO
2026-02-12 09:49:18,891-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NexusKeyValueDAO
2026-02-12 09:49:18,903-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for QuartzDAO
2026-02-12 09:49:18,919-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConfigurationDAO
2026-02-12 09:49:18,936-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for BlobStoreConfigurationDAO
2026-02-12 09:49:18,950-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RoutingRuleDAO
2026-02-12 09:49:18,962-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for BlobStoreMetricsDAO
2026-02-12 09:49:18,975-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for UpgradeTaskDAO
2026-02-12 09:49:18,987-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ScriptDAO
2026-02-12 09:49:19,023-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SearchTableDAO
2026-02-12 09:49:19,036-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for LdapConfigurationDAO
2026-02-12 09:49:19,047-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for KeyStoreDAO
2026-02-12 09:49:19,058-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TrustedSSLCertificateDAO
2026-02-12 09:49:19,071-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComponentApplicationScanScheduleDAO
2026-02-12 09:49:19,085-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComponentApplicationScanDAO
2026-02-12 09:49:19,098-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ReconcilePlanDetailsDAO
2026-02-12 09:49:19,113-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ReconcilePlanDAO
2026-02-12 09:49:19,125-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DistributedEventDAO
2026-02-12 09:49:19,136-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CacheDAO
2026-02-12 09:49:19,149-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SupportZipInfoDAO
2026-02-12 09:49:19,158-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DistributedAuthTicketCacheDAO
2026-02-12 09:49:19,168-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for FirewallIgnorePatternsDAO
2026-02-12 09:49:19,179-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RepositoryHealthCheckConfigurationDAO
2026-02-12 09:49:19,190-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for MalwareRemediatorTaskDAO
2026-02-12 09:49:19,202-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RepositoryMetricsDAO
2026-02-12 09:49:19,218-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NodeHeartbeatDAO
2026-02-12 09:49:19,232-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ChangeRepositoryBlobstoreDAO
2026-02-12 09:49:19,244-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SamlAuthenticationRequestDAO
2026-02-12 09:49:19,257-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SamlConfigurationDAO
2026-02-12 09:49:19,269-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SamlUserDAO
2026-02-12 09:49:19,284-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TagDAO
2026-02-12 09:49:19,296-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for UserTokenRecordDAO
2026-02-12 09:49:19,308-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AggregatedMetricsDAO
2026-02-12 09:49:19,320-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for MetricDAO
2026-02-12 09:49:19,338-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SwiftComponentTagDAO
2026-02-12 09:49:19,350-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptContentRepositoryDAO
2026-02-12 09:49:19,366-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptAssetBlobDAO
2026-02-12 09:49:19,397-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptComponentDAO
2026-02-12 09:49:19,422-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptAssetDAO
2026-02-12 09:49:19,437-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptBrowseNodeDAO
2026-02-12 09:49:19,452-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptKeyValueDAO
2026-02-12 09:49:19,464-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2ContentRepositoryDAO
2026-02-12 09:49:19,479-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2AssetBlobDAO
2026-02-12 09:49:19,501-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2ComponentDAO
2026-02-12 09:49:19,522-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2AssetDAO
2026-02-12 09:49:19,537-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2BrowseNodeDAO
2026-02-12 09:49:19,550-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawContentRepositoryDAO
2026-02-12 09:49:19,562-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawAssetBlobDAO
2026-02-12 09:49:19,580-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawComponentDAO
2026-02-12 09:49:19,599-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawAssetDAO
2026-02-12 09:49:19,613-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawBrowseNodeDAO
2026-02-12 09:49:19,625-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoContentRepositoryDAO
2026-02-12 09:49:19,638-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoAssetBlobDAO
2026-02-12 09:49:19,657-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoComponentDAO
2026-02-12 09:49:19,675-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoAssetDAO
2026-02-12 09:49:19,688-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoBrowseNodeDAO
2026-02-12 09:49:19,701-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsContentRepositoryDAO
2026-02-12 09:49:19,715-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsAssetBlobDAO
2026-02-12 09:49:19,734-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsComponentDAO
2026-02-12 09:49:19,755-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsAssetDAO
2026-02-12 09:49:19,768-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsBrowseNodeDAO
2026-02-12 09:49:19,781-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComposerContentRepositoryDAO
2026-02-12 09:49:19,794-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComposerAssetBlobDAO
2026-02-12 09:49:19,813-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComposerComponentDAO
2026-02-12 09:49:19,833-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComposerAssetDAO
2026-02-12 09:49:19,847-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComposerBrowseNodeDAO
2026-02-12 09:49:19,859-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanContentRepositoryDAO
2026-02-12 09:49:19,874-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanAssetBlobDAO
2026-02-12 09:49:19,891-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanComponentDAO
2026-02-12 09:49:19,910-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanAssetDAO
2026-02-12 09:49:19,924-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanBrowseNodeDAO
2026-02-12 09:49:19,936-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaContentRepositoryDAO
2026-02-12 09:49:19,949-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaAssetBlobDAO
2026-02-12 09:49:19,966-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaComponentDAO
2026-02-12 09:49:19,984-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaAssetDAO
2026-02-12 09:49:19,996-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaBrowseNodeDAO
2026-02-12 09:49:20,008-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerContentRepositoryDAO
2026-02-12 09:49:20,020-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerAssetBlobDAO
2026-02-12 09:49:20,037-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerComponentDAO
2026-02-12 09:49:20,054-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerAssetDAO
2026-02-12 09:49:20,068-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerBrowseNodeDAO
2026-02-12 09:49:20,078-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerForeignLayersDAO
2026-02-12 09:49:20,088-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsContentRepositoryDAO
2026-02-12 09:49:20,100-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsAssetBlobDAO
2026-02-12 09:49:20,116-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsComponentDAO
2026-02-12 09:49:20,134-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsAssetDAO
2026-02-12 09:49:20,150-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsBrowseNodeDAO
2026-02-12 09:49:20,160-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoContentRepositoryDAO
2026-02-12 09:49:20,172-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoAssetBlobDAO
2026-02-12 09:49:20,187-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoComponentDAO
2026-02-12 09:49:20,205-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoAssetDAO
2026-02-12 09:49:20,217-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoBrowseNodeDAO
2026-02-12 09:49:20,227-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmContentRepositoryDAO
2026-02-12 09:49:20,240-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmAssetBlobDAO
2026-02-12 09:49:20,256-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmComponentDAO
2026-02-12 09:49:20,274-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmAssetDAO
2026-02-12 09:49:20,287-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmBrowseNodeDAO
2026-02-12 09:49:20,298-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmKeyValueDAO
2026-02-12 09:49:20,310-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HuggingFaceContentRepositoryDAO
2026-02-12 09:49:20,322-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HuggingFaceAssetBlobDAO
2026-02-12 09:49:20,339-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HuggingFaceComponentDAO
2026-02-12 09:49:20,357-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HuggingFaceAssetDAO
2026-02-12 09:49:20,369-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HuggingFaceBrowseNodeDAO
2026-02-12 09:49:20,380-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmContentRepositoryDAO
2026-02-12 09:49:20,393-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmAssetBlobDAO
2026-02-12 09:49:20,409-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmComponentDAO
2026-02-12 09:49:20,427-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmAssetDAO
2026-02-12 09:49:20,440-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmBrowseNodeDAO
2026-02-12 09:49:20,451-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmKeyValueDAO
2026-02-12 09:49:20,461-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetContentRepositoryDAO
2026-02-12 09:49:20,473-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetAssetBlobDAO
2026-02-12 09:49:20,490-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetComponentDAO
2026-02-12 09:49:20,508-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetAssetDAO
2026-02-12 09:49:20,520-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetBrowseNodeDAO
2026-02-12 09:49:20,532-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2ContentRepositoryDAO
2026-02-12 09:49:20,543-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2AssetBlobDAO
2026-02-12 09:49:20,559-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2ComponentDAO
2026-02-12 09:49:20,575-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2AssetDAO
2026-02-12 09:49:20,588-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2BrowseNodeDAO
2026-02-12 09:49:20,598-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiContentRepositoryDAO
2026-02-12 09:49:20,610-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiAssetBlobDAO
2026-02-12 09:49:20,626-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiComponentDAO
2026-02-12 09:49:20,644-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiAssetDAO
2026-02-12 09:49:20,656-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiBrowseNodeDAO
2026-02-12 09:49:20,667-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiKeyValueDAO
2026-02-12 09:49:20,677-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RContentRepositoryDAO
2026-02-12 09:49:20,692-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RAssetBlobDAO
2026-02-12 09:49:20,717-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RComponentDAO
2026-02-12 09:49:20,744-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RAssetDAO
2026-02-12 09:49:20,762-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RBrowseNodeDAO
2026-02-12 09:49:20,775-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsContentRepositoryDAO
2026-02-12 09:49:20,788-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsAssetBlobDAO
2026-02-12 09:49:20,804-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsComponentDAO
2026-02-12 09:49:20,821-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsAssetDAO
2026-02-12 09:49:20,834-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsBrowseNodeDAO
2026-02-12 09:49:20,844-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SwiftContentRepositoryDAO
2026-02-12 09:49:20,857-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SwiftAssetBlobDAO
2026-02-12 09:49:20,875-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SwiftComponentDAO
2026-02-12 09:49:20,893-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SwiftAssetDAO
2026-02-12 09:49:20,905-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SwiftBrowseNodeDAO
2026-02-12 09:49:20,917-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TerraformContentRepositoryDAO
2026-02-12 09:49:20,929-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TerraformAssetBlobDAO
2026-02-12 09:49:20,945-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TerraformComponentDAO
2026-02-12 09:49:20,961-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TerraformAssetDAO
2026-02-12 09:49:20,973-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TerraformBrowseNodeDAO
2026-02-12 09:49:20,983-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumContentRepositoryDAO
2026-02-12 09:49:20,995-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumAssetBlobDAO
2026-02-12 09:49:21,012-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumComponentDAO
2026-02-12 09:49:21,029-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumAssetDAO
2026-02-12 09:49:21,042-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumBrowseNodeDAO
2026-02-12 09:49:21,053-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumKeyValueDAO
2026-02-12 09:49:21,064-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptComponentTagDAO
2026-02-12 09:49:21,075-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoComponentTagDAO
2026-02-12 09:49:21,086-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsComponentTagDAO
2026-02-12 09:49:21,097-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComposerComponentTagDAO
2026-02-12 09:49:21,107-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanComponentTagDAO
2026-02-12 09:49:21,119-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaComponentTagDAO
2026-02-12 09:49:21,132-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerComponentTagDAO
2026-02-12 09:49:21,143-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsComponentTagDAO
2026-02-12 09:49:21,153-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoComponentTagDAO
2026-02-12 09:49:21,162-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmComponentTagDAO
2026-02-12 09:49:21,171-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HuggingFaceComponentTagDAO
2026-02-12 09:49:21,181-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2ComponentTagDAO
2026-02-12 09:49:21,191-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmComponentTagDAO
2026-02-12 09:49:21,201-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetComponentTagDAO
2026-02-12 09:49:21,211-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2ComponentTagDAO
2026-02-12 09:49:21,221-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiComponentTagDAO
2026-02-12 09:49:21,231-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RComponentTagDAO
2026-02-12 09:49:21,241-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawComponentTagDAO
2026-02-12 09:49:21,252-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsComponentTagDAO
2026-02-12 09:49:21,263-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TerraformComponentTagDAO
2026-02-12 09:49:21,273-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumComponentTagDAO
2026-02-12 09:49:21,301-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.internal.node.datastore.LocalNodeAccess - ID: CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585
2026-02-12 09:49:21,334-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Restoring 26 BlobStores
2026-02-12 09:49:21,360-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Starting 26 BlobStores
2026-02-12 09:49:21,380-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,383-0800 INFO  [ForkJoinPool.commonPool-worker-2]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,386-0800 INFO  [ForkJoinPool.commonPool-worker-2]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,387-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,389-0800 INFO  [ForkJoinPool.commonPool-worker-2]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,392-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,392-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,394-0800 INFO  [ForkJoinPool.commonPool-worker-2]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,395-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,397-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,398-0800 INFO  [ForkJoinPool.commonPool-worker-2]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,398-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,399-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,400-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,400-0800 INFO  [ForkJoinPool.commonPool-worker-2]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,401-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,402-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,404-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,405-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,407-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,407-0800 INFO  [ForkJoinPool.commonPool-worker-2]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,408-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,411-0800 INFO  [ForkJoinPool.commonPool-worker-2]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,412-0800 INFO  [ForkJoinPool.commonPool-worker-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,412-0800 INFO  [ForkJoinPool.commonPool-worker-3]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,414-0800 INFO  [ForkJoinPool.commonPool-worker-3]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,414-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.self.hosted.blobstore.BlobStoreManagerImpl - Completed initialization
2026-02-12 09:49:21,422-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start RESTORE
2026-02-12 09:49:21,422-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start UPGRADE
2026-02-12 09:49:21,823-0800 ERROR [jetty-main-1]  *SYSTEM org.flywaydb.core.internal.command.DbMigrate - Migration of schema "public" to version "2.77 - SearchTableIndexesMigrationStep_2_77" failed! Changes successfully rolled back.
2026-02-12 09:49:21,836-0800 ERROR [jetty-main-1]  *SYSTEM org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl - Failed transition: NEW -> STARTED
org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:102)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:68)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start_aroundBody0(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport$AjcClosure1.run(StateGuardLifecycleSupport.java:1)
	at org.aspectj.runtime.reflect.JoinPointImpl.proceed(JoinPointImpl.java:164)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.lambda$0(TransitionsAspect.java:57)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:217)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.aroundTransitionsMethod(TransitionsAspect.java:55)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:68)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:150)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:106)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.moveToPhase(NexusServletContextListener.java:120)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:75)
	at org.eclipse.jetty.ee8.nested.ContextHandler.callContextInitialized(ContextHandler.java:786)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.callContextInitialized(ServletContextHandler.java:516)
	at org.eclipse.jetty.ee8.nested.ContextHandler.contextInitialized(ContextHandler.java:735)
	at org.eclipse.jetty.ee8.servlet.ServletHandler.initialize(ServletHandler.java:629)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.startContext(ServletContextHandler.java:311)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startWebapp(WebAppContext.java:1195)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startContext(WebAppContext.java:1165)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStartInContext(ContextHandler.java:626)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1450)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStart(ContextHandler.java:615)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.doStart(ServletContextHandler.java:243)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.doStart(WebAppContext.java:502)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:113)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$doStart$0(ContextHandler.java:757)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1456)
	at org.eclipse.jetty.server.handler.ContextHandler.doStart(ContextHandler.java:757)
	at org.eclipse.jetty.ee8.nested.ContextHandler$CoreContextHandler.doStart(ContextHandler.java:2290)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at io.dropwizard.metrics.jetty12.AbstractInstrumentedHandler.doStart(AbstractInstrumentedHandler.java:149)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.server.Server.start(Server.java:641)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.Server.doStart(Server.java:582)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer$JettyMainThread.run(JettyServer.java:369)
Caused by: org.flywaydb.core.internal.command.DbMigrate$FlywayMigrateException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:388)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$applyMigrations$1(DbMigrate.java:275)
	at org.flywaydb.core.internal.jdbc.TransactionalExecutionTemplate.execute(TransactionalExecutionTemplate.java:55)
	at org.flywaydb.core.internal.command.DbMigrate.applyMigrations(DbMigrate.java:274)
	at org.flywaydb.core.internal.command.DbMigrate.migrateGroup(DbMigrate.java:247)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$migrateAll$0(DbMigrate.java:141)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLAdvisoryLockTemplate.execute(PostgreSQLAdvisoryLockTemplate.java:69)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLConnection.lock(PostgreSQLConnection.java:99)
	at org.flywaydb.core.internal.schemahistory.JdbcTableSchemaHistory.lock(JdbcTableSchemaHistory.java:139)
	at org.flywaydb.core.internal.command.DbMigrate.migrateAll(DbMigrate.java:141)
	at org.flywaydb.core.internal.command.DbMigrate.migrate(DbMigrate.java:98)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:172)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:124)
	at org.flywaydb.core.FlywayExecutor.execute(FlywayExecutor.java:205)
	at org.flywaydb.core.Flyway.migrate(Flyway.java:124)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:98)
	... 46 common frames omitted
Caused by: org.postgresql.util.PSQLException: ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement
	at org.postgresql.core.v3.QueryExecutorImpl.receiveErrorResponse(QueryExecutorImpl.java:2725)
	at org.postgresql.core.v3.QueryExecutorImpl.processResults(QueryExecutorImpl.java:2412)
	at org.postgresql.core.v3.QueryExecutorImpl.execute(QueryExecutorImpl.java:371)
	at org.postgresql.jdbc.PgStatement.executeInternal(PgStatement.java:502)
	at org.postgresql.jdbc.PgStatement.execute(PgStatement.java:419)
	at org.postgresql.jdbc.PgPreparedStatement.executeWithFlags(PgPreparedStatement.java:194)
	at org.postgresql.jdbc.PgPreparedStatement.execute(PgPreparedStatement.java:180)
	at com.zaxxer.hikari.pool.ProxyPreparedStatement.execute(ProxyPreparedStatement.java:44)
	at com.zaxxer.hikari.pool.HikariProxyPreparedStatement.execute(HikariProxyPreparedStatement.java)
	at org.sonatype.nexus.upgrade.datastore.DatabaseMigrationStep.runStatement(DatabaseMigrationStep.java:56)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPgTrgmIndexIfSupported(SearchTableIndexesMigrationStep_2_77.java:226)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPostgreSQLSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:85)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:60)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.migrate(SearchTableIndexesMigrationStep_2_77.java:51)
	at org.sonatype.nexus.upgrade.datastore.internal.NexusJavaMigration.migrate(NexusJavaMigration.java:96)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.executeOnce(JavaMigrationExecutor.java:55)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.lambda$execute$0(JavaMigrationExecutor.java:48)
	at org.flywaydb.core.internal.database.DefaultExecutionStrategy.execute(DefaultExecutionStrategy.java:27)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.execute(JavaMigrationExecutor.java:47)
	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:377)
	... 61 common frames omitted
2026-02-12 09:49:21,840-0800 ERROR [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.internal.NexusServletContextListener - Failed to initialize context
org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:102)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:68)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start_aroundBody0(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport$AjcClosure1.run(StateGuardLifecycleSupport.java:1)
	at org.aspectj.runtime.reflect.JoinPointImpl.proceed(JoinPointImpl.java:164)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.lambda$0(TransitionsAspect.java:57)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:217)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.aroundTransitionsMethod(TransitionsAspect.java:55)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:68)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:150)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:106)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.moveToPhase(NexusServletContextListener.java:120)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:75)
	at org.eclipse.jetty.ee8.nested.ContextHandler.callContextInitialized(ContextHandler.java:786)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.callContextInitialized(ServletContextHandler.java:516)
	at org.eclipse.jetty.ee8.nested.ContextHandler.contextInitialized(ContextHandler.java:735)
	at org.eclipse.jetty.ee8.servlet.ServletHandler.initialize(ServletHandler.java:629)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.startContext(ServletContextHandler.java:311)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startWebapp(WebAppContext.java:1195)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startContext(WebAppContext.java:1165)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStartInContext(ContextHandler.java:626)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1450)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStart(ContextHandler.java:615)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.doStart(ServletContextHandler.java:243)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.doStart(WebAppContext.java:502)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:113)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$doStart$0(ContextHandler.java:757)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1456)
	at org.eclipse.jetty.server.handler.ContextHandler.doStart(ContextHandler.java:757)
	at org.eclipse.jetty.ee8.nested.ContextHandler$CoreContextHandler.doStart(ContextHandler.java:2290)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at io.dropwizard.metrics.jetty12.AbstractInstrumentedHandler.doStart(AbstractInstrumentedHandler.java:149)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.server.Server.start(Server.java:641)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.Server.doStart(Server.java:582)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer$JettyMainThread.run(JettyServer.java:369)
Caused by: org.flywaydb.core.internal.command.DbMigrate$FlywayMigrateException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:388)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$applyMigrations$1(DbMigrate.java:275)
	at org.flywaydb.core.internal.jdbc.TransactionalExecutionTemplate.execute(TransactionalExecutionTemplate.java:55)
	at org.flywaydb.core.internal.command.DbMigrate.applyMigrations(DbMigrate.java:274)
	at org.flywaydb.core.internal.command.DbMigrate.migrateGroup(DbMigrate.java:247)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$migrateAll$0(DbMigrate.java:141)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLAdvisoryLockTemplate.execute(PostgreSQLAdvisoryLockTemplate.java:69)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLConnection.lock(PostgreSQLConnection.java:99)
	at org.flywaydb.core.internal.schemahistory.JdbcTableSchemaHistory.lock(JdbcTableSchemaHistory.java:139)
	at org.flywaydb.core.internal.command.DbMigrate.migrateAll(DbMigrate.java:141)
	at org.flywaydb.core.internal.command.DbMigrate.migrate(DbMigrate.java:98)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:172)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:124)
	at org.flywaydb.core.FlywayExecutor.execute(FlywayExecutor.java:205)
	at org.flywaydb.core.Flyway.migrate(Flyway.java:124)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:98)
	... 46 common frames omitted
Caused by: org.postgresql.util.PSQLException: ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement
	at org.postgresql.core.v3.QueryExecutorImpl.receiveErrorResponse(QueryExecutorImpl.java:2725)
	at org.postgresql.core.v3.QueryExecutorImpl.processResults(QueryExecutorImpl.java:2412)
	at org.postgresql.core.v3.QueryExecutorImpl.execute(QueryExecutorImpl.java:371)
	at org.postgresql.jdbc.PgStatement.executeInternal(PgStatement.java:502)
	at org.postgresql.jdbc.PgStatement.execute(PgStatement.java:419)
	at org.postgresql.jdbc.PgPreparedStatement.executeWithFlags(PgPreparedStatement.java:194)
	at org.postgresql.jdbc.PgPreparedStatement.execute(PgPreparedStatement.java:180)
	at com.zaxxer.hikari.pool.ProxyPreparedStatement.execute(ProxyPreparedStatement.java:44)
	at com.zaxxer.hikari.pool.HikariProxyPreparedStatement.execute(HikariProxyPreparedStatement.java)
	at org.sonatype.nexus.upgrade.datastore.DatabaseMigrationStep.runStatement(DatabaseMigrationStep.java:56)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPgTrgmIndexIfSupported(SearchTableIndexesMigrationStep_2_77.java:226)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPostgreSQLSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:85)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:60)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.migrate(SearchTableIndexesMigrationStep_2_77.java:51)
	at org.sonatype.nexus.upgrade.datastore.internal.NexusJavaMigration.migrate(NexusJavaMigration.java:96)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.executeOnce(JavaMigrationExecutor.java:55)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.lambda$execute$0(JavaMigrationExecutor.java:48)
	at org.flywaydb.core.internal.database.DefaultExecutionStrategy.execute(DefaultExecutionStrategy.java:27)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.execute(JavaMigrationExecutor.java:47)
	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:377)
	... 61 common frames omitted
2026-02-12 09:49:21,841-0800 WARN  [jetty-main-1]  *SYSTEM org.eclipse.jetty.ee8.webapp.WebAppContext - Failed startup of context oeje8w.WebAppContext@5a2fefcb{Sonatype Nexus,/,null,false}
java.lang.RuntimeException: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:79)
	at org.eclipse.jetty.ee8.nested.ContextHandler.callContextInitialized(ContextHandler.java:786)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.callContextInitialized(ServletContextHandler.java:516)
	at org.eclipse.jetty.ee8.nested.ContextHandler.contextInitialized(ContextHandler.java:735)
	at org.eclipse.jetty.ee8.servlet.ServletHandler.initialize(ServletHandler.java:629)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.startContext(ServletContextHandler.java:311)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startWebapp(WebAppContext.java:1195)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startContext(WebAppContext.java:1165)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStartInContext(ContextHandler.java:626)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1450)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStart(ContextHandler.java:615)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.doStart(ServletContextHandler.java:243)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.doStart(WebAppContext.java:502)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:113)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$doStart$0(ContextHandler.java:757)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1456)
	at org.eclipse.jetty.server.handler.ContextHandler.doStart(ContextHandler.java:757)
	at org.eclipse.jetty.ee8.nested.ContextHandler$CoreContextHandler.doStart(ContextHandler.java:2290)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at io.dropwizard.metrics.jetty12.AbstractInstrumentedHandler.doStart(AbstractInstrumentedHandler.java:149)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.server.Server.start(Server.java:641)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.Server.doStart(Server.java:582)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer$JettyMainThread.run(JettyServer.java:369)
Caused by: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:102)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:68)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start_aroundBody0(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport$AjcClosure1.run(StateGuardLifecycleSupport.java:1)
	at org.aspectj.runtime.reflect.JoinPointImpl.proceed(JoinPointImpl.java:164)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.lambda$0(TransitionsAspect.java:57)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:217)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.aroundTransitionsMethod(TransitionsAspect.java:55)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:68)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:150)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:106)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.moveToPhase(NexusServletContextListener.java:120)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:75)
	... 33 common frames omitted
Caused by: org.flywaydb.core.internal.command.DbMigrate$FlywayMigrateException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:388)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$applyMigrations$1(DbMigrate.java:275)
	at org.flywaydb.core.internal.jdbc.TransactionalExecutionTemplate.execute(TransactionalExecutionTemplate.java:55)
	at org.flywaydb.core.internal.command.DbMigrate.applyMigrations(DbMigrate.java:274)
	at org.flywaydb.core.internal.command.DbMigrate.migrateGroup(DbMigrate.java:247)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$migrateAll$0(DbMigrate.java:141)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLAdvisoryLockTemplate.execute(PostgreSQLAdvisoryLockTemplate.java:69)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLConnection.lock(PostgreSQLConnection.java:99)
	at org.flywaydb.core.internal.schemahistory.JdbcTableSchemaHistory.lock(JdbcTableSchemaHistory.java:139)
	at org.flywaydb.core.internal.command.DbMigrate.migrateAll(DbMigrate.java:141)
	at org.flywaydb.core.internal.command.DbMigrate.migrate(DbMigrate.java:98)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:172)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:124)
	at org.flywaydb.core.FlywayExecutor.execute(FlywayExecutor.java:205)
	at org.flywaydb.core.Flyway.migrate(Flyway.java:124)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:98)
	... 46 common frames omitted
Caused by: org.postgresql.util.PSQLException: ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement
	at org.postgresql.core.v3.QueryExecutorImpl.receiveErrorResponse(QueryExecutorImpl.java:2725)
	at org.postgresql.core.v3.QueryExecutorImpl.processResults(QueryExecutorImpl.java:2412)
	at org.postgresql.core.v3.QueryExecutorImpl.execute(QueryExecutorImpl.java:371)
	at org.postgresql.jdbc.PgStatement.executeInternal(PgStatement.java:502)
	at org.postgresql.jdbc.PgStatement.execute(PgStatement.java:419)
	at org.postgresql.jdbc.PgPreparedStatement.executeWithFlags(PgPreparedStatement.java:194)
	at org.postgresql.jdbc.PgPreparedStatement.execute(PgPreparedStatement.java:180)
	at com.zaxxer.hikari.pool.ProxyPreparedStatement.execute(ProxyPreparedStatement.java:44)
	at com.zaxxer.hikari.pool.HikariProxyPreparedStatement.execute(HikariProxyPreparedStatement.java)
	at org.sonatype.nexus.upgrade.datastore.DatabaseMigrationStep.runStatement(DatabaseMigrationStep.java:56)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPgTrgmIndexIfSupported(SearchTableIndexesMigrationStep_2_77.java:226)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPostgreSQLSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:85)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:60)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.migrate(SearchTableIndexesMigrationStep_2_77.java:51)
	at org.sonatype.nexus.upgrade.datastore.internal.NexusJavaMigration.migrate(NexusJavaMigration.java:96)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.executeOnce(JavaMigrationExecutor.java:55)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.lambda$execute$0(JavaMigrationExecutor.java:48)
	at org.flywaydb.core.internal.database.DefaultExecutionStrategy.execute(DefaultExecutionStrategy.java:27)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.execute(JavaMigrationExecutor.java:47)
	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:377)
	... 61 common frames omitted
2026-02-12 09:49:21,844-0800 ERROR [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Failed to start
java.lang.RuntimeException: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:79)
	at org.eclipse.jetty.ee8.nested.ContextHandler.callContextInitialized(ContextHandler.java:786)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.callContextInitialized(ServletContextHandler.java:516)
	at org.eclipse.jetty.ee8.nested.ContextHandler.contextInitialized(ContextHandler.java:735)
	at org.eclipse.jetty.ee8.servlet.ServletHandler.initialize(ServletHandler.java:629)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.startContext(ServletContextHandler.java:311)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startWebapp(WebAppContext.java:1195)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startContext(WebAppContext.java:1165)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStartInContext(ContextHandler.java:626)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1450)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStart(ContextHandler.java:615)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.doStart(ServletContextHandler.java:243)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.doStart(WebAppContext.java:502)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:113)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$doStart$0(ContextHandler.java:757)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1456)
	at org.eclipse.jetty.server.handler.ContextHandler.doStart(ContextHandler.java:757)
	at org.eclipse.jetty.ee8.nested.ContextHandler$CoreContextHandler.doStart(ContextHandler.java:2290)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at io.dropwizard.metrics.jetty12.AbstractInstrumentedHandler.doStart(AbstractInstrumentedHandler.java:149)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.server.Server.start(Server.java:641)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.Server.doStart(Server.java:582)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer$JettyMainThread.run(JettyServer.java:369)
Caused by: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:102)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:68)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start_aroundBody0(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport$AjcClosure1.run(StateGuardLifecycleSupport.java:1)
	at org.aspectj.runtime.reflect.JoinPointImpl.proceed(JoinPointImpl.java:164)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.lambda$0(TransitionsAspect.java:57)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:217)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.aroundTransitionsMethod(TransitionsAspect.java:55)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:68)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:150)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:106)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.moveToPhase(NexusServletContextListener.java:120)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:75)
	... 33 common frames omitted
Caused by: org.flywaydb.core.internal.command.DbMigrate$FlywayMigrateException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:388)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$applyMigrations$1(DbMigrate.java:275)
	at org.flywaydb.core.internal.jdbc.TransactionalExecutionTemplate.execute(TransactionalExecutionTemplate.java:55)
	at org.flywaydb.core.internal.command.DbMigrate.applyMigrations(DbMigrate.java:274)
	at org.flywaydb.core.internal.command.DbMigrate.migrateGroup(DbMigrate.java:247)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$migrateAll$0(DbMigrate.java:141)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLAdvisoryLockTemplate.execute(PostgreSQLAdvisoryLockTemplate.java:69)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLConnection.lock(PostgreSQLConnection.java:99)
	at org.flywaydb.core.internal.schemahistory.JdbcTableSchemaHistory.lock(JdbcTableSchemaHistory.java:139)
	at org.flywaydb.core.internal.command.DbMigrate.migrateAll(DbMigrate.java:141)
	at org.flywaydb.core.internal.command.DbMigrate.migrate(DbMigrate.java:98)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:172)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:124)
	at org.flywaydb.core.FlywayExecutor.execute(FlywayExecutor.java:205)
	at org.flywaydb.core.Flyway.migrate(Flyway.java:124)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:98)
	... 46 common frames omitted
Caused by: org.postgresql.util.PSQLException: ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement
	at org.postgresql.core.v3.QueryExecutorImpl.receiveErrorResponse(QueryExecutorImpl.java:2725)
	at org.postgresql.core.v3.QueryExecutorImpl.processResults(QueryExecutorImpl.java:2412)
	at org.postgresql.core.v3.QueryExecutorImpl.execute(QueryExecutorImpl.java:371)
	at org.postgresql.jdbc.PgStatement.executeInternal(PgStatement.java:502)
	at org.postgresql.jdbc.PgStatement.execute(PgStatement.java:419)
	at org.postgresql.jdbc.PgPreparedStatement.executeWithFlags(PgPreparedStatement.java:194)
	at org.postgresql.jdbc.PgPreparedStatement.execute(PgPreparedStatement.java:180)
	at com.zaxxer.hikari.pool.ProxyPreparedStatement.execute(ProxyPreparedStatement.java:44)
	at com.zaxxer.hikari.pool.HikariProxyPreparedStatement.execute(HikariProxyPreparedStatement.java)
	at org.sonatype.nexus.upgrade.datastore.DatabaseMigrationStep.runStatement(DatabaseMigrationStep.java:56)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPgTrgmIndexIfSupported(SearchTableIndexesMigrationStep_2_77.java:226)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPostgreSQLSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:85)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:60)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.migrate(SearchTableIndexesMigrationStep_2_77.java:51)
	at org.sonatype.nexus.upgrade.datastore.internal.NexusJavaMigration.migrate(NexusJavaMigration.java:96)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.executeOnce(JavaMigrationExecutor.java:55)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.lambda$execute$0(JavaMigrationExecutor.java:48)
	at org.flywaydb.core.internal.database.DefaultExecutionStrategy.execute(DefaultExecutionStrategy.java:27)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.execute(JavaMigrationExecutor.java:47)
	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:377)
	... 61 common frames omitted
2026-02-12 09:49:21,844-0800 ERROR [main]  *SYSTEM org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer - Start failed
java.lang.RuntimeException: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:79)
	at org.eclipse.jetty.ee8.nested.ContextHandler.callContextInitialized(ContextHandler.java:786)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.callContextInitialized(ServletContextHandler.java:516)
	at org.eclipse.jetty.ee8.nested.ContextHandler.contextInitialized(ContextHandler.java:735)
	at org.eclipse.jetty.ee8.servlet.ServletHandler.initialize(ServletHandler.java:629)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.startContext(ServletContextHandler.java:311)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startWebapp(WebAppContext.java:1195)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startContext(WebAppContext.java:1165)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStartInContext(ContextHandler.java:626)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1450)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStart(ContextHandler.java:615)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.doStart(ServletContextHandler.java:243)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.doStart(WebAppContext.java:502)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:113)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$doStart$0(ContextHandler.java:757)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1456)
	at org.eclipse.jetty.server.handler.ContextHandler.doStart(ContextHandler.java:757)
	at org.eclipse.jetty.ee8.nested.ContextHandler$CoreContextHandler.doStart(ContextHandler.java:2290)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at io.dropwizard.metrics.jetty12.AbstractInstrumentedHandler.doStart(AbstractInstrumentedHandler.java:149)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.server.Server.start(Server.java:641)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.Server.doStart(Server.java:582)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer$JettyMainThread.run(JettyServer.java:369)
Caused by: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:102)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:68)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start_aroundBody0(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport$AjcClosure1.run(StateGuardLifecycleSupport.java:1)
	at org.aspectj.runtime.reflect.JoinPointImpl.proceed(JoinPointImpl.java:164)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.lambda$0(TransitionsAspect.java:57)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:217)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.aroundTransitionsMethod(TransitionsAspect.java:55)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:68)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:150)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:106)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.moveToPhase(NexusServletContextListener.java:120)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:75)
	... 33 common frames omitted
Caused by: org.flywaydb.core.internal.command.DbMigrate$FlywayMigrateException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:388)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$applyMigrations$1(DbMigrate.java:275)
	at org.flywaydb.core.internal.jdbc.TransactionalExecutionTemplate.execute(TransactionalExecutionTemplate.java:55)
	at org.flywaydb.core.internal.command.DbMigrate.applyMigrations(DbMigrate.java:274)
	at org.flywaydb.core.internal.command.DbMigrate.migrateGroup(DbMigrate.java:247)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$migrateAll$0(DbMigrate.java:141)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLAdvisoryLockTemplate.execute(PostgreSQLAdvisoryLockTemplate.java:69)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLConnection.lock(PostgreSQLConnection.java:99)
	at org.flywaydb.core.internal.schemahistory.JdbcTableSchemaHistory.lock(JdbcTableSchemaHistory.java:139)
	at org.flywaydb.core.internal.command.DbMigrate.migrateAll(DbMigrate.java:141)
	at org.flywaydb.core.internal.command.DbMigrate.migrate(DbMigrate.java:98)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:172)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:124)
	at org.flywaydb.core.FlywayExecutor.execute(FlywayExecutor.java:205)
	at org.flywaydb.core.Flyway.migrate(Flyway.java:124)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:98)
	... 46 common frames omitted
Caused by: org.postgresql.util.PSQLException: ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement
	at org.postgresql.core.v3.QueryExecutorImpl.receiveErrorResponse(QueryExecutorImpl.java:2725)
	at org.postgresql.core.v3.QueryExecutorImpl.processResults(QueryExecutorImpl.java:2412)
	at org.postgresql.core.v3.QueryExecutorImpl.execute(QueryExecutorImpl.java:371)
	at org.postgresql.jdbc.PgStatement.executeInternal(PgStatement.java:502)
	at org.postgresql.jdbc.PgStatement.execute(PgStatement.java:419)
	at org.postgresql.jdbc.PgPreparedStatement.executeWithFlags(PgPreparedStatement.java:194)
	at org.postgresql.jdbc.PgPreparedStatement.execute(PgPreparedStatement.java:180)
	at com.zaxxer.hikari.pool.ProxyPreparedStatement.execute(ProxyPreparedStatement.java:44)
	at com.zaxxer.hikari.pool.HikariProxyPreparedStatement.execute(HikariProxyPreparedStatement.java)
	at org.sonatype.nexus.upgrade.datastore.DatabaseMigrationStep.runStatement(DatabaseMigrationStep.java:56)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPgTrgmIndexIfSupported(SearchTableIndexesMigrationStep_2_77.java:226)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPostgreSQLSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:85)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:60)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.migrate(SearchTableIndexesMigrationStep_2_77.java:51)
	at org.sonatype.nexus.upgrade.datastore.internal.NexusJavaMigration.migrate(NexusJavaMigration.java:96)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.executeOnce(JavaMigrationExecutor.java:55)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.lambda$execute$0(JavaMigrationExecutor.java:48)
	at org.flywaydb.core.internal.database.DefaultExecutionStrategy.execute(DefaultExecutionStrategy.java:27)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.execute(JavaMigrationExecutor.java:47)
	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:377)
	... 61 common frames omitted
2026-02-12 09:49:21,847-0800 WARN  [JettyShutdownThread]  *SYSTEM org.eclipse.jetty.util.component.ContainerLifeCycle - Unable to destroy
java.lang.IllegalStateException: !STOPPED
	at org.eclipse.jetty.ee8.nested.HandlerWrapper.destroy(HandlerWrapper.java:119)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.destroy(WebAppContext.java:548)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.destroy(ContainerLifeCycle.java:228)
	at org.eclipse.jetty.server.Handler$Abstract.destroy(Handler.java:507)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$destroy$2(ContextHandler.java:1018)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.run(ContextHandler.java:1517)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.run(ContextHandler.java:1504)
	at org.eclipse.jetty.server.handler.ContextHandler.destroy(ContextHandler.java:1018)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.destroy(ContainerLifeCycle.java:228)
	at org.eclipse.jetty.server.Handler$Abstract.destroy(Handler.java:507)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.destroy(ContainerLifeCycle.java:228)
	at org.eclipse.jetty.server.Handler$Abstract.destroy(Handler.java:507)
	at org.eclipse.jetty.util.thread.ShutdownThread.run(ShutdownThread.java:142)
2026-02-12 09:49:21,849-0800 WARN  [main]  *SYSTEM org.springframework.context.annotation.AnnotationConfigApplicationContext - Exception encountered during context initialization - cancelling refresh attempt: org.springframework.context.ApplicationContextException: Failed to start bean 'org.sonatype.nexus.bootstrap.jetty.ManagedJetty'
2026-02-12 09:49:21,917-0800 WARN  [main]  *SYSTEM org.springframework.context.annotation.AnnotationConfigApplicationContext - Exception encountered during context initialization - cancelling refresh attempt: java.lang.RuntimeException: Failed to configure application
2026-02-12 09:49:21,918-0800 ERROR [main]  *SYSTEM org.springframework.boot.SpringApplication - Application run failed
java.lang.RuntimeException: Failed to configure application
	at org.sonatype.nexus.bootstrap.entrypoint.ApplicationLauncher.onContextRefreshed(ApplicationLauncher.java:112)
	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:103)
	at java.base/java.lang.reflect.Method.invoke(Method.java:580)
	at org.springframework.context.event.ApplicationListenerMethodAdapter.doInvoke(ApplicationListenerMethodAdapter.java:383)
	at org.springframework.context.event.ApplicationListenerMethodAdapter.processEvent(ApplicationListenerMethodAdapter.java:255)
	at org.springframework.context.event.ApplicationListenerMethodAdapter.onApplicationEvent(ApplicationListenerMethodAdapter.java:174)
	at org.springframework.context.event.SimpleApplicationEventMulticaster.doInvokeListener(SimpleApplicationEventMulticaster.java:185)
	at org.springframework.context.event.SimpleApplicationEventMulticaster.invokeListener(SimpleApplicationEventMulticaster.java:178)
	at org.springframework.context.event.SimpleApplicationEventMulticaster.multicastEvent(SimpleApplicationEventMulticaster.java:156)
	at org.springframework.context.support.AbstractApplicationContext.publishEvent(AbstractApplicationContext.java:454)
	at org.springframework.context.support.AbstractApplicationContext.publishEvent(AbstractApplicationContext.java:387)
	at org.springframework.context.support.AbstractApplicationContext.finishRefresh(AbstractApplicationContext.java:1009)
	at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:630)
	at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:755)
	at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:456)
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:335)
	at org.springframework.boot.builder.SpringApplicationBuilder.run(SpringApplicationBuilder.java:149)
	at com.sonatype.nexus.bootstrap.entrypoint.pro.SonatypeNexusRepositoryApplication.main(SonatypeNexusRepositoryApplication.java:44)
	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:103)
	at java.base/java.lang.reflect.Method.invoke(Method.java:580)
	at org.springframework.boot.loader.launch.Launcher.launch(Launcher.java:102)
	at org.springframework.boot.loader.launch.Launcher.launch(Launcher.java:64)
	at org.springframework.boot.loader.launch.JarLauncher.main(JarLauncher.java:40)
Caused by: org.springframework.context.ApplicationContextException: Failed to start bean 'org.sonatype.nexus.bootstrap.jetty.ManagedJetty'
	at org.springframework.context.support.DefaultLifecycleProcessor.doStart(DefaultLifecycleProcessor.java:408)
	at org.springframework.context.support.DefaultLifecycleProcessor.doStart(DefaultLifecycleProcessor.java:394)
	at org.springframework.context.support.DefaultLifecycleProcessor$LifecycleGroup.start(DefaultLifecycleProcessor.java:586)
	at java.base/java.lang.Iterable.forEach(Iterable.java:75)
	at org.springframework.context.support.DefaultLifecycleProcessor.startBeans(DefaultLifecycleProcessor.java:364)
	at org.springframework.context.support.DefaultLifecycleProcessor.onRefresh(DefaultLifecycleProcessor.java:310)
	at org.springframework.context.support.AbstractApplicationContext.finishRefresh(AbstractApplicationContext.java:1006)
	at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:630)
	at org.sonatype.nexus.bootstrap.entrypoint.SpringComponentScan.finishBootstrapComponentScanning(SpringComponentScan.java:87)
	at org.sonatype.nexus.bootstrap.entrypoint.ApplicationLauncher.onContextRefreshed(ApplicationLauncher.java:109)
	... 22 common frames omitted
Caused by: java.lang.RuntimeException: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:79)
	at org.eclipse.jetty.ee8.nested.ContextHandler.callContextInitialized(ContextHandler.java:786)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.callContextInitialized(ServletContextHandler.java:516)
	at org.eclipse.jetty.ee8.nested.ContextHandler.contextInitialized(ContextHandler.java:735)
	at org.eclipse.jetty.ee8.servlet.ServletHandler.initialize(ServletHandler.java:629)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.startContext(ServletContextHandler.java:311)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startWebapp(WebAppContext.java:1195)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.startContext(WebAppContext.java:1165)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStartInContext(ContextHandler.java:626)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1450)
	at org.eclipse.jetty.ee8.nested.ContextHandler.doStart(ContextHandler.java:615)
	at org.eclipse.jetty.ee8.servlet.ServletContextHandler.doStart(ServletContextHandler.java:243)
	at org.eclipse.jetty.ee8.webapp.WebAppContext.doStart(WebAppContext.java:502)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:113)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.handler.ContextHandler.lambda$doStart$0(ContextHandler.java:757)
	at org.eclipse.jetty.server.handler.ContextHandler$ScopedContext.call(ContextHandler.java:1456)
	at org.eclipse.jetty.server.handler.ContextHandler.doStart(ContextHandler.java:757)
	at org.eclipse.jetty.ee8.nested.ContextHandler$CoreContextHandler.doStart(ContextHandler.java:2290)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at io.dropwizard.metrics.jetty12.AbstractInstrumentedHandler.doStart(AbstractInstrumentedHandler.java:149)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.start(ContainerLifeCycle.java:169)
	at org.eclipse.jetty.server.Server.start(Server.java:641)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStart(ContainerLifeCycle.java:120)
	at org.eclipse.jetty.server.Handler$Abstract.doStart(Handler.java:491)
	at org.eclipse.jetty.server.Server.doStart(Server.java:582)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:93)
	at org.sonatype.nexus.bootstrap.entrypoint.jetty.JettyServer$JettyMainThread.run(JettyServer.java:369)
Caused by: org.sonatype.nexus.upgrade.datastore.UpgradeException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:102)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:68)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start_aroundBody0(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport$AjcClosure1.run(StateGuardLifecycleSupport.java:1)
	at org.aspectj.runtime.reflect.JoinPointImpl.proceed(JoinPointImpl.java:164)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.lambda$0(TransitionsAspect.java:57)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:217)
	at org.sonatype.nexus.common.stateguard.TransitionsAspect.aroundTransitionsMethod(TransitionsAspect.java:55)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:68)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:150)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:106)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.moveToPhase(NexusServletContextListener.java:120)
	at org.sonatype.nexus.extender.internal.NexusServletContextListener.contextInitialized(NexusServletContextListener.java:75)
	... 33 common frames omitted
Caused by: org.flywaydb.core.internal.command.DbMigrate$FlywayMigrateException: SQL State  : 58P01
Error Code : 0
Message    : ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement

	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:388)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$applyMigrations$1(DbMigrate.java:275)
	at org.flywaydb.core.internal.jdbc.TransactionalExecutionTemplate.execute(TransactionalExecutionTemplate.java:55)
	at org.flywaydb.core.internal.command.DbMigrate.applyMigrations(DbMigrate.java:274)
	at org.flywaydb.core.internal.command.DbMigrate.migrateGroup(DbMigrate.java:247)
	at org.flywaydb.core.internal.command.DbMigrate.lambda$migrateAll$0(DbMigrate.java:141)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLAdvisoryLockTemplate.execute(PostgreSQLAdvisoryLockTemplate.java:69)
	at org.flywaydb.core.internal.database.postgresql.PostgreSQLConnection.lock(PostgreSQLConnection.java:99)
	at org.flywaydb.core.internal.schemahistory.JdbcTableSchemaHistory.lock(JdbcTableSchemaHistory.java:139)
	at org.flywaydb.core.internal.command.DbMigrate.migrateAll(DbMigrate.java:141)
	at org.flywaydb.core.internal.command.DbMigrate.migrate(DbMigrate.java:98)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:172)
	at org.flywaydb.core.Flyway$1.execute(Flyway.java:124)
	at org.flywaydb.core.FlywayExecutor.execute(FlywayExecutor.java:205)
	at org.flywaydb.core.Flyway.migrate(Flyway.java:124)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:98)
	... 46 common frames omitted
Caused by: org.postgresql.util.PSQLException: ERROR: could not open extension control file "/usr/share/pgsql/extension/pg_trgm.control": No such file or directory
  Where: SQL statement "CREATE EXTENSION pg_trgm"
PL/pgSQL function inline_code_block line 11 at SQL statement
	at org.postgresql.core.v3.QueryExecutorImpl.receiveErrorResponse(QueryExecutorImpl.java:2725)
	at org.postgresql.core.v3.QueryExecutorImpl.processResults(QueryExecutorImpl.java:2412)
	at org.postgresql.core.v3.QueryExecutorImpl.execute(QueryExecutorImpl.java:371)
	at org.postgresql.jdbc.PgStatement.executeInternal(PgStatement.java:502)
	at org.postgresql.jdbc.PgStatement.execute(PgStatement.java:419)
	at org.postgresql.jdbc.PgPreparedStatement.executeWithFlags(PgPreparedStatement.java:194)
	at org.postgresql.jdbc.PgPreparedStatement.execute(PgPreparedStatement.java:180)
	at com.zaxxer.hikari.pool.ProxyPreparedStatement.execute(ProxyPreparedStatement.java:44)
	at com.zaxxer.hikari.pool.HikariProxyPreparedStatement.execute(HikariProxyPreparedStatement.java)
	at org.sonatype.nexus.upgrade.datastore.DatabaseMigrationStep.runStatement(DatabaseMigrationStep.java:56)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPgTrgmIndexIfSupported(SearchTableIndexesMigrationStep_2_77.java:226)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createPostgreSQLSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:85)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.createSearchComponentsIndexes(SearchTableIndexesMigrationStep_2_77.java:60)
	at org.sonatype.nexus.repository.search.sql.store.upgrade.SearchTableIndexesMigrationStep_2_77.migrate(SearchTableIndexesMigrationStep_2_77.java:51)
	at org.sonatype.nexus.upgrade.datastore.internal.NexusJavaMigration.migrate(NexusJavaMigration.java:96)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.executeOnce(JavaMigrationExecutor.java:55)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.lambda$execute$0(JavaMigrationExecutor.java:48)
	at org.flywaydb.core.internal.database.DefaultExecutionStrategy.execute(DefaultExecutionStrategy.java:27)
	at org.flywaydb.core.internal.resolver.java.JavaMigrationExecutor.execute(JavaMigrationExecutor.java:47)
	at org.flywaydb.core.internal.command.DbMigrate.doMigrateGroup(DbMigrate.java:377)
	... 61 common frames omitted
2026-02-12 10:07:32,007-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.pax.logging.NexusLogActivator - start
2026-02-12 10:07:32,186-0800 WARN  [FelixStartLevel]  *SYSTEM javax.xml.bind - Using non-standard property: javax.xml.bind.JAXBContext. Property javax.xml.bind.JAXBContextFactory should be used instead.
2026-02-12 10:07:32,339-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.features.internal.FeaturesWrapper - Fast FeaturesService starting
2026-02-12 10:07:32,446-0800 WARN  [FelixStartLevel]  *SYSTEM javax.xml.bind - Using non-standard property: javax.xml.bind.JAXBContext. Property javax.xml.bind.JAXBContextFactory should be used instead.
2026-02-12 10:07:33,506-0800 INFO  [FelixStartLevel]  *SYSTEM ROOT - bundle org.apache.felix.scr:2.1.30 (56) Starting with globalExtender setting: false
2026-02-12 10:07:33,511-0800 INFO  [FelixStartLevel]  *SYSTEM ROOT - bundle org.apache.felix.scr:2.1.30 (56)  Version = 2.1.30
2026-02-12 10:07:33,725-0800 WARN  [FelixStartLevel]  *SYSTEM uk.org.lidalia.sysoutslf4j.context.SysOutOverSLF4JInitialiser - Your logging framework class org.ops4j.pax.logging.slf4j.Slf4jLogger is not known - if it needs access to the standard println methods on the console you will need to register it by calling registerLoggingSystemPackage
2026-02-12 10:07:33,726-0800 INFO  [FelixStartLevel]  *SYSTEM uk.org.lidalia.sysoutslf4j.context.SysOutOverSLF4J - Package org.ops4j.pax.logging.slf4j registered; all classes within it or subpackages of it will be allowed to print to System.out and System.err
2026-02-12 10:07:33,730-0800 INFO  [FelixStartLevel]  *SYSTEM uk.org.lidalia.sysoutslf4j.context.SysOutOverSLF4J - Replaced standard System.out and System.err PrintStreams with SLF4JPrintStreams
2026-02-12 10:07:33,731-0800 INFO  [FelixStartLevel]  *SYSTEM uk.org.lidalia.sysoutslf4j.context.SysOutOverSLF4J - Redirected System.out and System.err to SLF4J for this context
2026-02-12 10:07:33,736-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder - Properties:
2026-02-12 10:07:33,736-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   application-host='0.0.0.0'
2026-02-12 10:07:33,737-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   application-port='8081'
2026-02-12 10:07:33,737-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   application-port-ssl='8444'
2026-02-12 10:07:33,737-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   fabric.etc='/opt/appdata/nexus/nexus-3.73.0-12/etc/fabric'
2026-02-12 10:07:33,737-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   jetty.etc='/opt/appdata/nexus/nexus-3.73.0-12/etc/jetty'
2026-02-12 10:07:33,738-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   karaf.base='/opt/appdata/nexus/nexus-3.73.0-12'
2026-02-12 10:07:33,738-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   karaf.data='/opt/appdata/nexus/sonatype-work/nexus3'
2026-02-12 10:07:33,738-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   karaf.etc='/opt/appdata/nexus/nexus-3.73.0-12/etc/karaf'
2026-02-12 10:07:33,738-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   karaf.home='/opt/appdata/nexus/nexus-3.73.0-12'
2026-02-12 10:07:33,738-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   karaf.instances='/opt/appdata/nexus/sonatype-work/nexus3/instances'
2026-02-12 10:07:33,738-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   logback.etc='/opt/appdata/nexus/nexus-3.73.0-12/etc/logback'
2026-02-12 10:07:33,739-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus-args='/opt/appdata/nexus/nexus-3.73.0-12/etc/jetty/jetty.xml,/opt/appdata/nexus/nexus-3.73.0-12/etc/jetty/jetty-https.xml,/opt/appdata/nexus/nexus-3.73.0-12/etc/jetty/jetty-requestlog.xml'
2026-02-12 10:07:33,739-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus-context-path='/'
2026-02-12 10:07:33,739-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus-edition='nexus-pro-edition'
2026-02-12 10:07:33,739-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus-features='nexus-pro-feature'
2026-02-12 10:07:33,739-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus.assetdownloads.enabled='true'
2026-02-12 10:07:33,740-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus.datastore.enabled='true'
2026-02-12 10:07:33,740-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus.scripts.allowCreation='true'
2026-02-12 10:07:33,740-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus.view.exhaustForAgents='Apache-Maven.*|libwww-perl.*'
2026-02-12 10:07:33,740-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   org.sonatype.nexus.repository.httpbridge.internal.HttpBridgeModule.legacy='true'
2026-02-12 10:07:33,740-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   ssl.etc='/opt/appdata/nexus/sonatype-work/nexus3/etc/ssl'
2026-02-12 10:07:33,740-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.Launcher - Java: 17.0.17, OpenJDK 64-Bit Server VM, Red Hat, Inc., 17.0.17+10-LTS
2026-02-12 10:07:33,741-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.Launcher - OS: Linux, 4.18.0-553.89.1.el8_10.x86_64, amd64
2026-02-12 10:07:33,741-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.Launcher - User: nexus, en, /home/nexus
2026-02-12 10:07:33,741-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.Launcher - CWD: /opt/appdata/nexus/nexus-3.73.0-12
2026-02-12 10:07:33,742-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.Launcher - TMP: /opt/appdata/nexus/sonatype-work/nexus3/tmp
2026-02-12 10:07:33,746-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.jetty.JettyServer - Starting
2026-02-12 10:07:33,752-0800 INFO  [FelixStartLevel]  *SYSTEM org.eclipse.jetty.util.log - Logging initialized @4042ms to org.eclipse.jetty.util.log.Slf4jLog
2026-02-12 10:07:33,756-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.jetty.JettyServer - Applying configuration: file:/opt/appdata/nexus/nexus-3.73.0-12/etc/jetty/jetty.xml
2026-02-12 10:07:33,873-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.jetty.JettyServer - Applying configuration: file:/opt/appdata/nexus/nexus-3.73.0-12/etc/jetty/jetty-https.xml
2026-02-12 10:07:33,907-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.jetty.JettyServer - Applying configuration: file:/opt/appdata/nexus/nexus-3.73.0-12/etc/jetty/jetty-requestlog.xml
2026-02-12 10:07:33,922-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.jetty.JettyServer - Starting: Server@36b6d16c{STOPPED}[9.4.53.v20231009]
2026-02-12 10:07:33,925-0800 INFO  [jetty-main-1]  *SYSTEM org.eclipse.jetty.server.Server - jetty-9.4.53.v20231009; built: 2023-10-09T12:29:09.265Z; git: 27bde00a0b95a1d5bbee0eae7984f891d2d0f8c9; jvm 17.0.17+10-LTS
2026-02-12 10:07:33,985-0800 INFO  [jetty-main-1]  *SYSTEM org.eclipse.jetty.server.session - DefaultSessionIdManager workerName=node0
2026-02-12 10:07:33,985-0800 INFO  [jetty-main-1]  *SYSTEM org.eclipse.jetty.server.session - No SessionScavenger set, using defaults
2026-02-12 10:07:33,987-0800 INFO  [jetty-main-1]  *SYSTEM org.eclipse.jetty.server.session - node0 Scavenging every 660000ms
2026-02-12 10:07:33,994-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.osgi.BootstrapListener - Initializing
2026-02-12 10:07:33,999-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.osgi.ProNexusEdition - Loading Pro Edition
2026-02-12 10:07:34,001-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.osgi.BootstrapListener - Installing: nexus-pro-edition/3.73.0.12 (nexus-datastore-mybatis/3.73.0.12)
2026-02-12 10:07:36,375-0800 INFO  [jetty-main-1]  *SYSTEM org.ehcache.core.osgi.EhcacheActivator - Detected OSGi Environment (core is in bundle: org.ehcache [156]): Using OSGi Based Service Loading
2026-02-12 10:07:36,926-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.osgi.BootstrapListener - Installed: nexus-pro-edition/3.73.0.12 (nexus-datastore-mybatis/3.73.0.12)
2026-02-12 10:07:37,265-0800 INFO  [jetty-main-1]  *SYSTEM org.apache.shiro.nexus.NexusWebSessionManager - Global session timeout: 1800000 ms
2026-02-12 10:07:37,265-0800 INFO  [jetty-main-1]  *SYSTEM org.apache.shiro.nexus.NexusWebSessionManager - Session-cookie prototype: name=NXSESSIONID, secure=true
2026-02-12 10:07:37,288-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.common [3.73.0.12]
2026-02-12 10:07:37,371-0800 INFO  [jetty-main-1]  *SYSTEM org.hibernate.validator.internal.util.Version - HV000001: Hibernate Validator 6.2.0.Final
2026-02-12 10:07:37,571-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.common [3.73.0.12]
2026-02-12 10:07:37,572-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.hibernate.validator [6.2.0.Final]
2026-02-12 10:07:37,590-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.hibernate.validator [6.2.0.Final]
2026-02-12 10:07:37,591-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.blobstore-api [3.73.0.12]
2026-02-12 10:07:37,606-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.blobstore-api [3.73.0.12]
2026-02-12 10:07:37,606-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.cache [3.73.0.12]
2026-02-12 10:07:37,630-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.cache [3.73.0.12]
2026-02-12 10:07:37,631-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.jmx [3.73.0.12]
2026-02-12 10:07:37,649-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.jmx [3.73.0.12]
2026-02-12 10:07:37,650-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.crypto [3.73.0.12]
2026-02-12 10:07:37,774-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.crypto [3.73.0.12]
2026-02-12 10:07:37,775-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.security [3.73.0.12]
2026-02-12 10:07:37,935-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.security [3.73.0.12]
2026-02-12 10:07:37,935-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.datastore [3.73.0.12]
2026-02-12 10:07:37,968-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.datastore [3.73.0.12]
2026-02-12 10:07:37,969-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.supportzip-api [3.73.0.12]
2026-02-12 10:07:37,989-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.supportzip-api [3.73.0.12]
2026-02-12 10:07:37,990-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.thread [3.73.0.12]
2026-02-12 10:07:38,004-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.thread [3.73.0.12]
2026-02-12 10:07:38,005-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.scheduling [3.73.0.12]
2026-02-12 10:07:38,045-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.scheduling [3.73.0.12]
2026-02-12 10:07:38,046-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.blobstore [3.73.0.12]
2026-02-12 10:07:38,083-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.blobstore [3.73.0.12]
2026-02-12 10:07:38,083-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.apache.tika.core [1.28.4]
2026-02-12 10:07:38,096-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.apache.tika.core [1.28.4]
2026-02-12 10:07:38,098-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.upgrade [3.73.0.12]
2026-02-12 10:07:38,122-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.upgrade [3.73.0.12]
2026-02-12 10:07:38,122-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.blobstore-file [3.73.0.12]
2026-02-12 10:07:38,162-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.blobstore-file [3.73.0.12]
2026-02-12 10:07:38,163-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.capability [3.73.0.12]
2026-02-12 10:07:38,182-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.capability [3.73.0.12]
2026-02-12 10:07:38,182-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.commands [3.73.0.12]
2026-02-12 10:07:38,196-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.commands [3.73.0.12]
2026-02-12 10:07:38,196-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.email [3.73.0.12]
2026-02-12 10:07:38,208-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.email [3.73.0.12]
2026-02-12 10:07:38,208-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.httpclient [3.73.0.12]
2026-02-12 10:07:38,222-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.httpclient [3.73.0.12]
2026-02-12 10:07:38,222-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.servlet [3.73.0.12]
2026-02-12 10:07:38,232-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.servlet [3.73.0.12]
2026-02-12 10:07:38,232-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.ssl [3.73.0.12]
2026-02-12 10:07:38,243-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.ssl [3.73.0.12]
2026-02-12 10:07:38,243-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.base [3.73.0.12]
2026-02-12 10:07:38,359-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.internal.metrics.MetricsModule - Metrics support configured
2026-02-12 10:07:38,382-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.internal.metrics.MetricsModule - Metrics support configured
2026-02-12 10:07:38,707-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.base [3.73.0.12]
2026-02-12 10:07:38,708-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.extdirect [3.73.0.12]
2026-02-12 10:07:38,738-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.extdirect [3.73.0.12]
2026-02-12 10:07:38,740-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.siesta [3.73.0.12]
2026-02-12 10:07:38,787-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.siesta [3.73.0.12]
2026-02-12 10:07:38,788-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.rest-jackson2 [3.73.0.12]
2026-02-12 10:07:38,798-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.rest-jackson2 [3.73.0.12]
2026-02-12 10:07:38,799-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.swagger [3.73.0.12]
2026-02-12 10:07:38,817-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.swagger [3.73.0.12]
2026-02-12 10:07:38,817-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.rapture [3.73.0.12]
2026-02-12 10:07:38,898-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.rapture [3.73.0.12]
2026-02-12 10:07:38,899-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.datastore-mybatis [3.73.0.12]
2026-02-12 10:07:38,927-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.datastore-mybatis [3.73.0.12]
2026-02-12 10:07:38,928-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.quartz [3.73.0.12]
2026-02-12 10:07:38,960-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.quartz [3.73.0.12]
2026-02-12 10:07:38,960-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING wrap_file_system_com_sonatype_licensing_license-bundle_1.6.0_license-bundle-1.6.0.jar [0.0.0]
2026-02-12 10:07:38,988-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED wrap_file_system_com_sonatype_licensing_license-bundle_1.6.0_license-bundle-1.6.0.jar [0.0.0]
2026-02-12 10:07:38,988-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.licensing-extension [3.73.0.12]
2026-02-12 10:07:39,014-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.licensing-extension [3.73.0.12]
2026-02-12 10:07:39,015-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.pro-edition [3.73.0.12]
2026-02-12 10:07:39,024-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.pro-edition [3.73.0.12]
2026-02-12 10:07:39,025-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusContextListener - Running lifecycle phases [KERNEL, STORAGE, RESTORE, UPGRADE, SCHEMAS, EVENTS, SECURITY, SERVICES, REPOSITORIES, CAPABILITIES, TASKS]
2026-02-12 10:07:39,026-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start KERNEL
2026-02-12 10:07:39,086-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.internal.log.overrides.file.LogbackLoggerOverrides - File: /opt/appdata/nexus/sonatype-work/nexus3/etc/logback/logback-overrides.xml
2026-02-12 10:07:39,087-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.internal.log.LogbackLogManager - Configuring
2026-02-12 10:07:39,100-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusContextListener - Installing: [nexus-pro-feature/3.73.0.12, nexus-datastore-mybatis/3.73.0.12, nexus-group-deploy/3.73.0.12, nexus-repository-cargo/3.73.0.12]
2026-02-12 10:07:49,739-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusContextListener - Installed: [nexus-pro-feature/3.73.0.12, nexus-datastore-mybatis/3.73.0.12, nexus-group-deploy/3.73.0.12, nexus-repository-cargo/3.73.0.12]
2026-02-12 10:07:49,754-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-audit-plugin [3.73.0.12]
2026-02-12 10:07:49,773-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-audit-plugin [3.73.0.12]
2026-02-12 10:07:49,783-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-ssl-plugin [3.73.0.12]
2026-02-12 10:07:49,807-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-ssl-plugin [3.73.0.12]
2026-02-12 10:07:50,336-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-blobstore-s3 [3.73.0.12]
2026-02-12 10:07:50,561-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-blobstore-s3 [3.73.0.12]
2026-02-12 10:07:50,564-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.selector [3.73.0.12]
2026-02-12 10:07:50,585-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.selector [3.73.0.12]
2026-02-12 10:07:50,585-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.core [3.73.0.12]
2026-02-12 10:07:50,786-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.core [3.73.0.12]
2026-02-12 10:07:50,788-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.elasticsearch [3.73.0.12]
2026-02-12 10:07:50,809-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.elasticsearch [3.73.0.12]
2026-02-12 10:07:50,810-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.repository-content [3.73.0.12]
2026-02-12 10:07:51,062-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.repository-content [3.73.0.12]
2026-02-12 10:07:51,063-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.repository-config [3.73.0.12]
2026-02-12 10:07:51,099-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.repository-config [3.73.0.12]
2026-02-12 10:07:51,100-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-coreui-plugin [3.73.0.12]
2026-02-12 10:07:51,198-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-coreui-plugin [3.73.0.12]
2026-02-12 10:07:51,210-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-repository-httpbridge [3.73.0.12]
2026-02-12 10:07:51,232-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-repository-httpbridge [3.73.0.12]
2026-02-12 10:07:51,478-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-blobstore-tasks [3.73.0.12]
2026-02-12 10:07:51,513-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-blobstore-tasks [3.73.0.12]
2026-02-12 10:07:51,515-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.cleanup-config [3.73.0.12]
2026-02-12 10:07:51,535-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.cleanup-config [3.73.0.12]
2026-02-12 10:07:51,536-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-repository-maven [3.73.0.12]
2026-02-12 10:07:51,667-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-repository-maven [3.73.0.12]
2026-02-12 10:07:51,668-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-script-plugin [3.73.0.12]
2026-02-12 10:07:51,697-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-script-plugin [3.73.0.12]
2026-02-12 10:07:51,703-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-task-log-cleanup [3.73.0.12]
2026-02-12 10:07:51,714-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-task-log-cleanup [3.73.0.12]
2026-02-12 10:07:51,721-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-onboarding-plugin [3.73.0.12]
2026-02-12 10:07:51,738-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-onboarding-plugin [3.73.0.12]
2026-02-12 10:07:51,747-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-default-role-plugin [3.73.0.12]
2026-02-12 10:07:51,761-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-default-role-plugin [3.73.0.12]
2026-02-12 10:07:51,780-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-repository-apt [3.73.0.12]
2026-02-12 10:07:51,855-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-repository-apt [3.73.0.12]
2026-02-12 10:07:52,084-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-repository-raw [3.73.0.12]
2026-02-12 10:07:52,131-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-repository-raw [3.73.0.12]
2026-02-12 10:07:52,159-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.cleanup [3.73.0.12]
2026-02-12 10:07:52,183-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.cleanup [3.73.0.12]
2026-02-12 10:07:52,248-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-ldap-plugin [3.73.0.12]
2026-02-12 10:07:52,289-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-ldap-plugin [3.73.0.12]
2026-02-12 10:07:52,475-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-tags-plugin [3.73.0.12]
2026-02-12 10:07:52,538-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-tags-plugin [3.73.0.12]
2026-02-12 10:07:52,539-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-proui-plugin [3.73.0.12]
2026-02-12 10:07:52,551-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-proui-plugin [3.73.0.12]
2026-02-12 10:07:52,557-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-proximanova-plugin [3.73.0.12]
2026-02-12 10:07:52,565-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-proximanova-plugin [3.73.0.12]
2026-02-12 10:07:52,653-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING wrap_file_system_com_sonatype_insight_scan_insight-scanner-core_2.36.66-01_insight-scanner-core-2.36.66-01.jar [0.0.0]
2026-02-12 10:07:52,665-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED wrap_file_system_com_sonatype_insight_scan_insight-scanner-core_2.36.66-01_insight-scanner-core-2.36.66-01.jar [0.0.0]
2026-02-12 10:07:52,666-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING wrap_file_system_com_sonatype_insight_scan_insight-scanner-model-io_2.36.66-01_insight-scanner-model-io-2.36.66-01.jar [0.0.0]
2026-02-12 10:07:52,679-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED wrap_file_system_com_sonatype_insight_scan_insight-scanner-model-io_2.36.66-01_insight-scanner-model-io-2.36.66-01.jar [0.0.0]
2026-02-12 10:07:52,680-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-healthcheck-base [3.73.0.12]
2026-02-12 10:07:53,422-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-healthcheck-base [3.73.0.12]
2026-02-12 10:07:53,423-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-malicious-risk-plugin [3.73.0.12]
2026-02-12 10:07:53,441-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-malicious-risk-plugin [3.73.0.12]
2026-02-12 10:07:53,444-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-usertoken-plugin [3.73.0.12]
2026-02-12 10:07:53,492-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-usertoken-plugin [3.73.0.12]
2026-02-12 10:07:53,493-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-analytics-plugin [3.73.0.12]
2026-02-12 10:07:53,575-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-analytics-plugin [3.73.0.12]
2026-02-12 10:07:53,576-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-licensing-plugin [3.73.0.12]
2026-02-12 10:07:53,595-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-licensing-plugin [3.73.0.12]
2026-02-12 10:07:53,667-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-crowd-plugin [3.73.0.12]
2026-02-12 10:07:53,710-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-crowd-plugin [3.73.0.12]
2026-02-12 10:07:53,711-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-npm [3.73.0.12]
2026-02-12 10:07:53,842-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-npm [3.73.0.12]
2026-02-12 10:07:53,844-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-nuget [3.73.0.12]
2026-02-12 10:07:53,994-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-nuget [3.73.0.12]
2026-02-12 10:07:53,995-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-rubygems [3.73.0.12]
2026-02-12 10:07:54,086-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-rubygems [3.73.0.12]
2026-02-12 10:07:54,088-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.rest-client [3.73.0.12]
2026-02-12 10:07:54,096-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.rest-client [3.73.0.12]
2026-02-12 10:07:54,096-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-migration-plugin [3.73.0.12]
2026-02-12 10:07:54,227-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-migration-plugin [3.73.0.12]
2026-02-12 10:07:54,288-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-vulnerability-plugin [3.73.0.12]
2026-02-12 10:07:54,328-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-vulnerability-plugin [3.73.0.12]
2026-02-12 10:07:54,329-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-outreach-plugin [3.73.0.12]
2026-02-12 10:07:54,355-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-outreach-plugin [3.73.0.12]
2026-02-12 10:07:54,367-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-rutauth-plugin [3.73.0.12]
2026-02-12 10:07:54,382-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-rutauth-plugin [3.73.0.12]
2026-02-12 10:07:54,415-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-yum [3.73.0.12]
2026-02-12 10:07:54,526-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-yum [3.73.0.12]
2026-02-12 10:07:54,563-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-group-deploy [3.73.0.12]
2026-02-12 10:07:54,575-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-group-deploy [3.73.0.12]
2026-02-12 10:07:54,575-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-docker [3.73.0.12]
2026-02-12 10:07:54,704-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-docker [3.73.0.12]
2026-02-12 10:07:54,743-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-ahc-plugin [3.73.0.12]
2026-02-12 10:07:54,783-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-ahc-plugin [3.73.0.12]
2026-02-12 10:07:54,930-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-pypi [3.73.0.12]
2026-02-12 10:07:55,014-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-pypi [3.73.0.12]
2026-02-12 10:07:55,029-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-conda [3.73.0.12]
2026-02-12 10:07:55,057-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-conda [3.73.0.12]
2026-02-12 10:07:55,073-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-conan [3.73.0.12]
2026-02-12 10:07:55,136-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-conan [3.73.0.12]
2026-02-12 10:07:55,150-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-gitlfs [3.73.0.12]
2026-02-12 10:07:55,181-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-gitlfs [3.73.0.12]
2026-02-12 10:07:55,213-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-r [3.73.0.12]
2026-02-12 10:07:55,254-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-r [3.73.0.12]
2026-02-12 10:07:55,272-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-replication-plugin [3.73.0.12]
2026-02-12 10:07:55,293-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-replication-plugin [3.73.0.12]
2026-02-12 10:07:55,306-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-cocoapods [3.73.0.12]
2026-02-12 10:07:55,336-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-cocoapods [3.73.0.12]
2026-02-12 10:07:55,349-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-golang [3.73.0.12]
2026-02-12 10:07:55,390-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-golang [3.73.0.12]
2026-02-12 10:07:55,405-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-p2 [3.73.0.12]
2026-02-12 10:07:55,444-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-p2 [3.73.0.12]
2026-02-12 10:07:55,483-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-cleanup-pro-plugin [3.73.0.12]
2026-02-12 10:07:55,496-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-cleanup-pro-plugin [3.73.0.12]
2026-02-12 10:07:55,511-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-clm-plugin [3.73.0.12]
2026-02-12 10:07:55,540-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-clm-plugin [3.73.0.12]
2026-02-12 10:07:55,557-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-staging-plugin [3.73.0.12]
2026-02-12 10:07:55,576-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-staging-plugin [3.73.0.12]
2026-02-12 10:07:55,578-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING nexus-blobstore-azure-cloud [3.73.0.12]
2026-02-12 10:07:55,617-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED nexus-blobstore-azure-cloud [3.73.0.12]
2026-02-12 10:07:55,645-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-blobstore-group [3.73.0.12]
2026-02-12 10:07:55,668-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-blobstore-group [3.73.0.12]
2026-02-12 10:07:55,680-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-pro-system-checks-plugin [3.73.0.12]
2026-02-12 10:07:55,701-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-pro-system-checks-plugin [3.73.0.12]
2026-02-12 10:07:55,774-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-saml-plugin [3.73.0.12]
2026-02-12 10:07:55,929-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-saml-plugin [3.73.0.12]
2026-02-12 10:07:55,945-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-export-import-plugin [3.73.0.12]
2026-02-12 10:07:56,032-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-export-import-plugin [3.73.0.12]
2026-02-12 10:07:56,049-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-pro-datastore-plugin [3.73.0.12]
2026-02-12 10:07:56,106-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-pro-datastore-plugin [3.73.0.12]
2026-02-12 10:07:56,118-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-move-plugin [3.73.0.12]
2026-02-12 10:07:56,144-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-move-plugin [3.73.0.12]
2026-02-12 10:07:56,172-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-helm [3.73.0.12]
2026-02-12 10:07:56,236-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-helm [3.73.0.12]
2026-02-12 10:07:56,250-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-api-extension-plugin [3.73.0.12]
2026-02-12 10:07:56,271-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-api-extension-plugin [3.73.0.12]
2026-02-12 10:07:56,285-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-cargo [3.73.0.12]
2026-02-12 10:07:56,335-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-cargo [3.73.0.12]
2026-02-12 10:07:56,336-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start STORAGE
2026-02-12 10:07:56,358-0800 INFO  [FelixStartLevel]  *SYSTEM com.sonatype.nexus.datastore.DataStoreConfigurationFileSource - Loaded 'nexus' data store configuration from properties file (postgresql)
2026-02-12 10:07:56,389-0800 WARN  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - Database directory contains unsupported legacy database files; remove legacy files as soon as possible.
2026-02-12 10:07:56,395-0800 INFO  [FelixStartLevel]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Starting...
2026-02-12 10:07:56,477-0800 INFO  [FelixStartLevel]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Start completed.
2026-02-12 10:07:56,478-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Loading MyBatis configuration from /opt/appdata/nexus/nexus-3.73.0-12/etc/fabric/mybatis.xml
2026-02-12 10:07:56,540-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - MyBatis databaseId: PostgreSQL
2026-02-12 10:07:56,652-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for UpgradeTaskDAO
2026-02-12 10:07:56,700-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SoftDeletedBlobsDAO
2026-02-12 10:07:56,751-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for JwtSecretDAO
2026-02-12 10:07:56,771-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for LoggingOverridesDAO
2026-02-12 10:07:56,798-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DeploymentIdDAO
2026-02-12 10:07:56,812-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NodeIdDAO
2026-02-12 10:07:56,830-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AnonymousConfigurationDAO
2026-02-12 10:07:56,854-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CPrivilegeDAO
2026-02-12 10:07:56,885-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CRoleDAO
2026-02-12 10:07:56,900-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CUserDAO
2026-02-12 10:07:56,915-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CUserRoleMappingDAO
2026-02-12 10:07:56,944-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RealmConfigurationDAO
2026-02-12 10:07:56,961-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SecretsDAO
2026-02-12 10:07:56,992-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for QuartzDAO
2026-02-12 10:07:57,052-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for KeyStoreDAO
2026-02-12 10:07:57,067-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CapabilityStorageItemDAO
2026-02-12 10:07:57,082-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for EmailConfigurationDAO
2026-02-12 10:07:57,095-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HttpClientConfigurationDAO
2026-02-12 10:07:57,110-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NexusKeyValueDAO
2026-02-12 10:07:57,139-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ApiKeyDAO
2026-02-12 10:07:57,168-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ApiKeyV2DAO
2026-02-12 10:07:57,194-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SelectorConfigurationDAO
2026-02-12 10:07:57,208-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for BlobStoreMetricsDAO
2026-02-12 10:07:57,221-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConfigurationDAO
2026-02-12 10:07:57,235-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for BlobStoreConfigurationDAO
2026-02-12 10:07:57,248-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RoutingRuleDAO
2026-02-12 10:07:57,261-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CleanupPolicyDAO
2026-02-12 10:07:57,298-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2ContentRepositoryDAO
2026-02-12 10:07:57,336-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2ComponentDAO
2026-02-12 10:07:57,428-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2AssetBlobDAO
2026-02-12 10:07:57,481-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2AssetDAO
2026-02-12 10:07:57,517-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2BrowseNodeDAO
2026-02-12 10:07:57,544-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ScriptDAO
2026-02-12 10:07:57,555-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptContentRepositoryDAO
2026-02-12 10:07:57,581-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptKeyValueDAO
2026-02-12 10:07:57,615-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptComponentDAO
2026-02-12 10:07:57,690-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptAssetBlobDAO
2026-02-12 10:07:57,740-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptAssetDAO
2026-02-12 10:07:57,773-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptBrowseNodeDAO
2026-02-12 10:07:57,794-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawContentRepositoryDAO
2026-02-12 10:07:57,810-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawComponentDAO
2026-02-12 10:07:57,846-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawAssetBlobDAO
2026-02-12 10:07:57,889-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawAssetDAO
2026-02-12 10:07:57,924-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawBrowseNodeDAO
2026-02-12 10:07:57,949-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for LdapConfigurationDAO
2026-02-12 10:07:57,961-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TagDAO
2026-02-12 10:07:57,986-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptComponentTagDAO
2026-02-12 10:07:58,001-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoComponentTagDAO
2026-02-12 10:07:58,017-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsComponentTagDAO
2026-02-12 10:07:58,034-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanComponentTagDAO
2026-02-12 10:07:58,049-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaComponentTagDAO
2026-02-12 10:07:58,065-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerComponentTagDAO
2026-02-12 10:07:58,081-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsComponentTagDAO
2026-02-12 10:07:58,096-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoComponentTagDAO
2026-02-12 10:07:58,111-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmComponentTagDAO
2026-02-12 10:07:58,127-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2ComponentTagDAO
2026-02-12 10:07:58,142-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmComponentTagDAO
2026-02-12 10:07:58,157-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetComponentTagDAO
2026-02-12 10:07:58,172-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2ComponentTagDAO
2026-02-12 10:07:58,187-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiComponentTagDAO
2026-02-12 10:07:58,202-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RComponentTagDAO
2026-02-12 10:07:58,217-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawComponentTagDAO
2026-02-12 10:07:58,233-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsComponentTagDAO
2026-02-12 10:07:58,248-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumComponentTagDAO
2026-02-12 10:07:58,259-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for FirewallIgnorePatternsDAO
2026-02-12 10:07:58,269-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RepositoryHealthCheckConfigurationDAO
2026-02-12 10:07:58,282-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for UserTokenRecordDAO
2026-02-12 10:07:58,312-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AggregatedMetricsDAO
2026-02-12 10:07:58,341-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HistoricalLoginInfoDAO
2026-02-12 10:07:58,364-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for MetricDAO
2026-02-12 10:07:58,383-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmContentRepositoryDAO
2026-02-12 10:07:58,403-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmComponentDAO
2026-02-12 10:07:58,443-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmAssetBlobDAO
2026-02-12 10:07:58,490-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmAssetDAO
2026-02-12 10:07:58,534-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmBrowseNodeDAO
2026-02-12 10:07:58,564-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetAssetBlobDAO
2026-02-12 10:07:58,597-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetContentRepositoryDAO
2026-02-12 10:07:58,610-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetComponentDAO
2026-02-12 10:07:58,650-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetAssetDAO
2026-02-12 10:07:58,681-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetBrowseNodeDAO
2026-02-12 10:07:58,700-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsContentRepositoryDAO
2026-02-12 10:07:58,712-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsComponentDAO
2026-02-12 10:07:58,747-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsAssetBlobDAO
2026-02-12 10:07:58,800-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsAssetDAO
2026-02-12 10:07:58,834-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsBrowseNodeDAO
2026-02-12 10:07:58,859-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsComponentDAO
2026-02-12 10:07:58,899-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DownloadCountDAO
2026-02-12 10:07:58,922-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Log4JVisualizerConfigurationDAO
2026-02-12 10:07:58,975-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumContentRepositoryDAO
2026-02-12 10:07:58,999-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumComponentDAO
2026-02-12 10:07:59,036-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumKeyValueDAO
2026-02-12 10:07:59,060-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumAssetBlobDAO
2026-02-12 10:07:59,102-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumAssetDAO
2026-02-12 10:07:59,134-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumBrowseNodeDAO
2026-02-12 10:07:59,166-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerAssetBlobDAO
2026-02-12 10:07:59,198-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerContentRepositoryDAO
2026-02-12 10:07:59,210-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerComponentDAO
2026-02-12 10:07:59,249-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerAssetDAO
2026-02-12 10:07:59,283-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerBrowseNodeDAO
2026-02-12 10:07:59,305-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerForeignLayersDAO
2026-02-12 10:07:59,328-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComponentApplicationScanDAO
2026-02-12 10:07:59,363-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComponentApplicationScanScheduleDAO
2026-02-12 10:07:59,394-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiContentRepositoryDAO
2026-02-12 10:07:59,407-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiComponentDAO
2026-02-12 10:07:59,442-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiAssetBlobDAO
2026-02-12 10:07:59,483-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiAssetDAO
2026-02-12 10:07:59,566-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiBrowseNodeDAO
2026-02-12 10:07:59,585-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaContentRepositoryDAO
2026-02-12 10:07:59,596-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaComponentDAO
2026-02-12 10:07:59,628-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaAssetBlobDAO
2026-02-12 10:07:59,665-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaAssetDAO
2026-02-12 10:07:59,696-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaBrowseNodeDAO
2026-02-12 10:07:59,726-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanAssetBlobDAO
2026-02-12 10:07:59,757-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanContentRepositoryDAO
2026-02-12 10:07:59,768-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanComponentDAO
2026-02-12 10:07:59,806-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanAssetDAO
2026-02-12 10:07:59,839-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanBrowseNodeDAO
2026-02-12 10:07:59,871-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsContentRepositoryDAO
2026-02-12 10:07:59,881-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsComponentDAO
2026-02-12 10:07:59,914-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsAssetBlobDAO
2026-02-12 10:07:59,952-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsAssetDAO
2026-02-12 10:07:59,991-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsBrowseNodeDAO
2026-02-12 10:08:00,011-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RContentRepositoryDAO
2026-02-12 10:08:00,023-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RComponentDAO
2026-02-12 10:08:00,059-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RAssetBlobDAO
2026-02-12 10:08:00,100-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RAssetDAO
2026-02-12 10:08:00,134-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RBrowseNodeDAO
2026-02-12 10:08:00,155-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsContentRepositoryDAO
2026-02-12 10:08:00,165-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsComponentDAO
2026-02-12 10:08:00,199-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsAssetBlobDAO
2026-02-12 10:08:00,236-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsAssetDAO
2026-02-12 10:08:00,268-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsBrowseNodeDAO
2026-02-12 10:08:00,289-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoContentRepositoryDAO
2026-02-12 10:08:00,299-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoComponentDAO
2026-02-12 10:08:00,336-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoAssetBlobDAO
2026-02-12 10:08:00,378-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoAssetDAO
2026-02-12 10:08:00,411-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoBrowseNodeDAO
2026-02-12 10:08:00,432-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2AssetBlobDAO
2026-02-12 10:08:00,465-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2ContentRepositoryDAO
2026-02-12 10:08:00,477-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2ComponentDAO
2026-02-12 10:08:00,513-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2AssetDAO
2026-02-12 10:08:00,546-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2BrowseNodeDAO
2026-02-12 10:08:00,570-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DeletedBlobDAO
2026-02-12 10:08:00,594-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NodeHeartbeatDAO
2026-02-12 10:08:00,627-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SamlConfigurationDAO
2026-02-12 10:08:00,638-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SamlUserDAO
2026-02-12 10:08:00,648-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RepositoryMetricsDAO
2026-02-12 10:08:00,673-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ChangeRepositoryBlobstoreDAO
2026-02-12 10:08:00,690-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmContentRepositoryDAO
2026-02-12 10:08:00,708-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmKeyValueDAO
2026-02-12 10:08:00,729-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmComponentDAO
2026-02-12 10:08:00,761-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmAssetBlobDAO
2026-02-12 10:08:00,794-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmAssetDAO
2026-02-12 10:08:00,836-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmBrowseNodeDAO
2026-02-12 10:08:00,855-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoAssetBlobDAO
2026-02-12 10:08:00,885-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoContentRepositoryDAO
2026-02-12 10:08:00,895-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoComponentDAO
2026-02-12 10:08:00,953-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoAssetDAO
2026-02-12 10:08:00,986-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CargoBrowseNodeDAO
2026-02-12 10:08:01,022-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.internal.node.datastore.LocalNodeAccess - ID: CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585
2026-02-12 10:08:01,049-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start RESTORE
2026-02-12 10:08:01,104-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start UPGRADE
2026-02-12 10:08:01,252-0800 ERROR [FelixStartLevel]  *SYSTEM org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl - Missing migrations: [BrowseNodeMigrationStep_2_3, CustomS3RegionCapabilityMigrationStep_2_4, GoogleBlobStoreMigrationStep_2_5, S3FailoverMigrationStep_2_6, SoftDeletedBlobsByBlobStoreIndexMigrationStep_2_7, ConanV2UpgradeStep_2_8, MalwareRemediatorTaskMigrationStep_2_9, MalwareRemediatorMigrationStep_2_10, BlobstoreSecretsMigrationStep_2_11, HuggingFaceProxyDatabaseMigrationStep_2_12, CoordinateMigrationStep_2_13, RemoveDistributedCooperationMigrationStep_2_14, RemoveLog4JVisualizer_2_15, SearchCapabilityStep_2_16, TrustedCertificatesMigrationStep_2_17, NodeHeartBeatMigrationStep_2_17_1, ConanCleanupMigrationStep_2_18, AssetBlobMigrationStep_2_18_1, AssetBlobMigrationStep_2_18_2, FileBlobStoreMetricsMigrationStep_2_19, S3BlobStoreMetricsMigrationStep_2_20, AzureBlobStoreMetricsMigrationStep_2_21, RepairAptMetadataLeadingSlash_2_22, AssetBlobAddedToRepositoryMigrationStep_2_27, ComponentEntityVersionMigrationStep_2_28, Maven2ComponentBaseVersionMigrationStep_2_29, ApiKeyCreatedMigrationStep_2_30, SoftDeletedBlobsDatePathRefMigrationStep_2_31, AssetTableIndexesMigrationStep_2_32, ComponentApplicationScanEvaluationDelayMigrationStep_2_33, AggregatedMetricsNodeIdMigrationStep_2_34, ReconcilePlanDetailsPropertiesMigrationStep_2_35, DistributedAuthTicketCacheRealmNameMigrationStep_2_36, SearchComponentsAdditionalColumnsMigrationStep_2_37, NodeHeartbeatInfoColumnsMigrationStep_2_38, NugetComponentIndexesMigrationStep_2_39, QuartzIndexesMigrationStep_2_40, ApiKeyIndexesMigrationStep_2_41, NexusKeyValueIndexesMigrationStep_2_42, CleanupPolicyIndexMigrationStep_2_43, LoggingOverridesIndexMigrationStep_2_44, UserRoleMappingIndexMigrationStep_2_45, PrivilegeIndexMigrationStep_2_46, SecretsIndexMigrationStep_2_47, SoftDeletedBlobsIndexMigrationStep_2_48, NodeHeartbeatIndexesMigrationStep_2_49, ComponentTableIndexesMigrationStep_2_50, DistributedAuthTicketCacheIndexesMigrationStep_2_51, CacheIndexesMigrationStep_2_52, SearchTableIndexesMigrationStep_2_53, SupportZipInfoIndexesMigrationStep_2_54, DistributedEventIndexesMigrationStep_2_55, AggregatedMetricsIndexesMigrationStep_2_56, MetricsLogIndexesMigrationStep_2_57, RepositoryMetricsIndexesMigrationStep_2_58, ComponentApplicationScanIndexesMigrationStep_2_59, ComponentApplicationScanScheduleIndexesMigrationStep_2_60, ReconcilePlanIndexesMigrationStep_2_61, ReconcilePlanDetailsIndexesMigrationStep_2_62, UserTokenIndexesMigrationStep_2_63, DockerForeignLayersIndexesMigrationStep_2_64, KeyValueIndexesMigrationStep_2_65, BrowseNodeIndexesMigrationStep_2_66, AssetBlobIndexesMigrationStep_2_67, AssetIndexesMigrationStep_2_68, ComponentNormalizedVersionConstraintMigrationStep_2_69, AssetBlobExternalMetadataMigrationStep_2_70, ComponentIndexesMigrationStep_2_71, JobKeyUnificationMigrationStep_2_72, SwiftBrowseNodeIndexMigrationStep_2_73, PrivilegeNxRM2UpgradeStep_2_74, RepositoriesBearerTokenMigrationStep_2_75, RemoveOrphanedSearchRecordsMigrationStep_2_76]
2026-02-12 10:08:01,253-0800 ERROR [FelixStartLevel]  *SYSTEM org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl - Missing migrations: [BrowseNodeMigrationStep_2_3, CustomS3RegionCapabilityMigrationStep_2_4, GoogleBlobStoreMigrationStep_2_5, S3FailoverMigrationStep_2_6, SoftDeletedBlobsByBlobStoreIndexMigrationStep_2_7, ConanV2UpgradeStep_2_8, MalwareRemediatorTaskMigrationStep_2_9, MalwareRemediatorMigrationStep_2_10, BlobstoreSecretsMigrationStep_2_11, HuggingFaceProxyDatabaseMigrationStep_2_12, CoordinateMigrationStep_2_13, RemoveDistributedCooperationMigrationStep_2_14, RemoveLog4JVisualizer_2_15, SearchCapabilityStep_2_16, TrustedCertificatesMigrationStep_2_17, NodeHeartBeatMigrationStep_2_17_1, ConanCleanupMigrationStep_2_18, AssetBlobMigrationStep_2_18_1, AssetBlobMigrationStep_2_18_2, FileBlobStoreMetricsMigrationStep_2_19, S3BlobStoreMetricsMigrationStep_2_20, AzureBlobStoreMetricsMigrationStep_2_21, RepairAptMetadataLeadingSlash_2_22, AssetBlobAddedToRepositoryMigrationStep_2_27, ComponentEntityVersionMigrationStep_2_28, Maven2ComponentBaseVersionMigrationStep_2_29, ApiKeyCreatedMigrationStep_2_30, SoftDeletedBlobsDatePathRefMigrationStep_2_31, AssetTableIndexesMigrationStep_2_32, ComponentApplicationScanEvaluationDelayMigrationStep_2_33, AggregatedMetricsNodeIdMigrationStep_2_34, ReconcilePlanDetailsPropertiesMigrationStep_2_35, DistributedAuthTicketCacheRealmNameMigrationStep_2_36, SearchComponentsAdditionalColumnsMigrationStep_2_37, NodeHeartbeatInfoColumnsMigrationStep_2_38, NugetComponentIndexesMigrationStep_2_39, QuartzIndexesMigrationStep_2_40, ApiKeyIndexesMigrationStep_2_41, NexusKeyValueIndexesMigrationStep_2_42, CleanupPolicyIndexMigrationStep_2_43, LoggingOverridesIndexMigrationStep_2_44, UserRoleMappingIndexMigrationStep_2_45, PrivilegeIndexMigrationStep_2_46, SecretsIndexMigrationStep_2_47, SoftDeletedBlobsIndexMigrationStep_2_48, NodeHeartbeatIndexesMigrationStep_2_49, ComponentTableIndexesMigrationStep_2_50, DistributedAuthTicketCacheIndexesMigrationStep_2_51, CacheIndexesMigrationStep_2_52, SearchTableIndexesMigrationStep_2_53, SupportZipInfoIndexesMigrationStep_2_54, DistributedEventIndexesMigrationStep_2_55, AggregatedMetricsIndexesMigrationStep_2_56, MetricsLogIndexesMigrationStep_2_57, RepositoryMetricsIndexesMigrationStep_2_58, ComponentApplicationScanIndexesMigrationStep_2_59, ComponentApplicationScanScheduleIndexesMigrationStep_2_60, ReconcilePlanIndexesMigrationStep_2_61, ReconcilePlanDetailsIndexesMigrationStep_2_62, UserTokenIndexesMigrationStep_2_63, DockerForeignLayersIndexesMigrationStep_2_64, KeyValueIndexesMigrationStep_2_65, BrowseNodeIndexesMigrationStep_2_66, AssetBlobIndexesMigrationStep_2_67, AssetIndexesMigrationStep_2_68, ComponentNormalizedVersionConstraintMigrationStep_2_69, AssetBlobExternalMetadataMigrationStep_2_70, ComponentIndexesMigrationStep_2_71, JobKeyUnificationMigrationStep_2_72, SwiftBrowseNodeIndexMigrationStep_2_73, PrivilegeNxRM2UpgradeStep_2_74, RepositoriesBearerTokenMigrationStep_2_75, RemoveOrphanedSearchRecordsMigrationStep_2_76]
2026-02-12 10:08:01,255-0800 ERROR [FelixStartLevel]  *SYSTEM org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl - Failed transition: NEW -> STARTED
org.sonatype.nexus.upgrade.datastore.UpgradeException: The database appears to be from a later version of Nexus Repository
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.checkSchemaVersionIsAcceptable(UpgradeManagerImpl.java:204)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:89)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:62)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.MethodInvocationAction.run(MethodInvocationAction.java:39)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:206)
	at org.sonatype.nexus.common.stateguard.TransitionsInterceptor.invoke(TransitionsInterceptor.java:57)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:210)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:121)
	at org.sonatype.nexus.extender.NexusContextListener.moveToPhase(NexusContextListener.java:334)
	at org.sonatype.nexus.extender.NexusContextListener.frameworkEvent(NexusContextListener.java:231)
	at org.apache.felix.framework.Felix.setActiveStartLevel(Felix.java:1597)
	at org.apache.felix.framework.FrameworkStartLevelImpl.run(FrameworkStartLevelImpl.java:308)
	at java.base/java.lang.Thread.run(Thread.java:840)
2026-02-12 10:08:01,256-0800 ERROR [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusContextListener - Failed to start nexus
org.sonatype.nexus.upgrade.datastore.UpgradeException: The database appears to be from a later version of Nexus Repository
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.checkSchemaVersionIsAcceptable(UpgradeManagerImpl.java:204)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:89)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:62)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.MethodInvocationAction.run(MethodInvocationAction.java:39)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:206)
	at org.sonatype.nexus.common.stateguard.TransitionsInterceptor.invoke(TransitionsInterceptor.java:57)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:210)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:121)
	at org.sonatype.nexus.extender.NexusContextListener.moveToPhase(NexusContextListener.java:334)
	at org.sonatype.nexus.extender.NexusContextListener.frameworkEvent(NexusContextListener.java:231)
	at org.apache.felix.framework.Felix.setActiveStartLevel(Felix.java:1597)
	at org.apache.felix.framework.FrameworkStartLevelImpl.run(FrameworkStartLevelImpl.java:308)
	at java.base/java.lang.Thread.run(Thread.java:840)
2026-02-12 10:08:01,257-0800 ERROR [FelixStartLevel]  *SYSTEM Felix - Framework listener delivery error.
java.lang.RuntimeException: org.sonatype.nexus.upgrade.datastore.UpgradeException: The database appears to be from a later version of Nexus Repository
	at org.sonatype.nexus.extender.NexusContextListener.frameworkEvent(NexusContextListener.java:243)
	at org.apache.felix.framework.Felix.setActiveStartLevel(Felix.java:1597)
	at org.apache.felix.framework.FrameworkStartLevelImpl.run(FrameworkStartLevelImpl.java:308)
	at java.base/java.lang.Thread.run(Thread.java:840)
Caused by: org.sonatype.nexus.upgrade.datastore.UpgradeException: The database appears to be from a later version of Nexus Repository
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.checkSchemaVersionIsAcceptable(UpgradeManagerImpl.java:204)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:89)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:62)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.MethodInvocationAction.run(MethodInvocationAction.java:39)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:206)
	at org.sonatype.nexus.common.stateguard.TransitionsInterceptor.invoke(TransitionsInterceptor.java:57)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:210)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:121)
	at org.sonatype.nexus.extender.NexusContextListener.moveToPhase(NexusContextListener.java:334)
	at org.sonatype.nexus.extender.NexusContextListener.frameworkEvent(NexusContextListener.java:231)
	... 3 common frames omitted
2026-02-12 10:08:01,271-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusContextListener - Uptime: 31 seconds and 557 milliseconds (nexus-pro-edition/3.73.0.12)
2026-02-12 10:08:01,272-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Shutting down
2026-02-12 10:08:01,279-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop RESTORE
2026-02-12 10:08:01,280-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop STORAGE
2026-02-12 10:08:01,306-0800 INFO  [FelixStartLevel]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Shutdown initiated...
2026-02-12 10:08:01,372-0800 INFO  [FelixStartLevel]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Shutdown completed.
2026-02-12 10:08:01,372-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop KERNEL
2026-02-12 10:11:38,760-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.pax.logging.NexusLogActivator - start
2026-02-12 10:11:38,944-0800 WARN  [FelixStartLevel]  *SYSTEM javax.xml.bind - Using non-standard property: javax.xml.bind.JAXBContext. Property javax.xml.bind.JAXBContextFactory should be used instead.
2026-02-12 10:11:39,091-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.features.internal.FeaturesWrapper - Fast FeaturesService starting
2026-02-12 10:11:39,195-0800 WARN  [FelixStartLevel]  *SYSTEM javax.xml.bind - Using non-standard property: javax.xml.bind.JAXBContext. Property javax.xml.bind.JAXBContextFactory should be used instead.
2026-02-12 10:11:39,923-0800 INFO  [FelixStartLevel]  *SYSTEM ROOT - bundle org.apache.felix.scr:2.1.30 (56) Starting with globalExtender setting: false
2026-02-12 10:11:39,928-0800 INFO  [FelixStartLevel]  *SYSTEM ROOT - bundle org.apache.felix.scr:2.1.30 (56)  Version = 2.1.30
2026-02-12 10:11:40,154-0800 WARN  [FelixStartLevel]  *SYSTEM uk.org.lidalia.sysoutslf4j.context.SysOutOverSLF4JInitialiser - Your logging framework class org.ops4j.pax.logging.slf4j.Slf4jLogger is not known - if it needs access to the standard println methods on the console you will need to register it by calling registerLoggingSystemPackage
2026-02-12 10:11:40,155-0800 INFO  [FelixStartLevel]  *SYSTEM uk.org.lidalia.sysoutslf4j.context.SysOutOverSLF4J - Package org.ops4j.pax.logging.slf4j registered; all classes within it or subpackages of it will be allowed to print to System.out and System.err
2026-02-12 10:11:40,158-0800 INFO  [FelixStartLevel]  *SYSTEM uk.org.lidalia.sysoutslf4j.context.SysOutOverSLF4J - Replaced standard System.out and System.err PrintStreams with SLF4JPrintStreams
2026-02-12 10:11:40,159-0800 INFO  [FelixStartLevel]  *SYSTEM uk.org.lidalia.sysoutslf4j.context.SysOutOverSLF4J - Redirected System.out and System.err to SLF4J for this context
2026-02-12 10:11:40,163-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder - Properties:
2026-02-12 10:11:40,164-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   application-host='0.0.0.0'
2026-02-12 10:11:40,164-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   application-port='8081'
2026-02-12 10:11:40,164-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   application-port-ssl='8444'
2026-02-12 10:11:40,165-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   fabric.etc='/opt/appdata/nexus/nexus-3.70.1-02/etc/fabric'
2026-02-12 10:11:40,165-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   jetty.etc='/opt/appdata/nexus/nexus-3.70.1-02/etc/jetty'
2026-02-12 10:11:40,165-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   karaf.base='/opt/appdata/nexus/nexus-3.70.1-02'
2026-02-12 10:11:40,165-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   karaf.data='/opt/appdata/nexus/sonatype-work/nexus3'
2026-02-12 10:11:40,165-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   karaf.etc='/opt/appdata/nexus/nexus-3.70.1-02/etc/karaf'
2026-02-12 10:11:40,166-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   karaf.home='/opt/appdata/nexus/nexus-3.70.1-02'
2026-02-12 10:11:40,166-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   karaf.instances='/opt/appdata/nexus/sonatype-work/nexus3/instances'
2026-02-12 10:11:40,166-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   logback.etc='/opt/appdata/nexus/nexus-3.70.1-02/etc/logback'
2026-02-12 10:11:40,166-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus-args='/opt/appdata/nexus/nexus-3.70.1-02/etc/jetty/jetty.xml,/opt/appdata/nexus/nexus-3.70.1-02/etc/jetty/jetty-https.xml,/opt/appdata/nexus/nexus-3.70.1-02/etc/jetty/jetty-requestlog.xml'
2026-02-12 10:11:40,166-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus-context-path='/'
2026-02-12 10:11:40,167-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus-edition='nexus-pro-edition'
2026-02-12 10:11:40,167-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus-features='nexus-pro-feature'
2026-02-12 10:11:40,167-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus.assetdownloads.enabled='true'
2026-02-12 10:11:40,167-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus.datastore.enabled='true'
2026-02-12 10:11:40,167-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus.hazelcast.discovery.isEnabled='true'
2026-02-12 10:11:40,168-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus.scripts.allowCreation='true'
2026-02-12 10:11:40,168-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   nexus.view.exhaustForAgents='Apache-Maven.*|libwww-perl.*'
2026-02-12 10:11:40,169-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   org.sonatype.nexus.repository.httpbridge.internal.HttpBridgeModule.legacy='true'
2026-02-12 10:11:40,169-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.ConfigurationBuilder -   ssl.etc='/opt/appdata/nexus/sonatype-work/nexus3/etc/ssl'
2026-02-12 10:11:40,169-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.Launcher - Java: 17.0.17, OpenJDK 64-Bit Server VM, Red Hat, Inc., 17.0.17+10-LTS
2026-02-12 10:11:40,170-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.Launcher - OS: Linux, 4.18.0-553.89.1.el8_10.x86_64, amd64
2026-02-12 10:11:40,170-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.Launcher - User: nexus, en, /home/nexus
2026-02-12 10:11:40,170-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.Launcher - CWD: /opt/appdata/nexus/nexus-3.70.1-02
2026-02-12 10:11:40,172-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.Launcher - TMP: /opt/appdata/nexus/sonatype-work/nexus3/tmp
2026-02-12 10:11:40,176-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.jetty.JettyServer - Starting
2026-02-12 10:11:40,182-0800 INFO  [FelixStartLevel]  *SYSTEM org.eclipse.jetty.util.log - Logging initialized @3350ms to org.eclipse.jetty.util.log.Slf4jLog
2026-02-12 10:11:40,185-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.jetty.JettyServer - Applying configuration: file:/opt/appdata/nexus/nexus-3.70.1-02/etc/jetty/jetty.xml
2026-02-12 10:11:40,324-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.jetty.JettyServer - Applying configuration: file:/opt/appdata/nexus/nexus-3.70.1-02/etc/jetty/jetty-https.xml
2026-02-12 10:11:40,387-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.bootstrap.jetty.JettyServer - Applying configuration: file:/opt/appdata/nexus/nexus-3.70.1-02/etc/jetty/jetty-requestlog.xml
2026-02-12 10:11:40,406-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.jetty.JettyServer - Starting: Server@2e41e5ca{STOPPED}[9.4.53.v20231009]
2026-02-12 10:11:40,409-0800 INFO  [jetty-main-1]  *SYSTEM org.eclipse.jetty.server.Server - jetty-9.4.53.v20231009; built: 2023-10-09T12:29:09.265Z; git: 27bde00a0b95a1d5bbee0eae7984f891d2d0f8c9; jvm 17.0.17+10-LTS
2026-02-12 10:11:40,474-0800 INFO  [jetty-main-1]  *SYSTEM org.eclipse.jetty.server.session - DefaultSessionIdManager workerName=node0
2026-02-12 10:11:40,474-0800 INFO  [jetty-main-1]  *SYSTEM org.eclipse.jetty.server.session - No SessionScavenger set, using defaults
2026-02-12 10:11:40,475-0800 INFO  [jetty-main-1]  *SYSTEM org.eclipse.jetty.server.session - node0 Scavenging every 600000ms
2026-02-12 10:11:40,485-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.osgi.BootstrapListener - Initializing
2026-02-12 10:11:40,492-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.osgi.ProNexusEdition - Loading Pro Edition
2026-02-12 10:11:40,493-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.osgi.BootstrapListener - Installing: nexus-pro-edition/3.70.1.02 (nexus-datastore-mybatis/3.70.1.02)
2026-02-12 10:11:43,468-0800 INFO  [jetty-main-1]  *SYSTEM org.ehcache.core.osgi.EhcacheActivator - Detected OSGi Environment (core is in bundle: org.ehcache [152]): Using OSGi Based Service Loading
2026-02-12 10:11:44,313-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.bootstrap.osgi.BootstrapListener - Installed: nexus-pro-edition/3.70.1.02 (nexus-datastore-mybatis/3.70.1.02)
2026-02-12 10:11:44,735-0800 INFO  [jetty-main-1]  *SYSTEM org.apache.shiro.nexus.NexusWebSessionManager - Global session timeout: 1800000 ms
2026-02-12 10:11:44,736-0800 INFO  [jetty-main-1]  *SYSTEM org.apache.shiro.nexus.NexusWebSessionManager - Session-cookie prototype: name=NXSESSIONID, secure=true
2026-02-12 10:11:44,760-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.common [3.70.1.02]
2026-02-12 10:11:44,871-0800 INFO  [jetty-main-1]  *SYSTEM org.hibernate.validator.internal.util.Version - HV000001: Hibernate Validator 6.2.0.Final
2026-02-12 10:11:45,039-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.common [3.70.1.02]
2026-02-12 10:11:45,040-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.hibernate.validator [6.2.0.Final]
2026-02-12 10:11:45,102-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.hibernate.validator [6.2.0.Final]
2026-02-12 10:11:45,103-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.blobstore-api [3.70.1.02]
2026-02-12 10:11:45,130-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.blobstore-api [3.70.1.02]
2026-02-12 10:11:45,131-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.cache [3.70.1.02]
2026-02-12 10:11:45,191-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.cache [3.70.1.02]
2026-02-12 10:11:45,192-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.jmx [3.70.1.02]
2026-02-12 10:11:45,211-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.jmx [3.70.1.02]
2026-02-12 10:11:45,214-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.crypto [3.70.1.02]
2026-02-12 10:11:45,325-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.crypto [3.70.1.02]
2026-02-12 10:11:45,326-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.security [3.70.1.02]
2026-02-12 10:11:45,517-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.security [3.70.1.02]
2026-02-12 10:11:45,517-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.datastore [3.70.1.02]
2026-02-12 10:11:45,555-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.datastore [3.70.1.02]
2026-02-12 10:11:45,555-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.supportzip-api [3.70.1.02]
2026-02-12 10:11:45,590-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.supportzip-api [3.70.1.02]
2026-02-12 10:11:45,591-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.thread [3.70.1.02]
2026-02-12 10:11:45,608-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.thread [3.70.1.02]
2026-02-12 10:11:45,609-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.scheduling [3.70.1.02]
2026-02-12 10:11:45,667-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.scheduling [3.70.1.02]
2026-02-12 10:11:45,667-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.blobstore [3.70.1.02]
2026-02-12 10:11:45,714-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.blobstore [3.70.1.02]
2026-02-12 10:11:45,715-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.apache.tika.core [1.28.4]
2026-02-12 10:11:45,732-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.apache.tika.core [1.28.4]
2026-02-12 10:11:45,736-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.upgrade [3.70.1.02]
2026-02-12 10:11:45,768-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.upgrade [3.70.1.02]
2026-02-12 10:11:45,769-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.blobstore-file [3.70.1.02]
2026-02-12 10:11:45,817-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.blobstore-file [3.70.1.02]
2026-02-12 10:11:45,817-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.capability [3.70.1.02]
2026-02-12 10:11:45,837-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.capability [3.70.1.02]
2026-02-12 10:11:45,838-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.commands [3.70.1.02]
2026-02-12 10:11:45,852-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.commands [3.70.1.02]
2026-02-12 10:11:45,852-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.email [3.70.1.02]
2026-02-12 10:11:45,864-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.email [3.70.1.02]
2026-02-12 10:11:45,864-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.httpclient [3.70.1.02]
2026-02-12 10:11:45,881-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.httpclient [3.70.1.02]
2026-02-12 10:11:45,881-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.servlet [3.70.1.02]
2026-02-12 10:11:45,892-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.servlet [3.70.1.02]
2026-02-12 10:11:45,893-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.ssl [3.70.1.02]
2026-02-12 10:11:45,905-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.ssl [3.70.1.02]
2026-02-12 10:11:45,905-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.base [3.70.1.02]
2026-02-12 10:11:46,051-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.internal.metrics.MetricsModule - Metrics support configured
2026-02-12 10:11:46,075-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.internal.metrics.MetricsModule - Metrics support configured
2026-02-12 10:11:46,298-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.base [3.70.1.02]
2026-02-12 10:11:46,299-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.extdirect [3.70.1.02]
2026-02-12 10:11:46,338-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.extdirect [3.70.1.02]
2026-02-12 10:11:46,339-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.siesta [3.70.1.02]
2026-02-12 10:11:46,391-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.siesta [3.70.1.02]
2026-02-12 10:11:46,391-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.rest-jackson2 [3.70.1.02]
2026-02-12 10:11:46,402-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.rest-jackson2 [3.70.1.02]
2026-02-12 10:11:46,403-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.swagger [3.70.1.02]
2026-02-12 10:11:46,424-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.swagger [3.70.1.02]
2026-02-12 10:11:46,425-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.rapture [3.70.1.02]
2026-02-12 10:11:46,522-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.rapture [3.70.1.02]
2026-02-12 10:11:46,523-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.datastore-mybatis [3.70.1.02]
2026-02-12 10:11:46,552-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.datastore-mybatis [3.70.1.02]
2026-02-12 10:11:46,552-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.quartz [3.70.1.02]
2026-02-12 10:11:46,590-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.quartz [3.70.1.02]
2026-02-12 10:11:46,591-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING wrap_file_system_com_sonatype_licensing_license-bundle_1.6.0_license-bundle-1.6.0.jar [0.0.0]
2026-02-12 10:11:46,624-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED wrap_file_system_com_sonatype_licensing_license-bundle_1.6.0_license-bundle-1.6.0.jar [0.0.0]
2026-02-12 10:11:46,624-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.licensing-extension [3.70.1.02]
2026-02-12 10:11:46,654-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.licensing-extension [3.70.1.02]
2026-02-12 10:11:46,655-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.pro-edition [3.70.1.02]
2026-02-12 10:11:46,667-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.pro-edition [3.70.1.02]
2026-02-12 10:11:46,669-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusContextListener - Running lifecycle phases [KERNEL, STORAGE, RESTORE, UPGRADE, SCHEMAS, EVENTS, SECURITY, SERVICES, REPOSITORIES, CAPABILITIES, TASKS]
2026-02-12 10:11:46,669-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start KERNEL
2026-02-12 10:11:46,733-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.internal.log.overrides.file.LogbackLoggerOverrides - File: /opt/appdata/nexus/sonatype-work/nexus3/etc/logback/logback-overrides.xml
2026-02-12 10:11:46,735-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.internal.log.LogbackLogManager - Configuring
2026-02-12 10:11:46,750-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusContextListener - Installing: [nexus-pro-feature/3.70.1.02, nexus-datastore-mybatis/3.70.1.02, nexus-group-deploy/3.70.1.02]
2026-02-12 10:11:53,439-0800 INFO  [jetty-main-1]  *SYSTEM org.sonatype.nexus.extender.NexusContextListener - Installed: [nexus-pro-feature/3.70.1.02, nexus-datastore-mybatis/3.70.1.02, nexus-group-deploy/3.70.1.02]
2026-02-12 10:11:53,459-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-audit-plugin [3.70.1.02]
2026-02-12 10:11:53,478-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-audit-plugin [3.70.1.02]
2026-02-12 10:11:53,493-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-ssl-plugin [3.70.1.02]
2026-02-12 10:11:53,525-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-ssl-plugin [3.70.1.02]
2026-02-12 10:11:53,623-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.selector [3.70.1.02]
2026-02-12 10:11:53,650-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.selector [3.70.1.02]
2026-02-12 10:11:53,654-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.elasticsearch [3.70.1.02]
2026-02-12 10:11:53,672-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.elasticsearch [3.70.1.02]
2026-02-12 10:11:53,673-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.repository-content [3.70.1.02]
2026-02-12 10:11:53,967-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.repository-content [3.70.1.02]
2026-02-12 10:11:53,971-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.repository-config [3.70.1.02]
2026-02-12 10:11:54,007-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.repository-config [3.70.1.02]
2026-02-12 10:11:54,009-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-coreui-plugin [3.70.1.02]
2026-02-12 10:11:54,116-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-coreui-plugin [3.70.1.02]
2026-02-12 10:11:54,130-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-repository-httpbridge [3.70.1.02]
2026-02-12 10:11:54,154-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-repository-httpbridge [3.70.1.02]
2026-02-12 10:11:54,207-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-blobstore-tasks [3.70.1.02]
2026-02-12 10:11:54,230-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-blobstore-tasks [3.70.1.02]
2026-02-12 10:11:54,231-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.cleanup-config [3.70.1.02]
2026-02-12 10:11:54,253-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.cleanup-config [3.70.1.02]
2026-02-12 10:11:54,254-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.core [3.70.1.02]
2026-02-12 10:11:54,432-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.core [3.70.1.02]
2026-02-12 10:11:54,434-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-repository-maven [3.70.1.02]
2026-02-12 10:11:54,637-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-repository-maven [3.70.1.02]
2026-02-12 10:11:54,638-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-script-plugin [3.70.1.02]
2026-02-12 10:11:54,673-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-script-plugin [3.70.1.02]
2026-02-12 10:11:54,688-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-task-log-cleanup [3.70.1.02]
2026-02-12 10:11:54,700-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-task-log-cleanup [3.70.1.02]
2026-02-12 10:11:54,746-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-blobstore-s3 [3.70.1.02]
2026-02-12 10:11:54,998-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-blobstore-s3 [3.70.1.02]
2026-02-12 10:11:55,013-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-onboarding-plugin [3.70.1.02]
2026-02-12 10:11:55,033-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-onboarding-plugin [3.70.1.02]
2026-02-12 10:11:55,041-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-default-role-plugin [3.70.1.02]
2026-02-12 10:11:55,055-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-default-role-plugin [3.70.1.02]
2026-02-12 10:11:55,071-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-repository-apt [3.70.1.02]
2026-02-12 10:11:55,146-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-repository-apt [3.70.1.02]
2026-02-12 10:11:55,186-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.plugins.nexus-repository-raw [3.70.1.02]
2026-02-12 10:11:55,236-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.plugins.nexus-repository-raw [3.70.1.02]
2026-02-12 10:11:55,260-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.cleanup [3.70.1.02]
2026-02-12 10:11:55,285-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.cleanup [3.70.1.02]
2026-02-12 10:11:55,308-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-ldap-plugin [3.70.1.02]
2026-02-12 10:11:55,351-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-ldap-plugin [3.70.1.02]
2026-02-12 10:11:55,379-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-tags-plugin [3.70.1.02]
2026-02-12 10:11:55,445-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-tags-plugin [3.70.1.02]
2026-02-12 10:11:55,447-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-proui-plugin [3.70.1.02]
2026-02-12 10:11:55,461-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-proui-plugin [3.70.1.02]
2026-02-12 10:11:55,469-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-proximanova-plugin [3.70.1.02]
2026-02-12 10:11:55,477-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-proximanova-plugin [3.70.1.02]
2026-02-12 10:11:55,525-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING wrap_file_system_com_sonatype_insight_scan_insight-scanner-core_2.36.66-01_insight-scanner-core-2.36.66-01.jar [0.0.0]
2026-02-12 10:11:55,536-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED wrap_file_system_com_sonatype_insight_scan_insight-scanner-core_2.36.66-01_insight-scanner-core-2.36.66-01.jar [0.0.0]
2026-02-12 10:11:55,539-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING wrap_file_system_com_sonatype_insight_scan_insight-scanner-model-io_2.36.66-01_insight-scanner-model-io-2.36.66-01.jar [0.0.0]
2026-02-12 10:11:55,551-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED wrap_file_system_com_sonatype_insight_scan_insight-scanner-model-io_2.36.66-01_insight-scanner-model-io-2.36.66-01.jar [0.0.0]
2026-02-12 10:11:55,552-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-healthcheck-base [3.70.1.02]
2026-02-12 10:11:56,352-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-healthcheck-base [3.70.1.02]
2026-02-12 10:11:56,353-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-analytics-plugin [3.70.1.02]
2026-02-12 10:11:56,440-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-analytics-plugin [3.70.1.02]
2026-02-12 10:11:56,441-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-licensing-plugin [3.70.1.02]
2026-02-12 10:11:56,464-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-licensing-plugin [3.70.1.02]
2026-02-12 10:11:56,515-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-crowd-plugin [3.70.1.02]
2026-02-12 10:11:56,556-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-crowd-plugin [3.70.1.02]
2026-02-12 10:11:56,559-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-npm [3.70.1.02]
2026-02-12 10:11:56,682-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-npm [3.70.1.02]
2026-02-12 10:11:56,684-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-nuget [3.70.1.02]
2026-02-12 10:11:56,855-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-nuget [3.70.1.02]
2026-02-12 10:11:56,856-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-usertoken-plugin [3.70.1.02]
2026-02-12 10:11:56,905-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-usertoken-plugin [3.70.1.02]
2026-02-12 10:11:56,907-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-rubygems [3.70.1.02]
2026-02-12 10:11:56,983-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-rubygems [3.70.1.02]
2026-02-12 10:11:56,986-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING org.sonatype.nexus.rest-client [3.70.1.02]
2026-02-12 10:11:56,995-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED org.sonatype.nexus.rest-client [3.70.1.02]
2026-02-12 10:11:56,998-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-migration-plugin [3.70.1.02]
2026-02-12 10:11:57,119-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-migration-plugin [3.70.1.02]
2026-02-12 10:11:57,176-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-vulnerability-plugin [3.70.1.02]
2026-02-12 10:11:57,218-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-vulnerability-plugin [3.70.1.02]
2026-02-12 10:11:57,219-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-outreach-plugin [3.70.1.02]
2026-02-12 10:11:57,249-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-outreach-plugin [3.70.1.02]
2026-02-12 10:11:57,260-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-rutauth-plugin [3.70.1.02]
2026-02-12 10:11:57,273-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-rutauth-plugin [3.70.1.02]
2026-02-12 10:11:57,295-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-yum [3.70.1.02]
2026-02-12 10:11:57,390-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-yum [3.70.1.02]
2026-02-12 10:11:57,416-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-group-deploy [3.70.1.02]
2026-02-12 10:11:57,428-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-group-deploy [3.70.1.02]
2026-02-12 10:11:57,429-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-docker [3.70.1.02]
2026-02-12 10:11:57,601-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-docker [3.70.1.02]
2026-02-12 10:11:57,624-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-ahc-plugin [3.70.1.02]
2026-02-12 10:11:57,665-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-ahc-plugin [3.70.1.02]
2026-02-12 10:11:57,757-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-pypi [3.70.1.02]
2026-02-12 10:11:57,843-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-pypi [3.70.1.02]
2026-02-12 10:11:57,857-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-conda [3.70.1.02]
2026-02-12 10:11:57,886-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-conda [3.70.1.02]
2026-02-12 10:11:57,901-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-conan [3.70.1.02]
2026-02-12 10:11:57,966-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-conan [3.70.1.02]
2026-02-12 10:11:57,980-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-gitlfs [3.70.1.02]
2026-02-12 10:11:58,013-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-gitlfs [3.70.1.02]
2026-02-12 10:11:58,028-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-r [3.70.1.02]
2026-02-12 10:11:58,073-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-r [3.70.1.02]
2026-02-12 10:11:58,099-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-blobstore-group [3.70.1.02]
2026-02-12 10:11:58,118-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-blobstore-group [3.70.1.02]
2026-02-12 10:11:58,119-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-move-plugin [3.70.1.02]
2026-02-12 10:11:58,139-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-move-plugin [3.70.1.02]
2026-02-12 10:11:58,140-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-replication-plugin [3.70.1.02]
2026-02-12 10:11:58,174-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-replication-plugin [3.70.1.02]
2026-02-12 10:11:58,192-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-cocoapods [3.70.1.02]
2026-02-12 10:11:58,222-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-cocoapods [3.70.1.02]
2026-02-12 10:11:58,237-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-golang [3.70.1.02]
2026-02-12 10:11:58,275-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-golang [3.70.1.02]
2026-02-12 10:11:58,290-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-p2 [3.70.1.02]
2026-02-12 10:11:58,328-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-p2 [3.70.1.02]
2026-02-12 10:11:58,344-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-cleanup-pro-plugin [3.70.1.02]
2026-02-12 10:11:58,357-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-cleanup-pro-plugin [3.70.1.02]
2026-02-12 10:11:58,375-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-clm-plugin [3.70.1.02]
2026-02-12 10:11:58,407-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-clm-plugin [3.70.1.02]
2026-02-12 10:11:58,419-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-staging-plugin [3.70.1.02]
2026-02-12 10:11:58,439-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-staging-plugin [3.70.1.02]
2026-02-12 10:11:58,442-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING nexus-blobstore-azure-cloud [3.70.1.02]
2026-02-12 10:11:58,479-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED nexus-blobstore-azure-cloud [3.70.1.02]
2026-02-12 10:11:58,506-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-pro-system-checks-plugin [3.70.1.02]
2026-02-12 10:11:58,532-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-pro-system-checks-plugin [3.70.1.02]
2026-02-12 10:11:58,561-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-saml-plugin [3.70.1.02]
2026-02-12 10:11:58,729-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-saml-plugin [3.70.1.02]
2026-02-12 10:11:58,740-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-export-import-plugin [3.70.1.02]
2026-02-12 10:11:58,808-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-export-import-plugin [3.70.1.02]
2026-02-12 10:11:58,820-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-pro-datastore-plugin [3.70.1.02]
2026-02-12 10:11:58,876-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-pro-datastore-plugin [3.70.1.02]
2026-02-12 10:11:58,891-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-repository-helm [3.70.1.02]
2026-02-12 10:11:58,952-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-repository-helm [3.70.1.02]
2026-02-12 10:11:58,966-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATING com.sonatype.nexus.plugins.nexus-api-extension-plugin [3.70.1.02]
2026-02-12 10:11:58,986-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusBundleTracker - ACTIVATED com.sonatype.nexus.plugins.nexus-api-extension-plugin [3.70.1.02]
2026-02-12 10:11:58,987-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start STORAGE
2026-02-12 10:11:59,014-0800 INFO  [FelixStartLevel]  *SYSTEM com.sonatype.nexus.datastore.DataStoreConfigurationFileSource - Loaded 'nexus' data store configuration from properties file (postgresql)
2026-02-12 10:11:59,199-0800 INFO  [FelixStartLevel]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Starting...
2026-02-12 10:11:59,281-0800 INFO  [FelixStartLevel]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Start completed.
2026-02-12 10:11:59,282-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Loading MyBatis configuration from /opt/appdata/nexus/nexus-3.70.1-02/etc/fabric/mybatis.xml
2026-02-12 10:11:59,355-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - MyBatis databaseId: PostgreSQL
2026-02-12 10:11:59,472-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for UpgradeTaskDAO
2026-02-12 10:11:59,517-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SoftDeletedBlobsDAO
2026-02-12 10:11:59,572-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for JwtSecretDAO
2026-02-12 10:11:59,592-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for LoggingOverridesDAO
2026-02-12 10:11:59,619-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DeploymentIdDAO
2026-02-12 10:11:59,634-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NodeIdDAO
2026-02-12 10:11:59,650-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AnonymousConfigurationDAO
2026-02-12 10:11:59,671-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CPrivilegeDAO
2026-02-12 10:11:59,701-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CRoleDAO
2026-02-12 10:11:59,717-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CUserDAO
2026-02-12 10:11:59,734-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CUserRoleMappingDAO
2026-02-12 10:11:59,763-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RealmConfigurationDAO
2026-02-12 10:11:59,783-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for QuartzDAO
2026-02-12 10:11:59,836-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for KeyStoreDAO
2026-02-12 10:11:59,854-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for BlobStoreMetricsDAO
2026-02-12 10:11:59,868-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NexusKeyValueDAO
2026-02-12 10:11:59,895-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConfigurationDAO
2026-02-12 10:11:59,913-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for BlobStoreConfigurationDAO
2026-02-12 10:11:59,929-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RoutingRuleDAO
2026-02-12 10:11:59,944-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CleanupPolicyDAO
2026-02-12 10:11:59,971-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CapabilityStorageItemDAO
2026-02-12 10:11:59,987-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for EmailConfigurationDAO
2026-02-12 10:12:00,001-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HttpClientConfigurationDAO
2026-02-12 10:12:00,026-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ApiKeyDAO
2026-02-12 10:12:00,056-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SelectorConfigurationDAO
2026-02-12 10:12:00,082-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2ContentRepositoryDAO
2026-02-12 10:12:00,121-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2ComponentDAO
2026-02-12 10:12:00,182-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2AssetBlobDAO
2026-02-12 10:12:00,239-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2AssetDAO
2026-02-12 10:12:00,277-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2BrowseNodeDAO
2026-02-12 10:12:00,305-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ScriptDAO
2026-02-12 10:12:00,315-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptContentRepositoryDAO
2026-02-12 10:12:00,339-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptKeyValueDAO
2026-02-12 10:12:00,370-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptComponentDAO
2026-02-12 10:12:00,409-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptAssetBlobDAO
2026-02-12 10:12:00,455-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptAssetDAO
2026-02-12 10:12:00,495-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptBrowseNodeDAO
2026-02-12 10:12:00,519-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawContentRepositoryDAO
2026-02-12 10:12:00,579-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawComponentDAO
2026-02-12 10:12:00,616-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawAssetBlobDAO
2026-02-12 10:12:00,665-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawAssetDAO
2026-02-12 10:12:00,701-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawBrowseNodeDAO
2026-02-12 10:12:00,725-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for LdapConfigurationDAO
2026-02-12 10:12:00,739-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for TagDAO
2026-02-12 10:12:00,764-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AptComponentTagDAO
2026-02-12 10:12:00,780-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsComponentTagDAO
2026-02-12 10:12:00,797-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanComponentTagDAO
2026-02-12 10:12:00,813-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaComponentTagDAO
2026-02-12 10:12:00,829-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerComponentTagDAO
2026-02-12 10:12:00,845-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsComponentTagDAO
2026-02-12 10:12:00,861-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoComponentTagDAO
2026-02-12 10:12:00,877-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmComponentTagDAO
2026-02-12 10:12:00,893-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Maven2ComponentTagDAO
2026-02-12 10:12:00,908-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmComponentTagDAO
2026-02-12 10:12:00,924-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetComponentTagDAO
2026-02-12 10:12:00,939-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2ComponentTagDAO
2026-02-12 10:12:00,955-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiComponentTagDAO
2026-02-12 10:12:00,970-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RComponentTagDAO
2026-02-12 10:12:00,986-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RawComponentTagDAO
2026-02-12 10:12:01,001-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsComponentTagDAO
2026-02-12 10:12:01,018-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumComponentTagDAO
2026-02-12 10:12:01,029-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for FirewallIgnorePatternsDAO
2026-02-12 10:12:01,040-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RepositoryHealthCheckConfigurationDAO
2026-02-12 10:12:01,054-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for AggregatedMetricsDAO
2026-02-12 10:12:01,086-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HistoricalLoginInfoDAO
2026-02-12 10:12:01,114-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for MetricDAO
2026-02-12 10:12:01,137-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmContentRepositoryDAO
2026-02-12 10:12:01,169-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmComponentDAO
2026-02-12 10:12:01,209-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmAssetBlobDAO
2026-02-12 10:12:01,250-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmAssetDAO
2026-02-12 10:12:01,294-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NpmBrowseNodeDAO
2026-02-12 10:12:01,328-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetAssetBlobDAO
2026-02-12 10:12:01,362-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetContentRepositoryDAO
2026-02-12 10:12:01,376-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetComponentDAO
2026-02-12 10:12:01,415-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetAssetDAO
2026-02-12 10:12:01,446-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NugetBrowseNodeDAO
2026-02-12 10:12:01,472-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for UserTokenRecordDAO
2026-02-12 10:12:01,493-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsContentRepositoryDAO
2026-02-12 10:12:01,507-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsComponentDAO
2026-02-12 10:12:01,546-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsAssetBlobDAO
2026-02-12 10:12:01,605-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsAssetDAO
2026-02-12 10:12:01,638-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsBrowseNodeDAO
2026-02-12 10:12:01,663-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RubygemsComponentDAO
2026-02-12 10:12:01,704-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DownloadCountDAO
2026-02-12 10:12:01,730-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for Log4JVisualizerConfigurationDAO
2026-02-12 10:12:01,739-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumContentRepositoryDAO
2026-02-12 10:12:01,767-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumComponentDAO
2026-02-12 10:12:01,799-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumKeyValueDAO
2026-02-12 10:12:01,821-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumAssetBlobDAO
2026-02-12 10:12:01,862-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumAssetDAO
2026-02-12 10:12:01,895-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for YumBrowseNodeDAO
2026-02-12 10:12:01,929-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerAssetBlobDAO
2026-02-12 10:12:01,962-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerContentRepositoryDAO
2026-02-12 10:12:01,978-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerComponentDAO
2026-02-12 10:12:02,023-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerAssetDAO
2026-02-12 10:12:02,059-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerBrowseNodeDAO
2026-02-12 10:12:02,089-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DockerForeignLayersDAO
2026-02-12 10:12:02,121-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComponentApplicationScanDAO
2026-02-12 10:12:02,172-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ComponentApplicationScanScheduleDAO
2026-02-12 10:12:02,219-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiContentRepositoryDAO
2026-02-12 10:12:02,238-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiComponentDAO
2026-02-12 10:12:02,295-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiAssetBlobDAO
2026-02-12 10:12:02,362-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiAssetDAO
2026-02-12 10:12:02,466-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for PypiBrowseNodeDAO
2026-02-12 10:12:02,485-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaContentRepositoryDAO
2026-02-12 10:12:02,498-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaComponentDAO
2026-02-12 10:12:02,539-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaAssetBlobDAO
2026-02-12 10:12:02,590-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaAssetDAO
2026-02-12 10:12:02,625-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CondaBrowseNodeDAO
2026-02-12 10:12:02,659-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanAssetBlobDAO
2026-02-12 10:12:02,695-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanContentRepositoryDAO
2026-02-12 10:12:02,707-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanComponentDAO
2026-02-12 10:12:02,746-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanAssetDAO
2026-02-12 10:12:02,779-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ConanBrowseNodeDAO
2026-02-12 10:12:02,809-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsContentRepositoryDAO
2026-02-12 10:12:02,823-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsComponentDAO
2026-02-12 10:12:02,858-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsAssetBlobDAO
2026-02-12 10:12:02,896-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsAssetDAO
2026-02-12 10:12:02,929-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GitLfsBrowseNodeDAO
2026-02-12 10:12:02,949-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RContentRepositoryDAO
2026-02-12 10:12:02,964-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RComponentDAO
2026-02-12 10:12:02,999-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RAssetBlobDAO
2026-02-12 10:12:03,039-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RAssetDAO
2026-02-12 10:12:03,071-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RBrowseNodeDAO
2026-02-12 10:12:03,098-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ChangeRepositoryBlobstoreDAO
2026-02-12 10:12:03,113-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for ReplicationConnectionDAO
2026-02-12 10:12:03,122-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsContentRepositoryDAO
2026-02-12 10:12:03,137-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsComponentDAO
2026-02-12 10:12:03,175-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsAssetBlobDAO
2026-02-12 10:12:03,216-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsAssetDAO
2026-02-12 10:12:03,249-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for CocoapodsBrowseNodeDAO
2026-02-12 10:12:03,268-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoContentRepositoryDAO
2026-02-12 10:12:03,280-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoComponentDAO
2026-02-12 10:12:03,315-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoAssetBlobDAO
2026-02-12 10:12:03,355-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoAssetDAO
2026-02-12 10:12:03,386-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for GoBrowseNodeDAO
2026-02-12 10:12:03,407-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2AssetBlobDAO
2026-02-12 10:12:03,437-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2ContentRepositoryDAO
2026-02-12 10:12:03,449-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2ComponentDAO
2026-02-12 10:12:03,486-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2AssetDAO
2026-02-12 10:12:03,519-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for P2BrowseNodeDAO
2026-02-12 10:12:03,541-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for DeletedBlobDAO
2026-02-12 10:12:03,562-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for NodeHeartbeatDAO
2026-02-12 10:12:03,594-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SamlConfigurationDAO
2026-02-12 10:12:03,605-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for SamlUserDAO
2026-02-12 10:12:03,615-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for RepositoryMetricsDAO
2026-02-12 10:12:03,644-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmContentRepositoryDAO
2026-02-12 10:12:03,662-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmKeyValueDAO
2026-02-12 10:12:03,684-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmComponentDAO
2026-02-12 10:12:03,716-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmAssetBlobDAO
2026-02-12 10:12:03,750-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmAssetDAO
2026-02-12 10:12:03,779-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.datastore.mybatis.MyBatisDataStore - nexus - Creating schema for HelmBrowseNodeDAO
2026-02-12 10:12:03,811-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.internal.node.datastore.LocalNodeAccess - ID: CE221A03-078D59D1-0DB1A98F-CA904C6F-B161A585
2026-02-12 10:12:03,833-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start RESTORE
2026-02-12 10:12:03,874-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Start UPGRADE
2026-02-12 10:12:04,119-0800 ERROR [FelixStartLevel]  *SYSTEM org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl - Missing migrations: [SearchCapabilityStep_2_1, SecretsMigrationStep_2_2, BrowseNodeMigrationStep_2_3, CustomS3RegionCapabilityMigrationStep_2_4, GoogleBlobStoreMigrationStep_2_5, S3FailoverMigrationStep_2_6, SoftDeletedBlobsByBlobStoreIndexMigrationStep_2_7, ConanV2UpgradeStep_2_8, MalwareRemediatorTaskMigrationStep_2_9, MalwareRemediatorMigrationStep_2_10, BlobstoreSecretsMigrationStep_2_11, HuggingFaceProxyDatabaseMigrationStep_2_12, CoordinateMigrationStep_2_13, RemoveDistributedCooperationMigrationStep_2_14, RemoveLog4JVisualizer_2_15, SearchCapabilityStep_2_16, TrustedCertificatesMigrationStep_2_17, NodeHeartBeatMigrationStep_2_17_1, ConanCleanupMigrationStep_2_18, AssetBlobMigrationStep_2_18_1, AssetBlobMigrationStep_2_18_2, FileBlobStoreMetricsMigrationStep_2_19, S3BlobStoreMetricsMigrationStep_2_20, AzureBlobStoreMetricsMigrationStep_2_21, RepairAptMetadataLeadingSlash_2_22, AssetBlobAddedToRepositoryMigrationStep_2_27, ComponentEntityVersionMigrationStep_2_28, Maven2ComponentBaseVersionMigrationStep_2_29, ApiKeyCreatedMigrationStep_2_30, SoftDeletedBlobsDatePathRefMigrationStep_2_31, AssetTableIndexesMigrationStep_2_32, ComponentApplicationScanEvaluationDelayMigrationStep_2_33, AggregatedMetricsNodeIdMigrationStep_2_34, ReconcilePlanDetailsPropertiesMigrationStep_2_35, DistributedAuthTicketCacheRealmNameMigrationStep_2_36, SearchComponentsAdditionalColumnsMigrationStep_2_37, NodeHeartbeatInfoColumnsMigrationStep_2_38, NugetComponentIndexesMigrationStep_2_39, QuartzIndexesMigrationStep_2_40, ApiKeyIndexesMigrationStep_2_41, NexusKeyValueIndexesMigrationStep_2_42, CleanupPolicyIndexMigrationStep_2_43, LoggingOverridesIndexMigrationStep_2_44, UserRoleMappingIndexMigrationStep_2_45, PrivilegeIndexMigrationStep_2_46, SecretsIndexMigrationStep_2_47, SoftDeletedBlobsIndexMigrationStep_2_48, NodeHeartbeatIndexesMigrationStep_2_49, ComponentTableIndexesMigrationStep_2_50, DistributedAuthTicketCacheIndexesMigrationStep_2_51, CacheIndexesMigrationStep_2_52, SearchTableIndexesMigrationStep_2_53, SupportZipInfoIndexesMigrationStep_2_54, DistributedEventIndexesMigrationStep_2_55, AggregatedMetricsIndexesMigrationStep_2_56, MetricsLogIndexesMigrationStep_2_57, RepositoryMetricsIndexesMigrationStep_2_58, ComponentApplicationScanIndexesMigrationStep_2_59, ComponentApplicationScanScheduleIndexesMigrationStep_2_60, ReconcilePlanIndexesMigrationStep_2_61, ReconcilePlanDetailsIndexesMigrationStep_2_62, UserTokenIndexesMigrationStep_2_63, DockerForeignLayersIndexesMigrationStep_2_64, KeyValueIndexesMigrationStep_2_65, BrowseNodeIndexesMigrationStep_2_66, AssetBlobIndexesMigrationStep_2_67, AssetIndexesMigrationStep_2_68, ComponentNormalizedVersionConstraintMigrationStep_2_69, AssetBlobExternalMetadataMigrationStep_2_70, ComponentIndexesMigrationStep_2_71, JobKeyUnificationMigrationStep_2_72, SwiftBrowseNodeIndexMigrationStep_2_73, PrivilegeNxRM2UpgradeStep_2_74, RepositoriesBearerTokenMigrationStep_2_75, RemoveOrphanedSearchRecordsMigrationStep_2_76]
2026-02-12 10:12:04,119-0800 ERROR [FelixStartLevel]  *SYSTEM org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl - Missing migrations: [SearchCapabilityStep_2_1, SecretsMigrationStep_2_2, BrowseNodeMigrationStep_2_3, CustomS3RegionCapabilityMigrationStep_2_4, GoogleBlobStoreMigrationStep_2_5, S3FailoverMigrationStep_2_6, SoftDeletedBlobsByBlobStoreIndexMigrationStep_2_7, ConanV2UpgradeStep_2_8, MalwareRemediatorTaskMigrationStep_2_9, MalwareRemediatorMigrationStep_2_10, BlobstoreSecretsMigrationStep_2_11, HuggingFaceProxyDatabaseMigrationStep_2_12, CoordinateMigrationStep_2_13, RemoveDistributedCooperationMigrationStep_2_14, RemoveLog4JVisualizer_2_15, SearchCapabilityStep_2_16, TrustedCertificatesMigrationStep_2_17, NodeHeartBeatMigrationStep_2_17_1, ConanCleanupMigrationStep_2_18, AssetBlobMigrationStep_2_18_1, AssetBlobMigrationStep_2_18_2, FileBlobStoreMetricsMigrationStep_2_19, S3BlobStoreMetricsMigrationStep_2_20, AzureBlobStoreMetricsMigrationStep_2_21, RepairAptMetadataLeadingSlash_2_22, AssetBlobAddedToRepositoryMigrationStep_2_27, ComponentEntityVersionMigrationStep_2_28, Maven2ComponentBaseVersionMigrationStep_2_29, ApiKeyCreatedMigrationStep_2_30, SoftDeletedBlobsDatePathRefMigrationStep_2_31, AssetTableIndexesMigrationStep_2_32, ComponentApplicationScanEvaluationDelayMigrationStep_2_33, AggregatedMetricsNodeIdMigrationStep_2_34, ReconcilePlanDetailsPropertiesMigrationStep_2_35, DistributedAuthTicketCacheRealmNameMigrationStep_2_36, SearchComponentsAdditionalColumnsMigrationStep_2_37, NodeHeartbeatInfoColumnsMigrationStep_2_38, NugetComponentIndexesMigrationStep_2_39, QuartzIndexesMigrationStep_2_40, ApiKeyIndexesMigrationStep_2_41, NexusKeyValueIndexesMigrationStep_2_42, CleanupPolicyIndexMigrationStep_2_43, LoggingOverridesIndexMigrationStep_2_44, UserRoleMappingIndexMigrationStep_2_45, PrivilegeIndexMigrationStep_2_46, SecretsIndexMigrationStep_2_47, SoftDeletedBlobsIndexMigrationStep_2_48, NodeHeartbeatIndexesMigrationStep_2_49, ComponentTableIndexesMigrationStep_2_50, DistributedAuthTicketCacheIndexesMigrationStep_2_51, CacheIndexesMigrationStep_2_52, SearchTableIndexesMigrationStep_2_53, SupportZipInfoIndexesMigrationStep_2_54, DistributedEventIndexesMigrationStep_2_55, AggregatedMetricsIndexesMigrationStep_2_56, MetricsLogIndexesMigrationStep_2_57, RepositoryMetricsIndexesMigrationStep_2_58, ComponentApplicationScanIndexesMigrationStep_2_59, ComponentApplicationScanScheduleIndexesMigrationStep_2_60, ReconcilePlanIndexesMigrationStep_2_61, ReconcilePlanDetailsIndexesMigrationStep_2_62, UserTokenIndexesMigrationStep_2_63, DockerForeignLayersIndexesMigrationStep_2_64, KeyValueIndexesMigrationStep_2_65, BrowseNodeIndexesMigrationStep_2_66, AssetBlobIndexesMigrationStep_2_67, AssetIndexesMigrationStep_2_68, ComponentNormalizedVersionConstraintMigrationStep_2_69, AssetBlobExternalMetadataMigrationStep_2_70, ComponentIndexesMigrationStep_2_71, JobKeyUnificationMigrationStep_2_72, SwiftBrowseNodeIndexMigrationStep_2_73, PrivilegeNxRM2UpgradeStep_2_74, RepositoriesBearerTokenMigrationStep_2_75, RemoveOrphanedSearchRecordsMigrationStep_2_76]
2026-02-12 10:12:04,121-0800 ERROR [FelixStartLevel]  *SYSTEM org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl - Failed transition: NEW -> STARTED
org.sonatype.nexus.upgrade.datastore.UpgradeException: The database appears to be from a later version of Nexus Repository
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.checkSchemaVersionIsAcceptable(UpgradeManagerImpl.java:203)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:88)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:51)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.MethodInvocationAction.run(MethodInvocationAction.java:39)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:206)
	at org.sonatype.nexus.common.stateguard.TransitionsInterceptor.invoke(TransitionsInterceptor.java:57)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:210)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:121)
	at org.sonatype.nexus.extender.NexusContextListener.moveToPhase(NexusContextListener.java:334)
	at org.sonatype.nexus.extender.NexusContextListener.frameworkEvent(NexusContextListener.java:231)
	at org.apache.felix.framework.Felix.setActiveStartLevel(Felix.java:1597)
	at org.apache.felix.framework.FrameworkStartLevelImpl.run(FrameworkStartLevelImpl.java:308)
	at java.base/java.lang.Thread.run(Thread.java:840)
2026-02-12 10:12:04,122-0800 ERROR [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusContextListener - Failed to start nexus
org.sonatype.nexus.upgrade.datastore.UpgradeException: The database appears to be from a later version of Nexus Repository
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.checkSchemaVersionIsAcceptable(UpgradeManagerImpl.java:203)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:88)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:51)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.MethodInvocationAction.run(MethodInvocationAction.java:39)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:206)
	at org.sonatype.nexus.common.stateguard.TransitionsInterceptor.invoke(TransitionsInterceptor.java:57)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:210)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:121)
	at org.sonatype.nexus.extender.NexusContextListener.moveToPhase(NexusContextListener.java:334)
	at org.sonatype.nexus.extender.NexusContextListener.frameworkEvent(NexusContextListener.java:231)
	at org.apache.felix.framework.Felix.setActiveStartLevel(Felix.java:1597)
	at org.apache.felix.framework.FrameworkStartLevelImpl.run(FrameworkStartLevelImpl.java:308)
	at java.base/java.lang.Thread.run(Thread.java:840)
2026-02-12 10:12:04,123-0800 ERROR [FelixStartLevel]  *SYSTEM Felix - Framework listener delivery error.
java.lang.RuntimeException: org.sonatype.nexus.upgrade.datastore.UpgradeException: The database appears to be from a later version of Nexus Repository
	at org.sonatype.nexus.extender.NexusContextListener.frameworkEvent(NexusContextListener.java:243)
	at org.apache.felix.framework.Felix.setActiveStartLevel(Felix.java:1597)
	at org.apache.felix.framework.FrameworkStartLevelImpl.run(FrameworkStartLevelImpl.java:308)
	at java.base/java.lang.Thread.run(Thread.java:840)
Caused by: org.sonatype.nexus.upgrade.datastore.UpgradeException: The database appears to be from a later version of Nexus Repository
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.checkSchemaVersionIsAcceptable(UpgradeManagerImpl.java:203)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeManagerImpl.migrate(UpgradeManagerImpl.java:88)
	at org.sonatype.nexus.upgrade.datastore.UpgradeManager.migrate(UpgradeManager.java:34)
	at org.sonatype.nexus.upgrade.datastore.internal.UpgradeServiceImpl.doStart(UpgradeServiceImpl.java:51)
	at org.sonatype.nexus.common.stateguard.StateGuardLifecycleSupport.start(StateGuardLifecycleSupport.java:69)
	at org.sonatype.nexus.common.stateguard.MethodInvocationAction.run(MethodInvocationAction.java:39)
	at org.sonatype.nexus.common.stateguard.StateGuard$TransitionImpl.run(StateGuard.java:206)
	at org.sonatype.nexus.common.stateguard.TransitionsInterceptor.invoke(TransitionsInterceptor.java:57)
	at org.sonatype.nexus.extender.NexusLifecycleManager.startComponent(NexusLifecycleManager.java:210)
	at org.sonatype.nexus.extender.NexusLifecycleManager.to(NexusLifecycleManager.java:121)
	at org.sonatype.nexus.extender.NexusContextListener.moveToPhase(NexusContextListener.java:334)
	at org.sonatype.nexus.extender.NexusContextListener.frameworkEvent(NexusContextListener.java:231)
	... 3 common frames omitted
2026-02-12 10:12:04,136-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusContextListener - Uptime: 27 seconds and 299 milliseconds (nexus-pro-edition/3.70.1.02)
2026-02-12 10:12:04,136-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Shutting down
2026-02-12 10:12:04,139-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop RESTORE
2026-02-12 10:12:04,139-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop STORAGE
2026-02-12 10:12:04,143-0800 INFO  [FelixStartLevel]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Shutdown initiated...
2026-02-12 10:12:04,184-0800 INFO  [FelixStartLevel]  *SYSTEM com.zaxxer.hikari.HikariDataSource - nexus - Shutdown completed.
2026-02-12 10:12:04,185-0800 INFO  [FelixStartLevel]  *SYSTEM org.sonatype.nexus.extender.NexusLifecycleManager - Stop KERNEL
