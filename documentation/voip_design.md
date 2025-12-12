# VoIP Design

This document describes the Voice over IP (VoIP) design.

## Components

- **Voice Gateway:** Connects the internal VoIP network to the PSTN.
- **IP Phones:** Cisco IP Phones will be used.
- **Voice VLAN:** VLAN 70 is dedicated to voice traffic.

## Quality of Service (QoS)

- QoS will be implemented to prioritize voice traffic over data traffic to ensure high call quality.
- Voice traffic will be marked with DSCP EF.
