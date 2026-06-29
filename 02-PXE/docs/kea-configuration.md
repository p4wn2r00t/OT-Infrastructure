# Understanding Kea DHCP Configuration

## Overview

The primary configuration file for Kea DHCP is:

```text
/etc/kea/kea-dhcp4.conf
```

This file is written in JSON format and defines how the DHCP server behaves.

## Important Sections

### Dhcp4

The top-level object containing all IPv4 DHCP configuration.

### interfaces-config

Specifies which network interfaces Kea listens on.

Example:

- ens37 (Host-Only OT Network)

### lease-database

Stores information about active DHCP leases, allowing Kea to track assigned IP addresses.

### subnet4

Defines the IPv4 subnet managed by the DHCP server.

Example:

- 192.168.100.0/24

### pools

Defines the range of dynamically assignable IP addresses.

Example:

- 192.168.100.100 – 192.168.100.200

## Design Considerations

Static infrastructure devices such as the Ubuntu PXE Server, SCADA Server, and OT-SOC Server use fixed IP addresses outside the DHCP pool to prevent address conflicts.
