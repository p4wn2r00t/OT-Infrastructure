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


Why VMware?

Building a physical OT infrastructure requires multiple servers, networking equipment, and industrial devices, making it expensive and difficult to maintain for learning purposes.

VMware Workstation provides a virtual environment where multiple systems can be deployed on a single physical computer. This allows the entire OT infrastructure to be designed, tested, modified, and restored without affecting production systems.

Using VMware also makes it possible to simulate enterprise networking, server deployments, and OT communication in a safe and controlled environment.

Advantages of VMware

- Deploy multiple virtual machines on one computer.
- Simulate enterprise network topologies.
- Practice networking without physical hardware.
- Take snapshots and restore virtual machines.
- Safely perform testing and troubleshooting.
- Build a realistic OT Security lab.

## Virtual Networking

Virtual networking allows multiple virtual machines to communicate with each other without requiring dedicated physical networking equipment.

Instead of using physical switches, routers, and Ethernet cables, VMware creates software-based networking components called virtual switches and virtual networks (VMnets).

Each VMnet represents a separate virtual network that can be configured for different purposes, such as Internet access, isolated communication, or custom network segmentation.

Physical Network

A physical network consists of physical devices such as routers, switches, cables, and computers.

Virtual Network

A virtual network performs the same function as a physical network but is completely software-defined inside VMware Workstation.

VMnet

VMnet is VMware's virtual network. Each VMnet represents an independent network where virtual machines can communicate according to its configuration.

### In this project:

- VMnet8 is used as the NAT network.
- VMnet2 is used as the isolated OT Host-Only network.


# VMware Network Modes

VMware provides multiple networking modes that determine how virtual machines communicate with the host computer, other virtual machines, and external networks.

## NAT (Network Address Translation)

NAT allows virtual machines to access the Internet by using the host computer as an intermediary. The virtual machine can download updates and software while remaining hidden from the physical network.

In this project, NAT is used to provide Internet access to the Ubuntu Server and OT-SOC Server.

## Bridged Networking

Bridged mode connects a virtual machine directly to the physical network. The virtual machine behaves like an independent physical computer and receives its own IP address from the physical network.

## Host-Only Networking

Host-Only networking creates an isolated private network between the host and selected virtual machines. This mode is commonly used to simulate secure internal environments such as OT networks.

In this project, VMnet2 is configured as a Host-Only network to allow secure communication between Ubuntu Server, SCADA Server, and OT-SOC Server.

## Custom VMnet

Custom VMnets allow administrators to create dedicated virtual networks with their own IP addressing and communication rules. This provides flexibility when designing complex virtual infrastructures.

The OT network in this project is implemented using a custom Host-Only VMnet (VMnet2).


Multiple Network Interfaces

The Ubuntu Server is configured with two network interfaces, each serving a different purpose.

Interface 1 - NAT Network

The first interface provides Internet connectivity through VMware NAT. It is used to download software packages, security updates, and other external resources.

Interface 2 - Host-Only Network

The second interface is connected to the isolated OT network (VMnet2). This interface enables secure communication between the Ubuntu Server, SCADA Server, and OT-SOC Server without exposing OT traffic to the Internet.

Using separate interfaces for IT and OT communication reflects common network segmentation practices used in industrial environments.


# IP Address Planning

A structured IP addressing scheme was implemented to simplify network management and future expansion.

Two separate IP networks are used in this lab:

- 172.16.67.0/24 – VMware NAT network providing Internet connectivity.
- 192.168.100.0/24 – Host-Only OT network used for secure communication between industrial systems.

IP Address Allocation

Virtual Machine| Interface| IP Address| Purpose
Ubuntu Server| NAT| 172.16.67.134| Internet Access
Ubuntu Server| VMnet2| 192.168.100.10| OT Communication
SCADA Server| VMnet2| 192.168.100.20| Industrial Control System
OT-SOC Server| NAT| 172.16.67.128| Internet Access
OT-SOC Server| VMnet2| 192.168.100.30| OT Security Monitoring

This structured addressing scheme improves readability, simplifies troubleshooting, and allows additional OT devices to be integrated without redesigning the network.
