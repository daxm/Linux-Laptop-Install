# Linux-Laptop-Install
This repo is a list of applications that I install using Ansible during an install of Linux on a laptop

This repo contains Ansible playbooks to configure your system as a development machine upon a clean install. The playbooks should run in Debian based system but was only tested with **Ubuntu 18.04**

## Pre-requisites
On the system which you are going to setup using Ansible, perform these steps.
You need to install Ansible and git before running the playbooks. You can either install it using `pip` or though `apt`.
```
sudo apt install ansible git

```
And then clone this repo:
```
git clone https://github.com/daxm/Linux-Laptop-Install.git
cd Linux-Laptop-Install

```

## Perform the installation
You can just issue the following to install all packages:
```
ansible-playbook go.yml -K

```
OR, you can install sections of the playbook, based on tag(s).
```
ansible-playbook go.yml --tags "standard_install" -K

```

## List of packages and their tags
The list of packages that are installed are in the "./group_vars/all.yml" file.  Read the go.yml file to determine which play/role goes with which tag.

## Additional tasks
- In addition to the list of packages discussed above this playbook also does a Ubuntu dist upgrade.  This might require you to reboot, though I don't think you'll be warned/asked to do so.
