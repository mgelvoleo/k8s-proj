# k8s-proj

# Installed the ansible in our workstation


###
nano /etc/hosts

```
192.168.60.11 node
```


###
```
ssh-keygen
```

###
```
ssh-copy-id localhost
```

###
```
ssh-copy-id node
ssh-copy-id -i ~/.ssh/ansible.pub 192.168.60.11
```

###
Create file /inventory 

```
[minikube]
192.168.60.11
```

###
Create ansible.cfg
```
ansible.cfg

[defaults]

inventory = inventory
private_key_file = ~/.ssh/ansible

```
###
Create ansible.cfg
```
Bash Command
ansible all -m ping

```

# Tips to get the info of servers
ansible all -m gather_facts
ansible all -m gather_facts --limit 192.168.60.11
