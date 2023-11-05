# Ansible ping command
```Bash
# Maybe the sshpass should have to be installed
ansible -u vagrant -i inventory ubuntu -m ping --ask-pass
ansible -u vagrant -i inventory ubuntu -m ping -K

# Or use with copied ssh-key
# ssh-copy-id -i ~/.ssh/mykey user@host
ansible -u vagrant -i inventory ubuntu -m ping
ansible -u vagrant -i inventory win -m win_ping -vv 
```

# Ansible ad-hoc command
ansible -u vagrant -i inventory ubuntu -m shell -a "cat /etc/*ele*"