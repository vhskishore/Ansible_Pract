# Installation and Configuration

### Requirements:
- RHEL/Ubuntu/CentOS/Debian with Python2(version 2.7) or Python 3(Version 3.5 and higher) installed
- Windows isn't supported for control node.
- Master master Unix like based systems.
- We can select Windows or Linux servers for Ansible Nodes/Clients.

### Steps to configure Ansible
 - Launch/select required number of servers. Which are called Managed Nodes/Clients.
 - Requirements for Manager Nodes/Clients:
    - Python 2(version 2.6 or later) or Python 3 (version 3.5 or later)
*** Note: We can also work without Python on Manager Nodes that is using raw modules.

*** Ansible version 2.4 and later can manage earlier operating systems that contain Python 2.5 or higher.


### We can install Ansible in three ways.
 - Using YUM
 - Using pip
 - Using compile file

### Steps to install Ansible on Ubuntu
    sudo apt update
    sudo apt install software-properties-common
    sudo add-apt-repository --yes --update ppa:ansible/ansible
    sudo apt install ansible