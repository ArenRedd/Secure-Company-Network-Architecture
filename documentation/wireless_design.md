# Wireless Design

This document details the wireless network design.

## SSIDs

- **Corporate-WiFi:** WPA2-Enterprise with 802.1X/RADIUS authentication for corporate users.
- **Guest-WiFi:** WPA2-PSK with a captive portal for guest users.

## Access Points

- Lightweight Access Points (LAPs) will be deployed throughout the building to provide seamless roaming.
- The LAPs will be managed by a Wireless LAN Controller (WLC).

## Security

- **Authentication:** WPA2-Enterprise for corporate users, WPA2-PSK for guests.
- **Encryption:** AES.
- **Guest Access:** Guest traffic will be isolated from the corporate network.
