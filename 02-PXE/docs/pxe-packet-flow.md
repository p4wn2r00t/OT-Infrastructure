## PXE Boot Packet Flow

## Overview

PXE Boot is a multi-stage network boot process that enables a client computer to start an operating system installation without using local storage.

Understanding the packet flow simplifies troubleshooting and explains how DHCP, TFTP, and HTTP work together.

## PXE Boot Sequence

1. Client powers on and selects Network Boot.
2. Client broadcasts a DHCP Discover message.
3. DHCP Server responds with an IP address, boot server address, and boot file name.
4. Client requests the offered configuration.
5. DHCP Server acknowledges the lease.
6. Client contacts the TFTP server and downloads the PXE boot loader ("pxelinux.0").
7. The PXE boot menu is displayed.
8. The client downloads the Linux kernel and installation files from the HTTP server.
9. The operating system installer starts.

## Troubleshooting

- No IP Address → Check DHCP Server.
- Boot File Missing → Verify DHCP boot file configuration.
- TFTP Download Failure → Check TFTP service and file permissions.
- PXE Menu Missing → Verify PXE boot loader files.
- Installation Failure → Verify HTTP server and installation repository.

## OT Example

This workflow enables centralized deployment of operating systems for engineering workstations and maintenance systems, reducing manual installation time and ensuring standardized configurations across industrial environments.
