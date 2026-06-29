## Phase 2 – PXE Boot Infrastructure

## Overview

Preboot eXecution Environment (PXE) enables computers to boot and install an operating system from the network instead of local storage.

PXE is commonly used in enterprise environments to automate operating system deployment and reduce manual installation effort.

## PXE Workflow

1. Client powers on.
2. BIOS/UEFI selects Network Boot.
3. Client requests an IP address from the DHCP server.
4. DHCP provides an IP address, boot server address, and boot file name.
5. Client downloads the boot loader using TFTP.
6. The PXE boot menu is displayed.
7. The client downloads the Linux kernel and installation files using HTTP.
8. Operating system installation begins.

## Components Used

- DHCP Server
- TFTP Server
- HTTP Server
- PXE Boot Loader

## Benefits

- Automated operating system deployment.
- Centralized management.
- Faster provisioning.
- Consistent system configuration.
- Reduced manual effort.

## Industrial OT Example

PXE enables rapid deployment of engineering workstations, maintenance laptops, and test systems while ensuring standardized operating system installations across industrial environments.
