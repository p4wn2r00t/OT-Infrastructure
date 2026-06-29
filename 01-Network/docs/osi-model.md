# OSI Model

## Introduction

The Open Systems Interconnection (OSI) Model is a conceptual framework used to understand how data travels across a network.

Each layer performs a specific function during communication.

---

## OSI Layers

Layer 7 - Application

Provides services to applications such as SSH, HTTP, HTTPS, DNS, and Ping.

---

Layer 6 - Presentation

Responsible for data formatting, encryption, compression, and character encoding.

---

Layer 5 - Session

Creates, manages, and terminates communication sessions between devices.

---

Layer 4 - Transport

Provides end-to-end communication.

Protocols:

- TCP
- UDP

---

Layer 3 - Network

Responsible for logical addressing and routing.

Protocols:

- IPv4
- IPv6
- ICMP

Devices:

- Routers

---

Layer 2 - Data Link

Responsible for MAC addressing and Ethernet communication.

Protocols:

- Ethernet
- ARP

Devices:

- Switches

---

Layer 1 - Physical

Responsible for transmitting bits through cables, fiber optics, wireless signals, or virtual network interfaces.

---

OSI Model in This Lab

Layer 7 → SSH, Ping

Layer 4 → TCP, UDP

Layer 3 → IP Addressing

Layer 2 → Ethernet Frames, ARP

Layer 1 → VMware Virtual Switch, Virtual NICs

---

## OT Example

Industrial protocols such as Modbus TCP and EtherNet/IP operate on top of the lower OSI layers, using Ethernet and IP to communicate between Engineering Workstations, PLCs, HMIs, and SCADA systems.
