
---

# Zimbra Mail Server Automation

## Overview

This repository contains scripts and configuration files designed to automate user management and other essential tasks for the Zimbra Collaboration Server. Created with the goal of simplifying server administration, this project provides efficient and secure solutions for domain name management, user provisioning, and routine maintenance tasks.

## Project Details

- **Author**: Furqan Mushtaq Makhdoomi
- **Contact**: [furmak331@gmail.com](mailto:furmak331@gmail.com)
- **GitHub**: [furmak331](https://github.com/furmak331)
- **Domain Name**: Configured for use with a domain registered specifically for this project

## Features

- **Automated User Management**: Easily add, remove, and modify user accounts with a single command.
- **Domain Configuration**: Streamlined process to set up DNS records using dnsmasq.
- **Scheduled Backups**: Regular backup scripts to ensure data safety.
- **SSL Configuration**: Automated setup of SSL certificates for secure communication.
- **Health Monitoring**: Includes scripts to check server status and alert for potential issues.

## Getting Started

### Prerequisites

1. **Zimbra Collaboration Server**: Ensure Zimbra is installed on an Ubuntu 20.04 LTS server.
2. **dnsmasq**: Installed and configured for DNS management.
3. **Python 3.x**: Required for running the automation scripts.
4. **Shell (Bash)**: The scripts are designed to be executed in a Unix-like shell environment.

### Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/furmak331/zimbra-mail-automation.git
   cd zimbra-mail-automation
   ```

2. **Configure the Environment**:
   - Edit the `config.env` file to include your server details, domain name, and any other necessary configurations.
   - Update the DNS settings in `dnsmasq.conf` to match your domain setup.

3. **Run Setup Script**:
   ```bash
   bash setup.sh
   ```

4. **Set Up Scheduled Tasks**:
   - Use `cron` to schedule regular maintenance and backup tasks:
     ```bash
     crontab -e
     ```
   - Add the following line:
     ```bash
     0 2 * * * /path/to/backup.sh
     ```

### Usage

- **Add a New User**:
  ```bash
  ./manage_users.sh add <username> <password>
  ```
- **Remove a User**:
  ```bash
  ./manage_users.sh remove <username>
  ```
- **View Server Health**:
  ```bash
  ./health_check.sh
  ```

## Folder Structure

```plaintext
zimbra-mail-automation/
├── scripts/
│   ├── manage_users.sh
│   ├── health_check.sh
│   └── backup.sh
├── config/
│   ├── dnsmasq.conf
│   └── config.env
├── setup.sh
└── README.md
```

## Contribution

Contributions are welcome! Please fork the repository, create a feature branch, and submit a pull request. Be sure to follow the coding standards outlined in the CONTRIBUTING.md file.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by the need to streamline Zimbra server management tasks and reduce the manual workload.
- Special thanks to the open-source community for providing documentation and tools that made this automation possible.

---

