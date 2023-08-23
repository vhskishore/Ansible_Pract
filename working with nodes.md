# Working with Nodes
- Two ways:
    1. Ad-hoc commands
    2. Playbooks

# What is Ad-hoc command?
- The Ad-Hoc command is the one-liner ansible command that performs one task on the target host(s)/group(s).
```
ansible [-i <inventory_file location>] server:group:child-grpups -m module [-a arguments for modules (optional)]
```

```
ansible all -m ping
ansible db:web_server -m ping
```
```
ansible db:web_server -m shell -a "uptime"
ansible db:web_server -m shell -a "free -m"
```
```
ansible -i prod_inventory -m shell -a "uptime"
ansible -i prod_inventory -m shell -a "free -m"
```
- Module is simply a program designed to execute a task, Based on the required task we have to select required module.
```
ansible-doc -l
```
```
ansible-doc <module_name>
```