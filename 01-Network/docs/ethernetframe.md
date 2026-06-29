# Ethernet Frames

## Introduction

Ethernet is the foundation of communication inside Local Area Networks (LANs).

Before data is transmitted, Linux encapsulates it inside an Ethernet Frame.

---

Ethernet Frame Components

An Ethernet Frame contains:

- Destination MAC Address
- Source MAC Address
- EtherType
- Payload (IP Packet)
- Frame Check Sequence (FCS)

---

## Why MAC Addresses?

IP addresses identify devices logically.

MAC addresses identify network interfaces physically within the local network.

Both are required for successful communication.

---

Encapsulation

Application Data

↓

ICMP

↓

IP Packet

↓

Ethernet Frame

↓

VMware Virtual Switch

↓

Destination Device

Each networking layer adds its own header before transmitting data.

This process is called Encapsulation.

---

VMware Example

When Ubuntu Server communicates with SCADA Server, VMware's Virtual Switch forwards Ethernet Frames based on destination MAC addresses.

---

## OT Example

Industrial protocols such as Modbus TCP, EtherNet/IP, and PROFINET also travel inside Ethernet Frames before reaching PLCs, HMIs, and SCADA Servers.
