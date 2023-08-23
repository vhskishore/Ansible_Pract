# Download a file from Node to Master

- Syntax:

```
ansible -i<inventory_file> <server1:server2> -m <module> [-a arguments]
ansible prob_servers -m fetch -a "src=/sourct/file/path dest=/dest/path"
```
- Example
```
ansible prod_servers -m fetch -a "src=/home/ansadmin/demo.txt dest=./demo/"
```