Since multiple Ansible playbooks rely on the cmdeploy and nexus service accounts, and their credentials are currently stored in tfs_ansible_vault.yaml, the vault file must be updated each time we perform our semi-annual password rotation.

To ensure the playbooks continue running without interruption after the password change, please follow the steps below to update the credentials properly and maintain operational stability.
