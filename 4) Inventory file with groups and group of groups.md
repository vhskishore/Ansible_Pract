# Inventory file with Groups and Groups of Groups

 - If you want work with one server in inventoy file (IP/FQDN should be exist in inventory file)
   ```
   ansible <IP/FQDN> -m ping
   ```
 - If you want to work with two servers
   ```
   ansible <IP/FQDN>:<IP/FQDN> -m ping
   ```
 - If you want to work with particular servers among all serves in inventory file, update the inventory as follows
   ```
   [web_server]
   server1
   server2
   [midd_tomcat]
   server3
   server4
   [db_mysql]
   server5
   server6
   ```
 - Eventhough we have different groups we have common group which is [all]
 - We can club groups (Groups of Groups)
   ```
   [db:children]
   db_oracle
   db_mysql
   ansible db -m ping
   ```
  
