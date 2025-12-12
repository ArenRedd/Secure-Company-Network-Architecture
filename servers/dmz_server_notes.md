# DMZ Server Notes

This document contains notes about the servers in the DMZ.

## Web Server

- **Purpose:** Hosts the company's public website.
- **Hardening:**
    - Unnecessary services disabled.
    - Firewall enabled.
    - Regular security audits.

## DNS Server

- **Purpose:** Public DNS server for the company's domain.
- **Hardening:**
    - Running in a chroot jail.
    - DNSSEC enabled.
