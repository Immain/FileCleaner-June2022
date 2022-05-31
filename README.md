# FileCleaner-June2022
Ansible script to clean all files except the latest five files within a folder. This is useful if you consistently take backups but only want the latest of those files

## How it works:
For example, let's say you take consistent backups every 2-3 hours, at one point you realize that it's taking up too much space on your backup drive. This script will clean the folder of all backups except the latest five by checking the length of files inside of that folder. If you run the scipt again accidentally, it will not remove any other folders or files within the drive as a fail safe. 

## OS
This will work on 
- Ubuntu 
- CentOS
- Alma Linux
- Alpine

## How to Run:
all you need to do is navigate to where you store your ansible playbook files, then run the command:
```
ansible-playbook cleaner.yml
```

If you want to use this on multiple hosts, you would create the hosts file, and add the IP addresses of the machines you'd like to run the script on, then use the following command:
```
ansible-playbook cleaner.yml -i hosts
```
