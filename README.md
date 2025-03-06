# Born2beroot - A System Administration Challenge

Born2beroot is a project from the [42 São Paulo](https://www.42sp.org.br/) Common Core curriculum. It centers on configuring a secure virtual machine using Debian or Rocky Linux, providing hands-on experience with foundational system administration and security practices.

![42 São Paulo](https://img.shields.io/badge/42-São_Paulo-black?style=flat-square&logo=42)

## About 42

[42 São Paulo](https://www.42sp.org.br/) is a tuition-free, global coding school committed to peer-to-peer learning and project-based education. This project builds critical skills in server setup, user management, and system hardening.

## Project Overview

Born2beroot requires setting up a virtual machine from scratch with a chosen operating system (Debian or Rocky Linux). It emphasizes security and monitoring, split into:
- **Mandatory Part**: Establishes a secure server with SSH, `sudo`, and a monitoring script.
- **Bonus Part**: Adds advanced features, including additional service configuration (e.g., WordPress with Nginx or lighttpd, MariaDB) and an extra security tool beyond UFW (e.g., Fail2Ban or custom cron job), enhancing the system's functionality and protection.

### Key Features

- Configures SSH on port 4242, disabling root login for enhanced security.
- Enforces a robust password policy: minimum 10 characters, mixed case, numbers, special characters, and no user-related terms.
- Sets up `sudo` with strict rules: logs all commands, limits to 10 failed attempts, requires custom message on misuse.
- Includes a monitoring script running every 10 minutes via cron, broadcasting stats (e.g., OS, hostname, users, CPU/memory usage, disk space) using `wall`.
- Secures the system with UFW firewall, allowing only port 4242.
- Bonus:
  - Setup partitions manually (like the structure below).
  - Set up a functional WordPress website with lighttpd, MariaDB and PHP.
  - Set up a service of your choice (NGINX / Apache2 excluded). I chose LiteSpeed.

![image](https://github.com/user-attachments/assets/986823de-c401-4faa-8460-6332762072a3)

### Restrictions

- No graphical interface permitted; all configuration via command line.
- Requires specific disk partitions (e.g., separate `/var`, `/home`, encrypted LVM for Rocky).
- Prohibits weak passwords and insecure settings (e.g., unchanged defaults).
- Mandates proper memory cleanup and system shutdown procedures.
- Bonus must maintain mandatory security standards while adding services.

## Getting Started

### Prerequisites

- Virtualization software (e.g., VirtualBox).
- Debian or Rocky Linux ISO.

## Project Structure

- Virtual machine configuration files (specific to the virtualization tool).
- Shell script for system monitoring (`monitoring.sh`).
- Configuration files: `/etc/ssh/sshd_config` (SSH), `/etc/sudoers.d/` (sudo), `/etc/ufw/` (firewall).
- Bonus: web server files (e.g., Nginx/lighttpd configs), MariaDB setup, additional security tool configs.

## License

This project is part of the 42 curriculum and intended for educational use.
