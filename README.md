Requirements
-------------
* Ubuntu 22.04
* Ansible 2.10.8
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
## check if you can access your server

```console
ansible all -m ping -i hosts
```
if got success output it means your machine is reachable.

To deploy run this command on root folder where deploy.yaml exists
```
ansible-playbook deploy.yaml -i hosts.yaml
```

## Acess your machine and investigate
```
vagrant ssh
```

Role Variables
--------------
make sure you change the variables according to your needs
Parameter     | Value
------------- | -------------
MCC           | 001
MNC           | 01
s1ap_ip       | 192.168.0.97
s1ap_ip       | 192.168.0.97
centraldb_ip  | 192.168.0.97
exec_path     | "/usr/local/bin"
source_dir    | "/home/vagrant"


if your radio is configured with 192.168.200.0/24 subdomain and if is pointed to S1AP mme 192.168.200.202, radio should be connected and you will get a LTE system up and running