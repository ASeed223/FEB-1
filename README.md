---
- name: Nexus Configuration Test Deployment
  hosts: lxpd208
  become: no
  vars:
    # Path Definitions
    nexus_base_path: "/opt/nexus"
    # Target folder for testing
    nexus_test_dir: "{{ nexus_base_path }}/test"
    
    # Internal paths used inside the config files
    nexus_data_dir: "{{ nexus_base_path }}/sonatype-work/nexus3"
    nexus_ssl_dir: "{{ nexus_base_path }}/ssl"
    
    # Ownership (From your environment)
    deploy_user: "cmdeploy"
    deploy_group: "edrstaff"
    
    # Performance Parameters
    nexus_xms: "6G"
    nexus_xmx: "6G"
    nexus_max_direct_memory: "15530M"
    
    # Certificate and Passwords
    keystore_filename: "nexus01.jks"
    # Unified variable name to fix the 'undefined' error
    keystore_password: "edrcmadm"
    keystore_password_obf: "OBF:1unr1sov1uvk1u9h1ua11uum1sov1uo7"

  tasks:
    - name: Create the test directory
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

    - name: Display test deployment results
      debug:
        msg: 
          - "VMOptions Path: {{ nexus_test_dir }}/nexus.vmoptions"
          - "Jetty XML Path: {{ nexus_test_dir }}/jetty-https.xml"
          - "Deployment Status: Success"
