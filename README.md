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
1. Ensure you have Ansible installed on your control machine.
2. Clone this repository or copy the playbook file to your control machine.
3. Set up your Ansible inventory with the target Ubuntu machine(s).
4. Run the playbook using the following command:
   ```bash
   ansible-playbook -i <your-inventory-file> setup-ubuntu.yml
   ```

Replace `<your-inventory-file>` with the path to your inventory file.

## Customization
You can customize the playbook by modifying the `setup-ubuntu.yml` file. Add or remove packages as per your requirements.

## Caution
- Always test the playbook in a non-production environment before using it on your main system.
- Some tasks might require a reboot or may restart services. Ensure you have proper backups and configurations in place.

## Contribution
Contributions to this playbook are welcome. Please fork the repository and submit a pull request with your suggested changes.

## License
MIT License

## Author
Akhrimov Ruslan

## Disclaimer
This playbook is provided "as is", without warranty of any kind, express or implied.

