# Ansible  Kubernetes


## Setup SSH-KEYGEN for password less login

``` {.sh}
ssh-keygen -t ed25519 -C "ansible key"
ls -lrt  ~/.ssh/*
ssh-copy-id ~/.ssh/ed25519.pub 192.168.2.65
ssh-copy-id ~/.ssh/ed25519.pub 192.168.2.77

```


## First Command

``` {.sh}
ansible all --key-file ~/.ssh/ansible -i inventory  -m ping

```

## Gather Facts

``` {.sh}
ansible all -m gather_facts
ansible all -m gather_facts --limit  192.168.2.65
```
## Become Users

become allows us to elevate the privellege

``` {.sh}
ansible all -m  apt -a update_cache=true --become --ask-become-pass 
```