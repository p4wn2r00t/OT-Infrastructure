# Kea Directory Structure

## Overview

The Kea DHCP configuration is stored under `/etc/kea`.

## Important Files

### kea-dhcp4.conf

Primary configuration file for IPv4 DHCP services.

Responsibilities:

- IP address pools
- Subnets
- Lease timers
- PXE boot options
- DHCP options

### kea-dhcp6.conf

Configuration file for IPv6 DHCP.

Not used in this project.

### keactrl

Configuration for the Kea Control Agent, which provides REST API access for management and automation.
