# Kea DHCP Installation

## Overview

Kea DHCP is the DHCP server used in this OT Infrastructure Lab. It assigns IP addresses to PXE clients and provides boot information required for network boot.

## Installation

Update the package repository:

```bash
sudo apt update
```

Install the Kea DHCP server:

```bash
sudo apt install kea-dhcp4-server -y
```

## Verify Installation

Check the installed version:

```bash
kea-dhcp4 -V
```

Check the service status:

```bash
sudo systemctl status kea-dhcp4-server
```

Enable automatic startup:

```bash
sudo systemctl enable kea-dhcp4-server
```

## Important Directories

- `/etc/kea/` – Configuration files
- `/usr/sbin/` – Program binaries
- `/var/log/` – Log files

## Purpose

The Kea DHCP server provides:

- IP address assignment
- Network configuration
- PXE boot server information
- Boot filename for PXE clients
