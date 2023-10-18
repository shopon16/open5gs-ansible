Network Information
===========

Interface Name  | Protocol
-------------   | -------------
eth1            | internet
eth2            | S1AP

Requirements
-------------
* Ubuntu 20.04
* Ansible 2.10.8
* Vagrant 2.2.19
* MongoDB:		6.0.11
* Mongosh:		2.0.2

VM provisioning
-------------
create a vagrant machine with Vagrantfile which in root directory. this EPC core is deployed to ubuntu 20. please use ubuntu 20 otherwise you break some code.

update ip address in Vagrantfile for internet and s1ap with your corresponding setup.
```console
vagrant up
vagrant ssh-config
```
 Now update your hosts file (ansible_port and ansible_ssh_private_key_file) with the value you got from vagrant ssh-config command
## check if you are getting ip from your interfaces
```
ansible-playbook ./open5gs/test/debug.yaml -i hosts
```
```console
ansible all -m ping -i hosts
```
if got success output it means your machine is reachable.
you can also use debug.yaml file with your need.

To deploy go to each role and follow instructions

## Acess your machine and investigate
```
vagrant ssh
```
if your radio is configured with 192.168.200.0/24 subdomain and if is pointed to S1AP mme 192.168.200.202, radio should be connected and you will get a LTE system up and running