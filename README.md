# __Virtual Host - Ansible - Apache2__
### __Description__
This repository contain the method to automate of
installation and configuration of server web apache2
in another machine is done through the use of ssh and
ansible

### __`NOTE`__ :
Ansible can be used by `only` Linux distributions or 
MacOS ``NOT Microsoft Windows``. So you need computer under Linux the following of this project

&nbsp;
## Setup 1 : Clone this repository
```sh
git clone https://github.com/Daris02/virtualhost-apache2-sys1.git
```

&nbsp;
## Setup 2 : Install  Ansible
Use doc in this link : [install ansible](https://ansible.org/install)

&nbsp;
## Setup 3 : Launch Ansible

- Change the IP Address in `inventory.yml` and `playbook.yml` to your personnal hosts IP

- Run this command to check your ansible function
```sh
ansible all -i inventory.yml -m ping
``` 
<!-- output: ![alt-img](/image/img1.png) -->

- Run this command to launch automate configuration in your machine and enter your password (of host managed)
```sh
ansible-playbook -i inventory.yml playbook.yml --ask-become-pass -k
```
-i : to indicate the inventory 

-k : to etablish the SSH connection

--ask-become-pass : to get the authorization like root (sudo) while the launch all playbook

