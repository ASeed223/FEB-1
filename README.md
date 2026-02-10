nohup rsync -avzP -e ssh --bwlimit=100000 /opt/appdata/nexus/sonatype-work/nexus3/blobs/ cmdeploy@lxpd208:/opt/appdata/nexus/sonatype-work/nexus3/blobs/ > sync.log 2>&1 &
