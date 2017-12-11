# Ansible-Playbook tomcat-mysql for SIT Agile 
Give and Take: Agile for Software Development in Action for Academic
[![ALCHEMISTCLUB](https://upic.me/i/o1/22141155_1886011418083364_1525842233310280391_n.png )](https://www.facebook.com/alchemistitbangmod/)

# Requirements

  - Clean CentOS 7 for deployment (specify in host file)
  - CentOS7 with ansible-playbook Package

### Installation
Install the dependencies on ansible master

```sh
$ yum install epel-release -y
$ yum install ansible -y
$ git clone https://github.com/alchemist-itbangmod/ansibleplaybook-sitagile
$ cd ansibleplaybook-sitagile/tomcat-mysql/
```
edit hosts located in ansibleplaybook-sitagile/tomcat-mysql/hosts file with ssh user and password for deployment server
```sh
[tomcat-servers]
10.4.56.70  ansible_connection=ssh  ansible_user=root   ansible_ssh_pass='password'
10.4.56.71  ansible_connection=ssh  ansible_user=root   ansible_ssh_pass='password'
10.4.56.72  ansible_connection=ssh  ansible_user=root   ansible_ssh_pass='password'
10.4.56.73  ansible_connection=ssh  ansible_user=root   ansible_ssh_pass='password'
```
start deploy node
```sh
$ ansible-playbook -i hosts site.yml -v
```