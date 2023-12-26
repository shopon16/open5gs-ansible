Role Name
===========

This roles intalls EPC core all in one and also configures it.

Requirements
-------------
* Ubuntu 22.04
* Ansible 2.10.8
* MongoDB:		6.0.11
* Mongosh:		2.0.2

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

Dependencies
------------

Example Playbook
----------------
    - hosts: dev
      become: true
      roles:
         - open5gs
      gather_facts: true

License
-------

BSD

Author Information
------------------
**Author**: Md Omar Faruque Swapon

[swapon.sust.eee@gmail.com](mailto:swapon.sust.eee@gmail.com)

