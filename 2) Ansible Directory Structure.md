# Ansible Directory Structure

- Default installation location
    - /etc/ansible which is called ansible_home
- ansible_home directory(default directory) consist of:
    - ansible.cfg
    - hosts
    - roles
- add IP/FQDN to hosts(inventory file) file
    ```
    vi /etc/ansible/hosts
    ```
- We can use our own Inventory file location and name. Open ansible.cfg and change
    ```
    vi /etc/ansible/ansible.cfg
    vi /etc/ansible/ansible.cfg
    inventory = <location of inventory file>
    ```
- Create custom host file with name myhosts add IP/FQDN to it and add following line in /etc/ansible/ansible.cfg
    ```
    vi /etc/ansible/ansible.cfg
    vi /etc/ansible/ansible.cfg
    inventory = /ansadmin/inventory/myhosts
    ```
- Suppose many people are working on same ansible location. To avoid confussion create own ansible directory
    ```
    cd my_ansible
    cp -rpP /etc/ansible/*
    vi inventory ( add all FQDN/IP to it)
    vi /my_ansible/ansible.cfg
    inventory = /my_ansible/inventory
    ```
- If we have different inventory files like inventory1 and inventory2, If I want to work with these inventories without updating in ansible.cfg file then manction
    ```
    ansible all -m ping -i <inventory location>
    ```
