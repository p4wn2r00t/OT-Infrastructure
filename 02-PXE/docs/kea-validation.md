# Kea DHCP Configuration Validation

## Objective

Before restarting the DHCP service, validate the configuration to ensure there are no syntax or configuration errors.

## Validation Command

```bash
sudo kea-dhcp4 -t /etc/kea/kea-dhcp4.conf
```

## Expected Result

The configuration should load successfully, and Kea should recognize the configured subnet.

Example:

- Subnet: 192.168.100.0/24

## Why Validate?

Validating the configuration before restarting the service helps prevent downtime caused by invalid configuration files.
