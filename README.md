---
- name: Nexus Configuration Test Deployment
  hosts: lxpd208
  become: no
  vars:
    # Path Definitions
    nexus_base_path: "/opt/nexus"
    nexus_install_dir: "{{ nexus_base_path }}/nexus3"
    nexus_data_dir: "{{ nexus_base_path }}/sonatype-work/nexus3"
    nexus_ssl_dir: "{{ nexus_base_path }}/ssl"
    
    # Ownership Definitions (Updated based on your environment)
    deploy_user: "cmdeploy"
    deploy_group: "edrstaff"
    
    # Performance Parameters
    nexus_xms: "6G"
    nexus_xmx: "6G"
    nexus_max_direct_memory: "15530M"
    
    # Certificate and Passwords
    keystore_filename: "nexus01.jks"
    keystore_password_raw: "edrcmadm"
    keystore_password_obf: "OBF:1unr1sov1uvk1u9h1ua11uum1sov1uo7"

  tasks:
    - name: Ensure target directories exist
      file:
        path: "{{ item }}"
        state: directory
        owner: "{{ deploy_user }}"
        group: "{{ deploy_group }}"
        mode: '0755'
      loop:
        - "{{ nexus_install_dir }}/bin"
        - "{{ nexus_install_dir }}/etc/jetty"
        - "{{ nexus_ssl_dir }}"

    - name: Generate nexus.vmoptions from template
      template:
        src: templates/nexus.vmoptions.j2
        dest: "{{ nexus_install_dir }}/bin/nexus.vmoptions"
        owner: "{{ deploy_user }}"
        group: "{{ deploy_group }}"
        mode: '0644'
        backup: yes
      register: vm_test

    - name: Generate jetty-https.xml from template
      template:
        src: templates/jetty-https.xml.j2
        dest: "{{ nexus_install_dir }}/etc/jetty/jetty-https.xml"
        owner: "{{ deploy_user }}"
        group: "{{ deploy_group }}"
        mode: '0644'
        backup: yes
      register: jetty_test

    - name: Check if JKS certificate exists
      stat:
        path: "{{ nexus_ssl_dir }}/{{ keystore_filename }}"
      register: jks_check

    - name: Display deployment status
      debug:
        msg: 
          - "VMOptions Status: {{ 'Changed' if vm_test.changed else 'No Change' }}"
          - "Jetty XML Status: {{ 'Changed' if jetty_test.changed else 'No Change' }}"
          - "Certificate File: {{ 'Found' if jks_check.stat.exists else 'Missing' }}"
