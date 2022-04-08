#Patch linux VM's 

This playbook/role will first determind the OS of the VM (Distro), before it will start patching it. <br>

This playbook works on: 
- [X] Debian
- [X] Centos
- [X] Ubuntu
- [X] RHEL8
- [X] Rocky Linux 8.5

on processor architecture:
- [X] x64
- [X] ARM

✅ Playbook requirements:
* Sudo access to the VM
* The target machine needs Internet access
* Ansible installed on the host running the playbook

Example playbook: 
```
- hosts: ip-address
  gather_facts: true
  become: yes

  roles:
  - linux_os_patch
```

Example playbook run: 
```
ansible-playbook setup.yml -i inventory --ask-become-pass
```
The playbook will then ask for the 'Sudo' password for the host target. 
