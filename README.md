mamercad.mariadb-galera
=======================

Stands up MariaDB 10.1.11 (and Galera) on RHEL/CentOS

Warnings
--------

The role puts SELinux into permissive mode and disabled firewalld

Requirements
------------

None

Role Variables
--------------

See the example inventory below...

Dependencies
------------

None

Example Inventory
-----------------

    [mariadb]
    mariadb1 primary=mariadb1 role=primary
    mariadb2 primary=mariadb1 role=nonprimary
    mariadb3 primary=mariadb1 role=nonprimary

    [mariadb:vars]
    ansible_ssh_user=root

Example Playbook
----------------

    - hosts:
        - mariadb
      roles:
        - mamercad.mariadb-galera

License
-------

GPLv3

Author Information
------------------

Mark Mercado <mamercad@umflint.edu>

