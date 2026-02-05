---
- name: Nexus Configuration Test Deployment
  hosts: lxpd208
  become: no
  vars:
    # Path Definitions
    nexus_base_path: "/opt/nexus"
    nexus_test_dir: "{{ nexus_base_path }}/test"
    
    # Internal paths used in config templates
    nexus_data_dir: "{{ nexus_base_path }}/sonatype-work/nexus3"
    nexus_ssl_dir: "{{ nexus_base_path }}/ssl"
    
    # Ownership
    deploy_user: "cmdeploy"
    deploy_group: "edrstaff"
    
    # Performance Parameters
    nexus_xms: "6G"
    nexus_xmx: "6G"
    nexus_max_direct_memory: "15530M"
    
    # Certificate and Passwords
    keystore_filename: "nexus01.jks"
    keystore_password: "edrcmadm"
    keystore_password_obf: "OBF:1unr1sov1uvk1u9h1ua11uum1sov1uo7"

  tasks:
    - name: Ensure test directory exists
      file:
        path: "{{ nexus_test_dir }}"
        state: directory
        owner: "{{ deploy_user }}"
        group: "{{ deploy_group }}"
        mode: '0755'

    - name: Generate nexus.vmoptions in test folder
      template:
        src: templates/nexus.vmoptions.j2
        dest: "{{ nexus_test_dir }}/nexus.vmoptions"
        owner: "{{ deploy_user }}"
        group: "{{ deploy_group }}"
        mode: '0644'
        backup: yes
      register: vm_test

    - name: Generate jetty-https.xml in test folder
      template:
        src: templates/jetty-https.xml.j2
        dest: "{{ nexus_test_dir }}/jetty-https.xml"
        owner: "{{ deploy_user }}"
        group: "{{ deploy_group }}"
        mode: '0644'
        backup: yes
      register: jetty_test

    - name: Verify if certificate exists at correct path
      stat:
        path: "{{ nexus_ssl_dir }}/{{ keystore_filename }}"
      register: jks_check

    - name: Display deployment status
      debug:
        msg: 
          - "VMOptions Path: {{ nexus_test_dir }}/nexus.vmoptions"
          - "Jetty XML Path: {{ nexus_test_dir }}/jetty-https.xml"
          - "SSL Certificate ({{ nexus_ssl_dir }}): {{ 'Found' if jks_check.stat.exists else 'Missing' }}"
