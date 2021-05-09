# pi-ansible

## Overview

This playbook is used to configure a media server. It performs installation of plex and any dependencies. It mounts an external hard drive with a friendly device name from udev and uses samba to share it on the network. It also configures a user account with sudo permissions and standard aliases. 

## Setup
### Prerequisites

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