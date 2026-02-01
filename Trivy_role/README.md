trivy_role
==========

Installs Trivy, the vulnerability scanner for containers and filesystems, on Debian/Ubuntu systems.
This role adds the official Trivy APT repository, installs required dependencies, and ensures Trivy is available system-wide.

Requirements
============

1- Linux OS: Debian/Ubuntu

2- Internet access to download Trivy packages

3- wget, gnupg, and lsb-release packages (installed automatically by the role)

Role Variables
==============

This role does not have any variables. All installation settings are default.

Dependencies
============

None.

Example Playbook
================
- hosts: security_servers
  become: yes
  roles:
    - role: trivy_role

License
========

BSD

Author Information

Lina Mohamed 
Ashgan Adel
Merna Athawy
shayma saeed
— GitHub: linamohamed93/ansible_project
