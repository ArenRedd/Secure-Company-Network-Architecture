# **Secure Company Network Architecture – Cisco Packet Tracer (Enterprise-Level Project)**

*A fully designed & implemented secure enterprise network for a 3-floor corporate building, featuring firewalls, DMZ, WLC, VLANs, HSRP redundancy, VoIP, cloud connectivity, and ISP failover.*

---

## 📸 **Network Topology**

### **Full Network Diagram**

> <img width="2896" height="7996" alt="full_topology" src="https://github.com/user-attachments/assets/f31f3ff5-618e-44cb-8669-ce20f45d824b" />

> 

---

## 🏢 **Project Overview**

This project simulates a **real enterprise-class secure network infrastructure** for a cloud-technology company with **600+ employees**, multiple floors, department segmentation, redundancy, VoIP services, wireless infrastructure, server rooms, and DMZ hosting.

This project demonstrates:

- Enterprise LAN design
- Multi-layer switching
- Firewall zone segmentation
- Server deployment
- Wireless LAN controller infrastructure
- VoIP telephony setup
- ISP redundancy & cloud customer access
- Full security hardening
- Scalable and future-proof network build

---

## 🎯 **Project Goals**

✔ Provide secure connectivity for all departments

✔ Segment the network using VLANs & firewalls

✔ Support cloud-based client access

✔ Enable VoIP communication

✔ Provide high availability (HSRP + EtherChannel)

✔ Allow wireless mobility via WLC + LAPs

✔ Secure critical servers using DMZ + Internal Zones

---

## 🧱 **Network Components**

### **1. Service Provider / ISP Layer**

- **ISP1 – Seacom**
- **ISP2 – Safaricom**
- Each connects to the company through **Cisco 2911 routers**
- Provides **dual-homing Internet redundancy**

### **2. Edge Security Layer**

- Two **Cisco ASA 5506-X Firewalls**
- Configured with **three security zones**:
    - **Outside Zone** (ISP links)
    - **DMZ Zone** (public servers)
    - **Inside Zone** (internal LAN)

### **3. Core Switching**

- **Two Cisco 3650 Multilayer Switches**
- Running:
    - **HSRP** (Gateway redundancy)
    - **OSPF / Static Routing**
    - **Layer-3 SVI interfaces**
    - **EtherChannel (LACP)** between core switches

### **4. Access Layer**

- Cisco 2960 switches across **6 departments**:
    - Sales & Marketing
    - HR & Logistics
    - Finance & Accounts
    - Admin & Public Relations
    - ICT Department
    - Server Room

Each access switch includes:

- VLAN trunk uplinks
- Wireless AP uplinks
- PC, IP Phone, Printer connections

---

## 🌐 **VLAN Structure**

| VLAN | Name | Purpose |
| --- | --- | --- |
| 10 | MANAGEMENT | Switch, WLC, Firewall mgmt |
| 20 | LAN (Wired Users) | PCs & wired hosts |
| 50 | WLAN | Access points + wireless clients |
| 70 | VOICE | IP Phones + Voice Gateway |
| 90 | SERVER-INSIDE | AD, DHCP, DNS, RADIUS |
| 199 | BLACKHOLE | Disabled & unused ports |

---

## 📡 **Wireless Architecture**

- **Cisco 2504 Wireless LAN Controller**
- **Lightweight Access Points (LAPs)**
- Centrally managed Wi-Fi SSIDs for VLAN 50
- Mobility + Scalability for future expansion

---

## 🖥 **Server Infrastructure**
| Server | Function |
| --- | --- |
| Active Directory | User authentication & Group Policy |
| DHCP Server | IP distribution for VLAN 10 / 20 / 50 |
| DNS Server | Internal name resolution |
| RADIUS Server | 802.1X & device authentication |

| Server | Function |
| --- | --- |
| Web Server | Public website |
| Email Server | Corporate mail |
| FTP Server | Customer data uploads |
| App Server | Cloud application services |
| File Storage | Publicly accessible storage |

### **Internal Servers (INSIDE Zone – VLAN 90)**

### **DMZ Servers (DMZ Zone)**

---

## ☎️ **VoIP System**

- **Cisco 2811 Voice Gateway**
- IP Phones on all departments
- Voice VLAN 70
- Numbering format: `4XX` per department
- DHCP Option 150 for TFTP auto-config

---

## 🔥 **Security Mechanisms**

### **Firewall Zone Policies**

- Strict ACLs between:
    - Inside ↔ DMZ
    - Inside ↔ Outside
    - DMZ ↔ Outside
- Public services exposed only via DMZ
- Internal services **never accessible from outside**

### **Switch Security**

- BPDU Guard
- PortFast
- Blackhole VLAN for all unused ports
- SSH access restricted to **Management VLAN only**

### **Routing Security**

- HSRP failover
- OSPF internal segmentation
- Static routes for DMZ + ASA

---

## 🚀 **High Availability (Redundancy)**

### ✔ Dual ISP Redundancy

Automatic switching if ISP1 fails.

### ✔ HSRP on Core Switches

Core-1 = active for VLAN 10 & 20

Core-2 = active for VLAN 50 & 90

Each becomes standby for the other → load balanced gateway.

### ✔ EtherChannel

Three physical links bundled for:

- Faster throughput
- Stability
- Instant link failover

---

## 🌍 **Cloud Connectivity**

A simulated cloud router connects:

- External USA client
- External China client

These clients can securely access DMZ public services.

---

## 🛠 **Configuration Guide Summary**

The project includes the following configurations:

### **Switching**

- VLAN creation + SVI interfaces
- Trunking
- EtherChannel (LACP)
- BPDU Guard, PortFast
- DHCP relay using IP helper-address

### **Routing**

- Inter-VLAN routing
- HSRP VIPs
- Static routes
- OSPF for internal distribution

### **Firewall**

- Inside, Outside, DMZ interfaces
- NAT rules
- ACLs
- Static routes
- Security levels

### **DHCP**

- Pools for Management, LAN, WiFi, Voice
- Excluded addresses
- Option 150 for IP Phones

### **VoIP**

- Dial-peers
- Telephony service
- Phone registration
- Voice VLAN assignments

---

## 📝 **Conclusion**

This project demonstrates a **fully functional, enterprise-level secure network** with:

- Redundancy
- Security zones
- Wireless infrastructure
- VoIP telephony
- Cloud access
- Modern industry-standard architecture

It is suitable for:

- College final projects
- Portfolio showcase
- Job interview demonstration
- Enterprise network practice
