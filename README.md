# simple-Ansible-all_for_Linux

## Overview
This Ansible playbook is designed to set up a clean Ubuntu system with a standard set of tools and utilities commonly used in development, system administration, and server management. It automates the installation and basic configuration of various software packages, making the system ready for use or further customization.

## Prerequisites
- Ansible installed on the control machine.
- SSH access to the target Ubuntu machine(s).
- The target machine should be Ubuntu (preferably the latest version).
- User with sudo privileges on the target machine.

## Features
The playbook includes tasks to install the following:
- Basic utilities like `curl`, `wget`, `git`, `vim`, `nano`.
- Programming languages and tools such as `python3`, `pip`, `nodejs`, `npm`, `java`, `gcc`, `g++`.
- Web server and database (`nginx`, `mysql-server`).
- System monitoring tools (`htop`, `nmon`, `net-tools`).
- Security tools (`ufw`, `fail2ban`).
- Backup tool (`rsync`).
- Docker and Docker Compose.
- Ansible and Terraform.
- Terminal session multiplexers (`screen`, `tmux`).
- Archive utilities (`zip`, `unzip`, `tar`).

## Usage
1. Ensure you have Ansible installed on your control machine. If not installed, here are the installation instructions:
   ## Step 1: Update the Package List
   Before installing new software, it's always a good idea to update your package manager to ensure you have access to the latest versions. Open your terminal and run:
   ```bash
   sudo apt update
   ```
   ## Step 2: Install Software Properties Common (Optional)
   This step is necessary if you want to add a Personal Package Archive (PPA) to your system, which can provide more up-to-date versions of Ansible:
   ```bash
   sudo apt install software-properties-common
   ```
   ## Step 3: Add Ansible's Official PPA (Optional)
   For the latest version of Ansible, you can add its official PPA to your system. This step is optional, but recommended for getting the most up-to-date version:
   ```bash
   sudo add-apt-repository --yes --update ppa:ansible/ansible
   ```
   ## Step 4: Install Ansible
   Now, install Ansible using the apt package manager:
   ```bash
   sudo apt install ansible
   ```
   ## Step 5: Verify Installation
   After installation, you can verify that Ansible is correctly installed by checking its version:
   ```bash
   ansible --version
   ```
   This command will display the installed version of Ansible, confirming that the installation was successful.

3. Clone this repository or copy the playbook file to your control machine.
4. Set up your Ansible inventory with the target Ubuntu machine(s). Ansible inventory and playbooks are typically stored in an Ansible project directory that you create on your management node (the computer from which you run Ansible).
5. Run the playbook using the following command:
   ```bash
   ansible-playbook -i <your-inventory-file> setup-ubuntu.yml
   ```

Replace `<your-inventory-file>` with the path to your inventory file. The repository contains a sample inventory.ini file. You need to create your own file.

## Customization
You can customize the playbook by modifying the `setup-ubuntu.yml` file. Add or remove packages as per your requirements.

## Caution
- Always test the playbook in a non-production environment before using it on your main system.
- Some tasks might require a reboot or may restart services. Ensure you have proper backups and configurations in place.

## Contribution
Contributions to this playbook are welcome.

## License
MIT License

## Author
Akhrimov Ruslan

## Disclaimer
This playbook is provided "as is", without warranty of any kind, express or implied.

