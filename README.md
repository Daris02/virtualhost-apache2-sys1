# __Virtual Host - Ansible - Apache2__
__Description__

This repository contain the method to automate of
installation and configuration of server web apache2
in another machine is done through the use of ssh and
ansible

&nbsp;
## Setup 1 : Install  Ansible
Use doc in this link [Install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) and for more doc. 

&nbsp;
## Setup 2 : Clone this repository
**If need a template for your project**
```sh
git clone https://github.com/Daris02/virtualhost-apache2-sys1.git
```

&nbsp;
## Setup 3 : Launch Ansible

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

## Final result

[ansiblePlaybook.webm](https://github.com/Daris02/virtualhost-apache2-sys1/assets/103503966/7bcb14a5-be36-42e7-96e0-af11b7f688eb)

[ResultKali.webm](https://github.com/Daris02/virtualhost-apache2-sys1/assets/103503966/355ab29a-2c06-4799-b8b6-41933232bf10)

