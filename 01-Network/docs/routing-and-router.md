## Routing and Routers

## What is a Router?

A router is a Layer 3 networking device responsible for forwarding packets between different IP networks.

Unlike a switch, which connects devices within the same network, a router enables communication between separate networks.

Why is Routing Required?

When the destination device belongs to another network, the source system forwards the packet to its default gateway.

The router then determines the best path to reach the destination network.

Routing in This Lab

The OT Infrastructure Lab contains two separate networks:

- 172.16.67.0/24 (VMware NAT Network)
- 192.168.100.0/24 (Host-Only OT Network)

Communication within the OT network occurs directly through the VMware Virtual Switch.

Internet-bound traffic is forwarded through the VMware NAT gateway (172.16.67.2).

## Default Gateway

The default gateway is used whenever the destination IP address does not belong to the local subnet.

Linux determines this using its routing table, which can be viewed with:

ip route

Industrial OT Example

Engineering Workstations may require Internet access for software updates, while PLCs and SCADA systems remain isolated inside the OT network.

Routers and firewalls enforce this separation, reducing the attack surface and improving security.
