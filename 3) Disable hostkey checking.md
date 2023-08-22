# Disable Host Key Checking

### Ways to disable Host Key Checking
 - export ANSIBLE_HOST_KEY_CHECKING=False
 - In ansible.cfg file uncomment hostkey checking as false
   ```
   host_key_checking = False
   ```
