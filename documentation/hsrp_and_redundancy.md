# HSRP and Redundancy

This document details the High Availability and Redundancy design.

## HSRP

- HSRP (Hot Standby Router Protocol) will be configured on the core switches to provide default gateway redundancy for all VLANs.
- **Core-SW1:** Active HSRP router for odd-numbered VLANs.
- **Core-SW2:** Active HSRP router for even-numbered VLANs.

## Link Redundancy

- EtherChannel will be used to bundle multiple physical links between switches to provide link redundancy and increased bandwidth.
- Redundant links will be established to both ISPs.
