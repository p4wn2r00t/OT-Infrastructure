# Phase 3 – DHCP Server

## Overview

The Dynamic Host Configuration Protocol (DHCP) automatically assigns IP addresses and network configuration information to client devices.

In this project, the Ubuntu Server will later be configured as a DHCP server to support PXE Boot and automated client provisioning.

## Why DHCP?

DHCP eliminates the need to manually configure IP addresses for every client.

It provides:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

## DHCP Communication (DORA)

Every DHCP client follows the DORA process:

1. Discover – The client searches for a DHCP server.
2. Offer – The DHCP server offers an available IP address.
3. Request – The client requests the offered address.
4. Acknowledge – The DHCP server confirms the lease.

## OT Considerations

Critical OT systems such as PLCs and SCADA servers typically use static IP addresses for stability and predictable communication.

DHCP is commonly used for engineering workstations, temporary systems, and automated deployment environments such as PXE Boot.
