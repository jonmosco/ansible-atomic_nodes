# Ansible role for Atomic Cluster configuration and deployment

### About
This follows Project Atomics getting started guide:
http://www.projectatomic.io/docs/gettingstarted/

I will try to maintain this as the document gets updated.  Please feel free to submit pull requests

###Vagrant environment

This repository contains a Vagrant environment as a test environment with one master, and one node,
and more can be added easily.

To change the IP Address of each Vagrant node, modify:
```
MASTER_IP="192.168.60.2"
NODE01_IP="192.168.60.3"
```

In order to use the role with Vagrant, there is a site.yml in the top level directory.  Add the correct
addresses from your Vagrant env in this file, and simply `vagrant up`

### Requirements

This playbook has been tested with Ansible 1.9+

### Usage

Variables:
```
  atomic_master:
  etcd_master:
  primary_interface:
```

###Bugs

Please submit pull requests
