# pi-ansible
Ansible playbooks for configuring my media server.

### TODO:
- Create the ajones user account (with aliases, ssh keys, etc)
- Create a udev entry for the XHD
- Mount the XHD on startup
- Configure samba for the XHD
- Assign static IP
- add new account to sudoers
- Run smbpassswd for the created user account

### Overview

This playbook is intended to be used to setup up my Raspberry Pi which I primarily use as a media server. The Vagrantfile is intended to be used in testing the playbook. We run the playbook on a virtual machine, then verify it's working correctly before deploying to the Raspberry Pi.

### Pre-Requisites

Install Ansible on the Linux host. On the Linux host run:
```
> apt-get install ansible
```

Copy this repository to the Linx host. From the Windows machine run:
```
> scp -r pi-ansible pi@192.168.1.xxx:/home/pi/.
```

TODO: should just pull the repo from git