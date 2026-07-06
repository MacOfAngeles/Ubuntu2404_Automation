## 🚀Info

This repository demonstrates the fast deployment of Ubuntu 24.04.4 LTS.

The system is intended to run dockers for train signalings environments in Switzerland.

Supports deployment in two network segments with fully automatic configuration and no manual handling required.

<img width="1897" height="1100" alt="613365534-b36dc9a3-ae53-4d15-b75f-d8c5596132b2" src="https://github.com/user-attachments/assets/3a623abf-87a1-4029-9eca-baa0371b5f3b" />


## Steps and Information
1. Offline Ubuntu Noble 24.04 Zero-Touch Installation with cloud-init
    - Use our own offline mirror
    - Perform a minimal desktop installation
    - Keep the system as minimal as possible; install only what is truly required
    - Configure VNC with the Xfce desktop environment using tightvncserver for remote desktop access
2. Configure Hostname and Static IP Address with Python
    - Run the Python script with sudo privileges only
3. Set Up the Test Environment with Ansible
4. Install Docker and Docker Compose
    - Enable SSH communication between containers
5. Privacy and Security Notice
    - 🔒For privacy and security reasons, some parts of this repository have been removed or modified

## 🛠Usage Guide
1. Variables for configurations
    - user_data (IP address for mirror, password)
    - init_py (DNS address, Domain)
    - ansible/group_vars/all.yml (all ansible variables)
2. Perform the automated installation using cloud-init
3. Log in with the user account: tool
4. Run sudo /init/init.py to configure the hostname and IP address
5. Execute the Ansible playbook [readme.de ansible](https://github.com/MacOfAngeles/Ubuntu2404_Automation/tree/main/ansible)

The installation is complete and the system is ready to use
