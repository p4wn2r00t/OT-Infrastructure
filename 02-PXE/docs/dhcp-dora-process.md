# DHCP DORA Process

## Overview

DHCP assigns IP addresses using a four-step exchange known as DORA.

### 1. Discover

The client broadcasts a DHCP Discover message to locate a DHCP server.

### 2. Offer

The DHCP server offers an available IP address and network configuration.

### 3. Request

The client requests the offered IP address.

### 4. Acknowledge

The DHCP server confirms the lease, allowing the client to use the assigned IP address.

## Importance in PXE

Before a PXE client can download a boot file, it must first receive an IP address through the DHCP DORA process.
