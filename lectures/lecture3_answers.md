# Lecture 3 — Cloud Computing Networking
## Answer Key

| Q   | Answer | Topic |
|-----|--------|-------|
| 1   | **B** — A group of connected devices that communicate to share data and resources | Network Definition |
| 2   | **C** — Bandwidth (not a listed network property; the 4 properties are Devices, Group, Communicate, Share data/resources) | Network Properties |
| 3   | **B** — Networking basics, Networks inside Data Centers, Virtual Networks | Course Focus |
| 4   | **C** — ISO | OSI Model |
| 5   | **D** — 7 | OSI Layers |
| 6   | **B** — 4 | TCP/IP Layers |
| 7   | **B** — Simpler structure and protocol-driven (practical) | TCP/IP vs OSI |
| 8   | **C** — Application, Presentation, and Session | TCP/IP Mapping |
| 9   | **C** — Data Link and Physical | TCP/IP Mapping |
| 10  | **C** — Network Layer | TCP/IP Mapping |
| 11  | **C** — Application Layer (HTTP) | Communication Example |
| 12  | **C** — Ask DNS for target IP | HTTP Request Flow |
| 13  | **B** — SYN and SYN-ACK | TCP Handshake |
| 14  | **B** — Makes a System Call for NIC access to send data | System Calls |
| 15  | **C** — Send TCP message of the actual request with sequence IDs | HTTP Request Flow |
| 16  | **C** — Network Layer (IP packets carrying TCP ACK data) | TCP/IP Layers |
| 17  | **C** — Application Layer | Layer Protocols |
| 18  | **B** — UDP and TCP | Transport Protocols |
| 19  | **C** — Internet and Network Interface | ARP Position |
| 20  | **C** — RIP, OSPF, BGP, EGP | Routing Protocols |
| 21  | **C** — How to provide network services to end-user applications? | App Layer |
| 22  | **B** — APIs | App Layer |
| 23  | **C** — TCP (TCP is a Transport Layer protocol, not Application) | App Layer Protocols |
| 24  | **B** — NFS | App Layer Protocols |
| 25  | **C** — How to provide end-to-end communication? | Transport Layer |
| 26  | **B** — Which application is sending/receiving the data | Ports |
| 27  | **B** — Connection-oriented | TCP |
| 28  | **C** — Connectionless | UDP |
| 29  | **B** — Reliability | TCP vs UDP |
| 30  | **C** — Efficiency | TCP vs UDP |
| 31  | **C** — SYN → SYN-ACK → SYN (confirmation/ACK) | TCP Handshake |
| 32  | **C** — Send multiple responses without establishing a connection | UDP |
| 33  | **C** — Web browsing (Source port 50000) | Transport Layer Example |
| 34  | **B** — How data reaches the destination? | Network Layer |
| 35  | **B** — The DHCP Server (assigned dynamically) via the Router | Private IPs |
| 36  | **B** — The ISP | Public IPs |
| 37  | **B** — Dynamic Host Configuration Protocol | DHCP |
| 38  | **C** — The Router | Private IPs |
| 39  | **B** — Network Address Translator | NAT |
| 40  | **B** — Translating private IPs to public IPs and vice versa | NAT Function |
| 41  | **D** — Authoritative DNS Server | DNS Resolution |
| 42  | **B** — Ask Recursive → Ask Root → Ask TLD → Ask Authoritative → Return IP | DNS Flow |
| 43  | **D** — 217.64.213.12 | DNS Example |
| 44  | **B** — Each router has a routing table to pass the message to the next best node | Routing |
| 45  | **B** — Multiple routers, each forwarding to the next best node | Routing |
| 46  | **C** — How is data transferred? | Data Link Layer |
| 47  | **C** — IEEE 802.3 | Ethernet Standard |
| 48  | **B** — IEEE 802.11 | Wi-Fi Standard |
| 49  | **D** — IEEE 802.15.1 | Bluetooth Standard |
| 50  | **B** — IEEE 802.15.4 | Zigbee Standard |
| 51  | **B** — 3G | 3GPP Standards |
| 52  | **B** — 4G | 3GPP Standards |
| 53  | **C** — 4.5G | 3GPP Standards |
| 54  | **B** — Synchronization and notification for the receiver | Ethernet Frame |
| 55  | **A** — Start Frame Delimiter — "10101011" | Ethernet Frame |
| 56  | **C** — 6 bytes | MAC Address |
| 57  | **C** — 4 bytes — 32-bit hash code for error detection | Ethernet Frame CRC |
| 58  | **B** — The payload size | Ethernet Frame |
| 59  | **B** — 46 to 1500 bytes | Ethernet Payload |
| 60  | **B** — 64 to 1518 bytes | Ethernet Frame Size |
| 61  | **A** — Destination MAC + Source MAC + EtherType = 14 bytes | Ethernet MAC Header |
| 62  | **B** — Encoding/Decoding bits for transmission | Manchester Encoding |
| 63  | **C** — Multiple signal levels (more than two) | Ethernet Encoding |
| 64  | **B** — Data flows only in one direction | Simplex |
| 65  | **B** — Both parties can send and receive simultaneously | Full-Duplex |
| 66  | **B** — Both ends can communicate but only one at a time | Half-Duplex |
| 67  | **C** — How raw bits are transferred over physical media? | Physical Layer |
| 68  | **D** — Satellite Links (not mentioned; optical fibers, physical cables, radio frequency are listed) | Physical Media |
| 69  | **B** — NICs and modems | Physical Layer Devices |
| 70  | **C** — Physical Layer | NIC |
| 71  | **B** — Via the PCI Bus connecting Host DMA, Memory, and Net Send/Recv DMA | NIC Architecture |
| 72  | **C** — Converting digital data to analogue and vice versa | Modem |
| 73  | **B** — Modulator/Demodulator | Modem |
| 74  | **C** — Physical Layer | Repeater |
| 75  | **B** — Amplifies/Regenerates the signal strength within the same network | Repeater |
| 76  | **B** — A multi-port Repeater that broadcasts data to all attached devices | Hub |
| 77  | **C** — Physical Layer | Hub |
| 78  | **C** — Broadcast to ALL connected hosts (B, C, D, E) | Hub Behavior |
| 79  | **B** — Data Layer (Data Link) | Bridge |
| 80  | **B** — A two-port connector that passes messages to the target segment | Bridge |
| 81  | **B** — Any two sub-networks or host segments | Bridge |
| 82  | **B** — Data Layer (Data Link) | Switch |
| 83  | **B** — A Switch sends data only to the destination; a Hub broadcasts to all | Switch vs Hub |
| 84  | **B** — Only Host E receives the message | Switch Behavior |
| 85  | **C** — Network Layer | Router |
| 86  | **C** — A multi-network connector that moves data between networks and provides traffic control | Router |
| 87  | **C** — A Router connecting 192.168.1.X and 41.68.220.X | Router Example |
| 88  | **C** — Network Layer | NAT |
| 89  | **C** — 150.150.0.1 (the Router+NAT's public IP replaces the private source IP) | NAT Translation |
| 90  | **C** — 10.0.0.1 (NAT reverses the translation on inbound traffic) | NAT Translation |
| 91  | **C** — Network Layer | Access Point |
| 92  | **C** — DNS resolver for external domains (Access Point acts as switch, DHCP, router, firewall) | Access Point Roles |
| 93  | **D** — Application (App) Layer | Gateway |
| 94  | **B** — A multi-system connector for similar/dissimilar networks | Gateway |
| 95  | **D** — Application (App) Layer | Load Balancer |
| 96  | **C** — Distributing incoming traffic across a group of servers | Load Balancer |
| 97  | **D** — Application (App) Layer | Firewall |
| 98  | **D** — Controlling incoming/outgoing traffic based on security rules | Firewall |
| 99  | **B** — Switch → Data Layer; Router → Network Layer; Load Balancer → App Layer | Device-Layer Mapping |
| 100 | **D** — 7 (Point-to-point, Bus, Ring, Star, Tree, Mesh, Hybrid) | Network Topology |
| 101 | **C** — Ring | Ring Topology |
| 102 | **D** — Star | Star Topology |
| 103 | **C** — A single shared backbone cable | Bus Topology |
| 104 | **C** — Every device connected to every other device | Mesh Topology |
| 105 | **B** — Top-of-Rack | TOR |
| 106 | **B** — 1 to 10Gbps | TOR Speed |
| 107 | **C** — Connect servers within the same rack together | TOR Function |
| 108 | **C** — ~100Gbps | Core Switch Speed |
| 109 | **B** — Connect racks together (within a sector) | Core Switch Function |
| 110 | **C** — Connect sectors together and the internet | Layer 3 Switch Function |
| 111 | **C** — Between servers in the SAME rack | In-Rack Traffic |
| 112 | **B** — Between servers in the SAME sector (different racks) | East-West Traffic |
| 113 | **C** — Between sectors or to/from the internet | North-South Traffic |
| 114 | **B** — Servers → TOR → Core Switch → Layer 3 Switch | Cloud Network Hierarchy |
| 115 | **B** — PNIC via the Hypervisor Kernel and VM Network | Virtual Entities |
| 116 | **C** — Virtual networks are isolated and can share the same underlying physical resources | Virtual Network Properties |
| 117 | **B** — An abstraction layer that represents nodes/links and controls resources | Network Hypervisor |
| 118 | **D** — Assign public IP addresses from the ISP (not a hypervisor function) | Network Hypervisor Functions |
| 119 | **B** — How VMs on the SAME server communicate? | Internal Virtualization |
| 120 | **B** — Virtual NICs (VNICs) and virtual switches | Internal Virtualization |
| 121 | **B** — Traps the system call and emulates the operation using Virtual NICs | System Call Emulation |
| 122 | **B** — The VM's connectivity and bandwidth | Virtual NIC |
| 123 | **B** — Routes network messages to the target Virtual NIC | Virtual Switch |
| 124 | **C** — 172.19.0.0/16 | Docker Networking |
| 125 | **B** — A virtual bridge (mybridge) | Docker Networking |
| 126 | **B** — How VMs on DIFFERENT servers communicate? | External Virtualization |
| 127 | **B** — Virtual iptables with the physical servers hosting the target VMs | External Virtualization |
| 128 | **B** — Grouping devices into separate, isolated sub-groups | VLAN Definition |
| 129 | **C** — IEEE 802.1Q | VLAN Standard |
| 130 | **B** — Between Source Address and Length/Type fields | 802.1Q Frame Position |
| 131 | **C** — 12 bits | VLAN VID |
| 132 | **B** — Tag Protocol IDentifier | 802.1Q Fields |
| 133 | **C** — 4096 (2^12) | VLAN Limit |
| 134 | **C** — Form a group and communicate directly | VLAN Communication |
| 135 | **B** — Inter-VLAN routing | Inter-VLAN |
| 136 | **C** — Security through network traffic isolation | VLAN Pros |
| 137 | **B** — Interoperability issues with legacy/non-aware devices | VLAN Cons |
| 138 | **B** — VLAN IDs are 12 bits (only 4096 segments) — not enough for cloud | VXLAN Motivation |
| 139 | **B** — The virtualized VLAN connection between two Layer-2 switches | VXLAN Overlay |
| 140 | **C** — The physical network connection moving data from one switch to another | VXLAN Underlay |
| 141 | **C** — Layer-3 Switches/Routers | VXLAN Devices |
| 142 | **B** — A UDP message with a VXLAN header | VXLAN Encapsulation |
| 143 | **B** — Identify servers in the same VXLAN group (VNI) | VXLAN Header |
| 144 | **B** — VXLAN Network Identifier | VNI |
| 145 | **B** — The VTEP (VXLAN Tunnel Endpoint) on the source side | VXLAN Packet Flow |
| 146 | **B** — VXLAN Tunnel End Point | VTEP |
| 147 | **B** — Multiple Network Hypervisors emulating the operation of a switch across multiple host machines | DVS |
| 148 | **B** — Provides virtual switch ports that are configurable (e.g., control data rate) | DVS Pros |
| 149 | **B** — A VLAN | DVS-VLAN Relation |
| 150 | **B** — Virtual Private Cloud | VPC |
| 151 | **B** — Private virtual networks inside public cloud | VPC Definition |
| 152 | **B** — Internet Gateway, NAT Gateway, Route Tables, Subnets | VPC Components |
| 153 | **B** — 10.0.0.0/24 | AWS VPC Example |
| 154 | **B** — Internet Gateway and NAT Gateway | VPC Gateways |
| 155 | **C** — Route Tables (public/private subnets representing VLAN segmentation) | VPC VLAN Segmentation |
| 156 | **C** — Traffic Control, Security & Isolation, Flexible Network as a Service | VPC Pros |
| 157 | **C** — VPN Gateway + VPN Connection + Customer Gateway | VPC-Corporate Connectivity |
| 158 | **C** — Route Tables | VPC Virtual Routers |
| 159 | **C** — Router | Device Selection |
| 160 | **B** — VLAN | Technology Selection |
| 161 | **B** — VLAN IDs are limited to 4096 segments (12-bit VID) | VXLAN vs VLAN |
| 162 | **D** — Network Access Layer (hypervisor intercepts at the virtual NIC level) | System Call & Virtualization |
| 163 | **B** — DNS query → TCP handshake → Send HTTP request → Wait for response → Render HTML | HTTP Flow |
| 164 | **C** — PNIC → Physical Network Interface Card on the host server | Terminology |
| 165 | **C** — East-West | Traffic Types |
| 166 | **C** — PRI (Priority Code Point — 3 bits) | 802.1Q Fields |
| 167 | **B** — 7 bytes — Synchronization/Notification for Receiver | Ethernet Preamble |
| 168 | **B** — ARP (Address Resolution Protocol) | ARP |
| 169 | **B** — Maps MAC to IP | RARP |
| 170 | **C** — All host machines through coordinated hypervisors | DVS Architecture |

---

## Quick Reference — Layer Summary

| Layer | OSI Name | TCP/IP Name | Key Devices | Key Protocols |
|-------|----------|-------------|-------------|---------------|
| 5/6/7 | App/Presentation/Session | Application | Gateway, Load Balancer, Firewall | HTTP, SMTP, SSH, FTP, NFS, WebSocket |
| 4 | Transport | Transport | — | TCP, UDP |
| 3 | Network | Internet | Router, NAT, Access Point | IP, ICMP, ARP, RARP, OSPF, BGP |
| 2 | Data Link | Network Access | Switch, Bridge | IEEE 802.3 (Ethernet), IEEE 802.11, 802.1Q |
| 1 | Physical | Network Access | NIC, Modem, Repeater, Hub | Manchester encoding, Simplex/Duplex |

---

## Quick Reference — Network Devices

| Device | Layer | Key Characteristic |
|--------|-------|--------------------|
| NIC | Physical | Sends/receives data via PCI Bus |
| Modem | Physical | Digital ↔ Analogue conversion |
| Repeater | Physical | Amplifies/regenerates signal, same network |
| Hub | Physical | Multi-port repeater → broadcasts to ALL |
| Bridge | Data Link | Two-port, passes to target segment |
| Switch | Data Link | Multi-port, sends only to destination (MAC-aware) |
| Router | Network | Multi-network, routing table, traffic control |
| NAT | Network | Private IP ↔ Public IP translation |
| Access Point | Network | Switch + DHCP + Router + Firewall |
| Gateway | Application | Multi-system connector (dissimilar networks) |
| Load Balancer | Application | Distributes traffic across servers |
| Firewall | Application | Controls traffic by security rules |

---

## Quick Reference — Cloud Network Traffic Types

| Traffic Type | Description |
|--------------|-------------|
| In-Rack | Between servers in the SAME rack |
| East-West | Between servers in the SAME sector (different racks) |
| North-South | Between sectors OR to/from the internet |

---

## Quick Reference — Wireless/Mobile Standards

| Standard | Technology |
|----------|-----------|
| IEEE 802.3 | Ethernet |
| IEEE 802.11 | Wi-Fi |
| IEEE 802.15.1 | Bluetooth |
| IEEE 802.15.4 | Zigbee |
| 3GPP LTE R8 | 3G |
| 3GPP LTE R10 | 4G |
| 3GPP LTE R13 | 4.5G |

---

## Quick Reference — VLAN vs VXLAN vs DVS vs VPC

| Technology | Problem Solved | Key Mechanism | Limit/Scale |
|-----------|---------------|---------------|-------------|
| VLAN (802.1Q) | Traffic isolation on same physical switches | 802.1Q tag in Ethernet frame | 4096 segments (12-bit VID) |
| VXLAN | Cloud-scale multi-tenancy | UDP encapsulation with VXLAN header + VNI | 16 million segments (24-bit VNI) |
| DVS | Virtual switch spanning multiple physical hosts | Multiple hypervisors coordinate as one switch | As many hosts as needed |
| VPC | Private network inside public cloud | Virtual Routers + VLAN + Gateways | Cloud provider scale |
