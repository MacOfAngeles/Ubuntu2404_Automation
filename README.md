## Info

This repository demonstrates the fast deployment of Ubuntu 24.04.4 LTS.

The system is intended to run dockers for train signalings environments in Switzerland.

Supports deployment in two network segments with fully automatic configuration and no manual handling required.


<img width="1266" height="606" alt="451425445-8441bc7a-ecab-4555-b615-0ce1d9ff8904" src="https://github.com/user-attachments/assets/16b6e847-3150-4a3c-931a-0ddca346945f" />

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
- For privacy and security reasons, some parts of this repository have been removed or modified

## Usage Guide
1. Variables for configurations
- 01_ubuntu_user_data.txt (IP address for mirror, password)
- 03_ansible/group_vars/all.yml (all ansible variables)
2. Perform the automated installation using cloud-init
3. Log in with the user account: tool
4. Run sudo /init/init.py to configure the hostname and IP address
5. Execute the Ansible playbook 03_ansible/readme.md

The installation is complete and the system is ready to use