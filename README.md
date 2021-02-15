# master_conf
master_conf
=========

This role should be applied after master-instance role. It will run all necessary commands for master configuration and master will be in READY state. 

Requirements
------------

Pre-requirements for this are your dynamic inventory should be ready and configuration file should be working. Also boto library need to be installed.

Role Variables
--------------

There are no role variables

Dependencies
------------

Other roles required are master-instance, slave-instance, slave_conf

Example Playbook
----------------

    - hosts: k8s_master_an
      roles:
         - master_conf
