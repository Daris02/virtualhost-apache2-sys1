# __Virtual Host - Ansible - Apache2__
### __Description__
This repository contain the method to automate of
installation and configuration of server web apache2
in another machine is done through the use of ssh and
ansible

### __`NOTE`__ :
Ansible can be used by `only` linux distributions or 
macOS ``NOT Microsoft Windows``

## __Setup 1 : Install  Ansible__
Use doc in this link : [install ansible](https://ansible.org/install)

## __Setup 2 : Configuration of Ansible__
1.  Create your personnal inventory in yml or text
> TXT
<!-- ```txt
[control]
192.168.67.129  ansible_connection=local

[managed]
192.168.67.215
``` -->

>YAML
<!-- ```yaml
all:
  hosts:
    192.168.67.129:
      ansible_connection: local
  children:
    webservers:
      hosts:
        192.168.67.215:
``` -->

For verify your ansible is already
```sh
ansible all -i inventory.yml -m ping
``` 
<!-- output: ![alt-img](/image/img1.png) -->

2.  Create your personnal playbook to execute all command
