# Domain Name System (DNS)

## What is DNS?

The Domain Name System (DNS) is responsible for translating human-readable domain names into IP addresses.

Example:

google.com → 142.250.x.x

Without DNS, users would need to remember numerical IP addresses instead of domain names.

How DNS Works

1. A user requests a domain name.
2. The operating system sends a DNS query to the configured DNS server.
3. The DNS server responds with the corresponding IP address.
4. The application communicates using the returned IP address.

Linux Commands

Display configured DNS servers:

cat /etc/resolv.conf

Test DNS resolution:

nslookup google.com

or

dig google.com

Troubleshooting

If "ping 8.8.8.8" succeeds but "ping google.com" fails, network connectivity is available but DNS resolution is not functioning correctly.

## OT Example

Engineering Workstations and OT-SOC servers use DNS for software updates, package downloads, and access to external services.

Industrial devices such as PLCs often communicate using static IP addresses within the OT network.
