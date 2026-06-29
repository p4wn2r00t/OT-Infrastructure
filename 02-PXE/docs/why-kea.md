# Why Kea DHCP?

## Overview

Kea DHCP is the modern Dynamic Host Configuration Protocol (DHCP) server developed by ISC. It replaces the legacy ISC DHCP Server and provides a scalable, actively maintained platform for IP address management.

## Why Kea?

The OT Infrastructure Lab uses Kea DHCP because it offers:

- Modern JSON-based configuration.
- Active development and maintenance.
- Improved scalability.
- REST API support.
- Better logging and monitoring capabilities.
- Enterprise-ready architecture.

## Role in the PXE Infrastructure

## Kea performs two critical tasks:

1. Assigns an IP address and other network configuration to PXE clients.
2. Provides PXE-specific information, including the boot server address and boot file name.

Without DHCP, a PXE client cannot discover the PXE server or begin the network boot process.

Relation to This Project

In this lab, Kea DHCP runs on the Ubuntu infrastructure server and supports automated PXE boot for newly deployed virtual machines.
