# pi-ansible
Ansible playbooks for configuring my media server.

### TODO:
- Assign static IP
- add new account to sudoers
- Run smbpassswd for the created user account

### Overview

This playbook is intended to be used to setup up my Raspberry Pi which I primarily use as a media server. The Vagrantfile is intended to be used in testing the playbook. We run the playbook on a virtual machine, then verify it's working correctly before deploying to the Raspberry Pi.

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