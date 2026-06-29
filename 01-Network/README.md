# Phase 1 - Network Infrastructure

## Introduction

Computer networking is the foundation of every modern IT and OT environment. Before deploying services such as PXE Boot, DHCP, TFTP, SCADA, or OT Security monitoring, a reliable and properly designed network infrastructure must be established.

This phase focuses on building a secure virtual network using VMware Workstation. The environment consists of Ubuntu Server, SCADA Server, and OT-SOC Server connected through NAT and Host-Only virtual networks.

The networking configuration provides Internet access where required while maintaining an isolated OT network for secure communication between industrial systems.

---

# What is a Computer Network?

A computer network is a collection of devices connected together to exchange information and resources.

In this lab, the network enables communication between:

- Ubuntu Server
- SCADA Server
- OT-SOC Server

This networking foundation will support all future phases of the project, including PXE Boot, DHCP, TFTP, HTTP, and OT Security Monitoring.
