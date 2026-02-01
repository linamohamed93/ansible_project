nodejs_role
===============

Installs NVM (Node Version Manager) and a specific Node.js version on Linux hosts.
This role removes any existing Node.js installation, installs required dependencies, sets up NVM, and installs Node.js.

Requirements
============

1- Linux OS (Ubuntu/Debian recommended)

2- Internet access to download NVM and Node.js

3- curl, build-essential, libssl-dev, software-properties-common, gnupg, and ca-certificates (installed automatically by the role)

Role Variables
===============

The following variables are available in defaults/main.yml:

1-  Version of NVM to install==> nvm_version: "v0.39.6"


2- Node.js version to install via NVM==>node_version: "14"

You can override these variables in your playbook or using host_vars/group_vars.

Dependencies
============

None.

Example Playbook
================
- hosts: dev_servers
  become: yes
  roles:
    - role: nvm_nodejs_role
      vars:
        nvm_version: "v0.39.6"
        node_version: "14"

License
========

BSD

Author Information
==================

Lina Mohamed 
Ashgan Adel
Merna Athaway
Shayma Saeed— GitHub: linamohamed93/ansible_project
