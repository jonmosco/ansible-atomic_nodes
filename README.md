# Ansible Playbook for Atomic Node configuration

### Usage
Create a hosts file to use for configuration of your Atomic host environment

Replace
```
  vars:
    atomic_master: 192.168.3.10
```
with your Kubernetes master address/hostname

Substitute your primary network interface:
```
ansible_eno16780032.ipv4.address
```
