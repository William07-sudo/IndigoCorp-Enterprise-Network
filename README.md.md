README

# IndigoCorp Enterprise Network Lab

> A Cisco Packet Tracer simulation of a secure enterprise network featuring inter(routing, switching), wireless networking, network services, IPv4/IPv6 connectivity, and simulated Internet access.

---

## Project Overview

This project demonstrates the design, implementation and configuration of a medium-sized enterprise network using Cisco Packet Tracer.

The network consists of an Essex branch office connected to a Regional Headquarters through routed WAN links and an ISP router that simulates Internet connectivity. The enterprise infrastructure includes multiple VLANs, Layer 3 switching, dynamic routing, enterprise wireless, DHCP, DNS, TFTP and dual-stack IPv4/IPv6 networking.

---

## Network Architecture

### Essex Branch

- Layer 3 Core Switch
- Four Access Switches
- Email Server
- Four Department VLANs (containing 2 PC's in each VLAN)
- Inter-VLAN Routing
- EtherChannel (LACP)
- Trunk Links

### Regional Headquarters

- Two Internal Routers
- DNS Server
- DHCP Server
- TFTP Server
- A PC
- IP Phone (Voice VLAN)
- Network Printer

### Wireless Infrastructure

- Cisco Wireless LAN Controller (WLC)
- Lightweight Access Point (LAP)
- Wireless Clients (Smartphone and Wireless End Device)
- Wireless VLAN

### WAN

- Essex Core Router
- Regional HQ Router
- ISP Router (represents simulated internet)

---

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS
- IPv4/IPV6
- OSPF (Dynamic Routing)
- Static Routing
- Port Address Translation (PAT)
- VLANs
- Inter-VLAN Routing
- EtherChannel
- SSH
- Port Security
- DHCP
- DNS
- TFTP
- Wireless LAN Controller
- Lightweight Access Point

---

## VLAN Design

| VLAN | Department 
|------|------------
|100   |Customer Service
|200   |Sales
|300   |Information Technology
|400   |Marketing
|10    |Voice
|80    |Wireless
|99    |Management

---

## IP Addressing

| Network | Purpose |
|---------|---------|
|192.168.30.0/24|Department VLANs|
|192.168.40.0/30|Regional HQ <-> R1|
|192.168.50.0/30|Regional HQ <-> R2|
|192.168.60.0/29|Server Network|
|192.168.70.0/26|Head Office LAN|

|203.0.113.0/30|Essex Core <-> Layer 3 Switch|
|203.0.114.0/30|Essex Core <-> Regional HQ|
|203.0.115.0/30|Regional HQ <-> ISP|

IPv6 is implemented throughout the routed infrastructure using the 2001:DB8::/64 documentation prefix (Within the HQ).

---

## Network Services

- DHCP

- DNS

- TFTP

- SSH Remote Management

- OSPF Dynamic Routing

- Inter-VLAN Routing

- IPv6 Routing

- Wireless LAN

- NAT/PAT

- Port Security

---

## Security Features

- SSH Version 2 enabled on all managed switches
- RSA key generation
- Password encryption
- Port Security (Sticky MAC)
- Management VLAN
- Disabled unused switch ports
- VLAN segmentation

---

## Routing

### Dynamic Routing

- OSPF Area 0
- Loopback Router IDs
- Internal route advertisement

### Static Routing

- Default routes toward HQ (and from HQ to ISP router)
- ISP default routing

### NAT

- PAT (Overload)
- Internal private addressing is translated to a public address
- Internet simulation through an ISP Router

---

## Wireless Network

The wireless network consists of:

- Cisco Wireless LAN Controller (WLAN)
- Lightweight Access Point
- Wireless Smartphone Client
- Wireless End Device

Wireless clients receive network configuration through DHCP and communicate with internal resources.

---

## Repository Structure

```
IndigoCorp-Enterprise-Network/
│
├── README.md
├── IndigoCorp.pkt
│
├── configs/
│   ├── ESSEX-CORE-ROUTER.txt
│   ├── ESSEX-SW1.txt
│   ├── ESSEX-SW2.txt
│   ├── ESSEX-SW3.txt
│   ├── ESSEX-SW4.txt
│   ├── HQ-ROUTER-1.txt
│   ├── HQ-ROUTER-2.txt
│   ├── HQ-SWITCH-1.txt
│   ├── HQ-SWITCH-2.txt
│   ├── ISP-ROUTER.txt
│   ├── MULTILAYER-SWITCH.txt
│   └── REGIONAL-HQ-ROUTER.txt
│
├── screenshots/
│   ├── DHCP-Config.png
│   ├── DNS-Entries.png
│   ├── REG-HQ-ROUTER-OSPF-PEER.png
│   ├── REG-HQ-ROUTER-ROUTING-TABLE.png
│   ├── Topology-Cont.png
│   ├── Topology.png
│   ├── VLAN-HQ-SWITCH2.png
│   ├── VLAN-L3-SWITCH.png
│   └── WLAN-Controller.png
│
└── documentation/
    ├── Network-Design.pdf
    └── IP-Addressing-Plan.pdf
```

---

## Skills Demonstrated

- Enterprise Network Design
- Inter-routing
- Segmentation
- Cisco IOS Configuration (Basic switch and router configuration)
- Dynamic Routing
- Static Routing
- IPv4 & IPv6 Networking
- Wireless Networking
- Network Security and best security practices
- Layer 2 & Layer 3 Troubleshooting
- Network Documentation

---

## How to Use

1. Clone or download this repository.
2. Open `IndigoCorp PT.pkt` using Cisco Packet Tracer (version 8.x or later recommended).
3. Explore the topology in Realtime mode.
4. Review the device configurations in the `configs/` folder.
5. Use the screenshots and documentation to understand the network design and verify connectivity.

## Author

**William Debrah**