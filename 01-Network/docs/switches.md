# Network Switches

## What is a Network Switch?

A network switch is a Layer 2 networking device that connects multiple devices within the same local network. Unlike a hub, a switch intelligently forwards data only to the intended destination by using MAC addresses.

## Why is a Switch Required?

Without a switch, every device would require a direct connection to every other device, making the network complex and difficult to manage.

A switch acts as a central communication point where all devices connect.

## How Does a Switch Work?

When a device sends data, the switch learns the source MAC address and stores it in its MAC Address Table.

When future packets are received, the switch checks its table and forwards the frame only to the correct destination port.

## MAC Address Table

The MAC Address Table stores:

- MAC Address
- Switch Port

This allows efficient forwarding and reduces unnecessary traffic.

## MAC Learning

Switches automatically learn MAC addresses by observing incoming Ethernet frames.

No manual configuration is required.

## Flooding

If the destination MAC address is unknown, the switch temporarily forwards the frame to all ports except the incoming port.

Once the destination device replies, the switch learns its MAC address and updates its MAC Address Table.

## MAC Aging

MAC entries are not stored permanently.

If a device becomes inactive for a period of time, the switch removes the entry automatically.

## Virtual Switch in VMware

VMware provides a software-based Virtual Switch that performs the same functions as a physical Ethernet switch.

In this project, the Virtual Switch connects:

- Ubuntu Server
- SCADA Server
- OT-SOC Server

through the VMnet2 Host-Only network.

## Industrial OT Example

Industrial Ethernet switches from vendors such as Siemens, Hirschmann, Cisco Industrial Ethernet, and Moxa use the same Layer 2 switching principles to connect PLCs, HMIs, SCADA Servers, and Engineering Workstations.
