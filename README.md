# k8s-proj

###
nano /etc/hosts

```
192.168.60.11 minikube
```


###
```
$ ssh-keygen
```

###
```
$ ssh-copy-id localhost
```

###
```
$ ssh-copy-id node
```

###
Create file inventory 

```
[minikube]
192.168.60.11
```

###
Create ansible.cfg
```
[defaults]

inventory = inventory
```
