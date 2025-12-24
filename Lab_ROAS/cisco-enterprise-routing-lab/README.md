# Cisco Enterprise Routing Lab – Multilayer & WAN

## 📌 Overview
This project simulates a real enterprise network using Cisco Packet Tracer.
It combines:
- Multilayer switching
- Inter-VLAN routing
- Router-on-a-Stick
- WAN routing with floating static routes
- ISP edge connectivity

## 🏗 Architecture
- Core: Cisco 3560 Multilayer Switch
- Edge Routers: Cisco 2811
- VLAN Segmentation
- DHCP Relay
- WAN redundancy

## 🧱 VLAN Design
| VLAN | Purpose |
|-----|--------|
| 101 | Users |
| 102 | HR |
| 103 | IT |
| 105 | Servers / DHCP |
| 150 | WiFi |
| 60/61/62 | Remote site |
| 100 | Management |

## 🌐 IP Addressing
- Core LAN: 192.168.110.0/24
- VLANs: /24 per VLAN
- WAN Links: /30
- ISP: 8.8.8.0/8 (simulated)

## 🔁 Routing
- Inter-VLAN routing on multilayer switch
- Static routing between routers
- Floating static routes for redundancy
- Default route toward ISP

## 🧪 Validation
- Inter-VLAN ping
- DHCP assignment per VLAN
- WAN failover
- Internet reachability (8.8.8.8)

## 🔜 Next Improvements
- ACL inter-VLAN
- NAT overload
- OSPF
- HSRP
- Port-security & BPDU Guard

## 🛠 Tools
- Cisco Packet Tracer
- Cisco IOS 12.x

## 👤 Author
Saidou DIA – Network Engineering Lab  
Learning by doing 🚀
