# Transfer file with COPY module

- We can transfer files with COPY module
```
ansible -i <inventory_file> or group of server -m copy -a "src="location of file from ansible master dest=location where to copy in node"
```

- Example:
```
ansible webservers -m copy -a "src=./host desk=/tmp"
```
- To copy content
```
ansible db -m copy -a "content = 'hello this is kishore' dest=/tmp/file.txt"
```
- If we re-run above command with different content to same file it will delete existing, To take backup of existing file
```
ansible db -m copy -a "content = 'hello this is kishore\n' dest=/tmp/file.txt backup=yes"
```