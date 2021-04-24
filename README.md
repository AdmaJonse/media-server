# pi-ansible
Ansible playbooks for configuring my media server.

### TODO:
- Assign static IP
- Set a password for the created user account using the ansible vault
- Run smbpassswd for the created user account using the same password
- configure the plex server
- udev rule trigger doesn't seem to work reliably

## Overview

This playbook is intended to be used to setup up my Raspberry Pi which I primarily use as a media server. The Vagrantfile is intended to be used in testing the playbook. We run the playbook on a virtual machine, then verify it's working correctly before deploying to the Raspberry Pi.

## Setup
### Pre-Requisites

Install Ansible on the Linux host:
```
> apt-get install ansible
```
Clone this repository onto the Linux host:
```
> git clone https://github.com/AdmaJonse/pi-ansible.git
```

### Running the Playbook

To run the playbook, use the following command:
```
> ansible-playbook pi.yml
```

## Troubleshooting
### Can't access the samba share from remote machines
Make sure you've run the `smbpasswd` command for the account you're attempting to use to login. As root, run the following:
```
> smbpasswd -a ajones
```

### The udev friendly name doesn't seem to be working
Rebooting or reconnecting the XHD will cause the rule to trigger as expected. Need to rework the playbook so that this isn't necessary. 