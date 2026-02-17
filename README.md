Encryption Key File Location

The Nexus custom encryption key is stored as a JSON file on each HA node.

File Path

/opt/nexus/sonatype-work/nexus3/etc/nexus.secrets.json

Important Notes

This file must exist on all Nexus HA nodes.

The file content must be identical across nodes.

Nexus reads this file during startup via nexus.properties.
