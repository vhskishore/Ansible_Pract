# Transfer file with COPY module

- We can transfer files with COPY module
```
ansible -i <inventory_file> or group of server -m copy -a "src="location of file from ansible master dest=location where to copy in node"
```

