# Ansible System Setup

This repository provides a fully automated setup for Ubuntu OS 24.04.4 LTS using Ansible.
The system is designed for train signal simulation and runs the required applications within Docker containers.
Key Features:
- Automated operating system installation and configuration
- Deployment managed entirely via Ansible
- Containerized environment using Docker
- Ready-to-use system with no additional configuration required after setup

User Accounts - The system includes the following predefined users:
- admin – administrative User-access
- tool – administrative OT-support
- user_docker – end user for operating Docker-based applications

Network Configuration:
- Supports to run in two network sections

Delivery State - After execution of the automation scripts:
- The PC is fully configured and operational
- No further setup steps are required
- The system is ready for lab use or customer delivery

## Features
- User management
- OS configuration
- Desktop setup (XFCE)
- Network + DNS configuration
- Firefox offline install
- VNC setup
- Certificates
- Simulation environment
- System tuning

👉 Requirements
- Ansible >= 2.12
- Linux Unbuntu 24.04.4 LTS (Noble Numbat)

## Usage

```bash
ansible-playbook playbooks/site.yml -i inventory/hosts.yml

📦 Full Ansible Repository Structure
03_ansible/
├── ansible.cfg
├── inventory/
│   └── hosts.yml
│
├── group_vars/
│   └── all.yml
│
├── playbooks/
│   └── site.yml
│
├── roles/
│
│   ├── os_start_installation/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── os_app_and_mirror/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── os_ntp/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── os_dns/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── os_fstab/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── os_users/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── os_mount_folders/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── os_ssh/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── os_vnc4server/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── os_desktop/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── os_plf/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── os_certificates/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── os_firefox/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── ve_patching/
│   │   └── tasks/
│   │       └── main.yml
│
│   ├── os_reboot/
│   │   └── tasks/
│   │       └── main.yml
│
└── README.md