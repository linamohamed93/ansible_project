# ansible_project
Ansible Project: Multi-Role Setup

This project contains several Ansible roles to install and configure key developer and security tools, including Nexus Repository, OWASP Dependency-Check, Trivy, and Node.js via NVM.
All roles are ready to be used in CI/CD pipelines or on Linux hosts.

Roles Overview
===============
1. Nexus_role
   ==========

Installs Sonatype Nexus Repository Manager OSS (3.x) as a container/pod.
The role pulls the official Nexus image and runs it with default settings.

Requirements:

1-Docker  installed on target host

2- Linux OS

3- Internet access to pull Nexus image

3- Variables: None

2. dependency_check_role
==============================

Installs OWASP Dependency-Check on Linux hosts.
Downloads the specified version, unpacks it, and sets up a global symlink for easy use.

Requirements:

1-Linux OS (Debian/Ubuntu recommended)

2-Internet access

3-wget and unzip (installed automatically)

Variables:

depcheck_version: "8.4.1"
install_dir: "/opt/dependency-check"




3. trivy_role
   ============

Installs Trivy vulnerability scanner via the official APT repository.

Requirements:

1- Linux OS: Debian/Ubuntu

2- Internet access

Variables: None


4. nodejs_role
================

Installs NVM (Node Version Manager) and a specific Node.js version.
Removes existing Node.js, installs dependencies, sets up NVM, and installs Node.js.

Requirements:

1- Linux OS (Debian/Ubuntu recommended)

2- Internet access

3- Required packages installed automatically: curl, build-essential, libssl-dev, software-properties-common, gnupg, ca-certificates

Variables:

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
Shyama saeed— GitHub: linamohamed93/ansible_project
