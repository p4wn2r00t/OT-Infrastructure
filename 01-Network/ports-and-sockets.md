# Ports and Sockets

## Overview

An IP address identifies a device on a network, while a port identifies a specific service running on that device.

This allows multiple applications to communicate simultaneously using the same IP address.

## Common Ports Used in This Project

| Service| Port| Protocol |
|--------|-----|----------| 
|SSH| 22| TCP |
| HTTP| 80| TCP |
| HTTPS| 443| TCP |
| DHCP Server| 67| UDP |
| DHCP Client| 68| UDP |
| TFTP| 69| UDP |

## What is a Socket?

A socket is the combination of an IP address and a port number.

Example:

- 192.168.100.10:22 → SSH Service
- 192.168.100.10:80 → HTTP Service

Sockets uniquely identify communication endpoints between clients and servers.

## Linux Commands

Display listening ports:

ss -tulpn

Display active connections:

ss -tun

## OT Example

Engineering Workstations communicate with infrastructure services through well-known ports.

Understanding port usage is essential for configuring firewalls, troubleshooting connectivity, and monitoring network traffic in OT environments.
