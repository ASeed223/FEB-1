find /opt/appdata/nexus/sonatype-work/nexus3/blobs/Docker/content -name "*.properties" -exec grep -l "deleted=true" {} + | head -n 10
