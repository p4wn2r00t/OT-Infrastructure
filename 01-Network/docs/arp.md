# Address Resolution Protocol (ARP)

## What is ARP?

Address Resolution Protocol (ARP) is a Layer 2 protocol used to discover the MAC address of a device when its IP address is already known.

Communication on an Ethernet network requires both an IP address and a MAC address.

## Why is ARP Required?

Before transmitting an Ethernet frame, the sender must know the destination MAC address.

If the MAC address is unknown, ARP is used to discover it.

## ARP Request

The source device sends a broadcast message asking:

"Who has this IP address?"

Every device on the local network receives the request.

## ARP Reply

Only the device that owns the requested IP address responds with its MAC address.

The reply is sent directly to the requesting device.

## ARP Cache

The sender stores the IP-to-MAC mapping in the ARP Cache.

Future communication can occur without sending another ARP Request until the cache entry expires.

## ARP Aging

ARP entries are temporary.

After a timeout period, old entries are removed and must be learned again.


## Example:

Ubuntu Server:

- IP Address: 192.168.100.10

SCADA Server:

- IP Address: 192.168.100.20

When Ubuntu pings SCADA for the first time:

1. Ubuntu sends an ARP Request.
2. SCADA replies with its MAC address.
3. Ubuntu stores the mapping in its ARP Cache.
4. Communication continues using Ethernet frames.

## OT Security Consideration

Attackers can exploit ARP using techniques such as ARP Spoofing or ARP Poisoning to redirect network traffic.

Monitoring ARP traffic is an important activity in OT Security monitoring and incident detection.
