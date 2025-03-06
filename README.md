# Born2beroot - A System Administration Challenge

Born2beroot is a project from the [42 São Paulo](https://www.42sp.org.br/) Common Core curriculum. It focuses on setting up and configuring a virtual machine to explore foundational system administration concepts using Debian or Rocky Linux.

![42 São Paulo](https://img.shields.io/badge/42-São_Paulo-black?style=flat-square&logo=42)

## About 42

[42 São Paulo](https://www.42sp.org.br/) is a tuition-free, global coding school dedicated to peer-to-peer learning and project-based education. This project introduces essential skills in server management and security.

## Project Overview

Born2beroot involves creating a secure virtual machine environment from scratch. The task requires installing and configuring an operating system (Debian or Rocky) with specific security and management features.

### Key Features
- Configures SSH access on port 4242 with root login disabled.
- Implements a strong password policy (e.g., minimum 10 characters, mixed case, numbers, no user-related words).
- Sets up `sudo` with strict logging and limited command execution (10 attempts max).
- Includes a monitoring script that broadcasts system stats (e.g., OS, hostname, users, CPU, memory) every 10 minutes via `wall`.
- Enforces security via UFW firewall and custom user management.

### Restrictions
- No graphical interface allowed; all work done via command line.
- Must adhere to specific partition layouts (e.g., separate `/var`, `/home`).
- No weak passwords or insecure configurations permitted.
- Requires full memory cleanup and proper system shutdown procedures.

## Getting Started

### Prerequisites
- Virtualization software (e.g., VirtualBox)
- Debian or Rocky Linux ISO

### Project Structure
- Virtual machine configuration files (specific to the chosen virtualization tool).
- Shell script for monitoring system status.
- System configuration files (e.g., `/etc/ssh/sshd_config`, `/etc/sudoers.d/`).

## License
This project is part of the 42 curriculum and intended for educational use.
