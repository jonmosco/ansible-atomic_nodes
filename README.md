# Ansible role for Atomic Cluster configuration and deplpyment

### About
This follows Project Atomics getting started guide:
http://www.projectatomic.io/docs/gettingstarted/

I will try to maintain this as the document gets updated.  Please feel free to submit pull requests

### Requirements

This playbook has been tested with Ansible 1.9+

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
