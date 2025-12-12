# Firewall Design

This document describes the firewall design and security zones.

## Security Zones

- **Inside (Trust):** Internal network (VLANs 10, 20, 30, 40, 50, 60, 70, 80, 100)
- **Outside (Untrust):** Internet
- **DMZ:** Demilitarized Zone (VLAN 90)

## Firewall Rules

- **Inside to Outside:** Allow outbound traffic from the internal network to the internet.
- **Outside to Inside:** Deny all inbound traffic from the internet to the internal network, except for established connections.
- **Outside to DMZ:** Allow specific inbound traffic (e.g., HTTP, HTTPS, DNS) to servers in the DMZ.
- **Inside to DMZ:** Allow internal users to access servers in the DMZ.
- **DMZ to Inside:** Deny all traffic from the DMZ to the internal network.
