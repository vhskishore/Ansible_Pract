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
