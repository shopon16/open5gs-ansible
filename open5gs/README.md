Role Name
===========

This roles will intall open5gs EPC core and configure network configuration for attaching radio.

Requirements
-------------
* Ubuntu 20.04
* Ansible 2.10.8
* Vagrant 2.2.19
* MongoDB:		6.0.11
* Mongosh:		2.0.2

Role Variables
--------------
Parameter     | Value
------------- | -------------
MCC           | 001
MNC           | 01

Dependencies
------------


Example Playbook
----------------

    - hosts: all
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

