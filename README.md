# __Virtual Host - Ansible - Apache2__
__Description__
This repository contain the method to automate of
installation and configuration of server web apache2
in another machine is done through the use of ssh and
ansible

&nbsp;
## Setup 1 : Clone this repository
```sh
git clone https://github.com/Daris02/virtualhost-apache2-sys1.git
```

&nbsp;
## Setup 2 : Install  Ansible
Use doc in this link : [install ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

&nbsp;
## Setup 3 : Launch Playbook

- Check ssh connection with your hosts is already exist

![alt-img](/image/ssh_connection2.png)

- Change the `ansible_ssh_host` in _inventory.yml_ to your personnal host ip address

![alt-img](/image/inventory.png)

&nbsp;
- Run this command to check your ansible connection ssh
```sh
ansible all -i inventory.yml -m ping
``` 

- Run this command to launch automate configuration in your machine and enter your password (of host managed)
```sh
ansible-playbook -i inventory.yml playbook.yml --ask-become-pass -k
```
__NOTE__
>-i : to indicate the inventory 

>-k : to etablish the SSH connection

>--ask-become-pass : to get the authorization like root (sudo) while the launch all playbook

