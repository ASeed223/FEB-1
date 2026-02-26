---
- name: Batch Fix All Blob Store Paths via Symlink
  hosts: lxpd208  # 运行 Nexus 的主服务器
  gather_facts: no
  become: yes
  vars:
    # 凭据声明
    nexus_username: "admin"
    nexus_password: "你的密码"
    nexus_url: "https://127.0.0.1:8443"
    
    # 目标大容量路径
    nfs_base_path: "/opt/appdata/nexus/sonatype-work/nexus3/blobs"
    # Nexus 默认的本地数据目录 (通常是显示 2.65GB 的地方)
    local_work_dir: "/opt/sonatype/sonatype-work/nexus3/blobs"

  tasks:
    - name: 1. Scan all Blob Stores via API
      ansible.builtin.uri:
        url: "{{ nexus_url }}/service/rest/v1/blobstores"
        method: GET
        user: "{{ nexus_username }}"
        password: "{{ nexus_password }}"
        force_basic_auth: yes
        validate_certs: no
      register: blob_list

    - name: 2. Stop Nexus Service before migration
      # 迁移 2.8TB 数据必须先停服务
      ansible.builtin.shell: /opt/nexus/nexus/bin/nexus stop
      ignore_errors: yes

    - name: 3. Process each Blob Store
      include_tasks: migrate_one.yml
      loop: "{{ blob_list.json }}"
      when: item.type == 'file'
      loop_control:
        label: "{{ item.name }}"

    - name: 4. Restart Nexus Service
      ansible.builtin.shell: /opt/nexus/nexus/bin/nexus start

# --- 另存为 migrate_one.yml ---
- name: "Migrating {{ item.name }}"
  block:
    - name: "Set paths for {{ item.name }}"
      set_fact:
        # 很多旧的 Blob Store 默认路径就是它的名字，在 local_work_dir 下
        current_phys_path: "{{ local_work_dir }}/{{ item.name }}"
        target_phys_path: "{{ nfs_base_path }}/{{ item.name }}"

    - name: "Create target directory on NFS"
      ansible.builtin.file:
        path: "{{ nfs_base_path }}"
        state: directory
        owner: nexus
        group: nexus

    - name: "Move and Symlink {{ item.name }}"
      shell: |
        # 如果当前路径是文件夹且不是软链接，说明需要迁移
        if [ -d "{{ current_phys_path }}" ] && [ ! -L "{{ current_phys_path }}" ]; then
          mv "{{ current_phys_path }}" "{{ target_phys_path }}"
          ln -s "{{ target_phys_path }}" "{{ current_phys_path }}"
          chown -h nexus:nexus "{{ current_phys_path }}"
        fi
