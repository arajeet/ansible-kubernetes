#Ansible  Kubernetes

## First Command

``` {.sh}
ansible all --key-file ~/.ssh/ansible -i inventory  -m ping

```

## Gather Facts

``` {.sh}
ansible all -m gather_facts
ansible all -m gather_facts --limit  192.168.2.65
```