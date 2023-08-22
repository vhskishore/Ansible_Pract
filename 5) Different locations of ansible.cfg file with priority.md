# Different locations of ansible.cfg file with priority

- Priotiry and locations (Top to Bottom)
    1. ANSIBLE_CONFIG environment variable.
    2. ./ansible.cfg from current directory.
    3. ~./ansible.cfg file present in home directory.
    4. /etc/ansible/ansible.cfg (Default ansible.cfg file).

- Ansible will only utilize the configuration settings from the file located in this sequence initially; if the setting is not present in the file chosen for deployment, it will not seek for it in the higher sequence files.

- Assume we have ansible.cfg file at current place with no settings, if we require inventory file location but did not put in current location, ansible will not consider other ansible.cfg files. It will not accept it from a different place in the ansible.cfg file. If it has settings, it will use them; otherwise, an error will occur.
