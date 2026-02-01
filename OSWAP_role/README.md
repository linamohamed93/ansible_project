dependency_check_role
=====================

Installs OWASP Dependency-Check on Linux hosts.
This role downloads the specified version, unpacks it to a directory, and creates a global symlink so the dependency-check command can be run from anywhere.

Requirements
============

1- Linux OS (Ubuntu, Debian, etc)

2- Internet access to download the Dependency-Check zip file

3- wget and unzip installed (the role installs them if missing)

Role Variables
===============

The following variables are available in defaults/main.yml and can be overridden:

# Version of Dependency-Check to install
depcheck_version: "8.4.1"

# Directory where Dependency-Check will be installed
install_dir: "/opt/dependency-check"

Dependencies
=============
java.

Example Playbook
================
- hosts: dev_servers
  become: yes
  roles:
    - role: dependency_check_role
      vars:
        depcheck_version: "8.4.1"
        install_dir: "/opt/dependency-check"

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
