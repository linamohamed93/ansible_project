Nexus_role
==========

Installs Sonatype Nexus Repository Manager as a container using Docker .
This role pulls the official Nexus image and runs it with customize settings.

Requirements
============

1- Target host must have Docker or Podman installed.

2- Linux OS (Ubuntu, Debian, CentOS, etc).

3- Internet access to pull the Nexus image.

Role Variables
==============

This role does not have any variables. All settings are default.

Dependencies
=============

Install Docker

Example Playbook
================
- hosts: nexus_servers
  become: yes
  roles:
    - role: Nexus_role

License
=======

BSD

Author Information
==================

Lina Mohamed
Ashgan Adel
Merna Athawy
shayma saeed
— GitHub: linamohamed93/ansible_project
