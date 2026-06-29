# Packet Flow in the OT Lab

## Introduction

Communication between devices does not occur instantly. Before a packet reaches its destination, Linux performs several networking operations.

Understanding packet flow is essential for troubleshooting, packet analysis, and OT Security monitoring.

---

# Packet Flow

When Ubuntu Server executes:

ping 192.168.100.20

Linux performs the following operations:

1. Checks the destination IP address.
2. Compares the destination network with its own subnet.
3. Determines that the destination is on the local network.
4. Checks the ARP Cache for the destination MAC address.
5. If unavailable, sends an ARP Request.
6. Receives an ARP Reply from the destination.
7. Creates an Ethernet Frame.
8. Sends the frame through the VMware Virtual Switch.
9. SCADA receives the ICMP Echo Request.
10. SCADA sends an ICMP Echo Reply.

---

Packet Path

Ubuntu Server

↓

Virtual Switch

↓

SCADA Server

↓

Virtual Switch

↓

Ubuntu Server

---

Why No Gateway?

Because both devices belong to the same subnet (192.168.100.0/24), Linux sends packets directly without using the default gateway.

---

## OT Example

The same communication process occurs when an Engineering Workstation exchanges data with a PLC or SCADA Server inside an industrial network.
