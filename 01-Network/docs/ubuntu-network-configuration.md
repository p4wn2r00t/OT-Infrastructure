# Ubuntu Server Network Configuration

## Overview

The Ubuntu Infrastructure Server is configured with two network interfaces.

### Interface 1 (ens33)

- Purpose: Internet Connectivity
- Network Type: VMware NAT
- IP Assignment: DHCP

### Interface 2 (ens37)

- Purpose: OT Network
- Network Type: VMware Host-Only (VMnet2)
- IP Address: 192.168.100.10/24
- Configuration: Static

## Why Two Interfaces?

Using separate interfaces isolates OT traffic from the Internet while allowing the infrastructure server to download updates and software packages.

This architecture follows common industrial network segmentation practices.
