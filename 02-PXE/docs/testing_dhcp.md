# Testing the Kea DHCP Server

## Objective

Verify that the DHCP server successfully assigns IP addresses to PXE clients.

## Verification

The Kea service was confirmed to be running:

```bash
sudo systemctl status kea-dhcp4-server
```

## Monitoring DHCP Requests

The following command was used to monitor DHCP activity:

```bash
sudo journalctl -u kea-dhcp4-server -f
```

## Result

The DHCP server successfully offered IP addresses from the configured pool.

Example lease advertisements:

- 192.168.100.100
- 192.168.100.101
- 192.168.100.102
- 192.168.100.103

## Conclusion

The DHCP server is functioning correctly and is ready to provide PXE boot information to network clients.
