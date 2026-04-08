# Lecture 3 — Cloud Computing Networking
## MCQ Bank (130 Questions)

---

### Section 1: Network Basics

**Q1.** A network is best defined as:
- A) A single device connected to the internet
- B) A group of connected devices that communicate with each other to share data and resources
- C) A software application used to transfer files
- D) A protocol for encoding binary data

---

**Q2.** Which of the following is NOT listed as a network property?
- A) Devices
- B) Group
- C) Bandwidth
- D) Share data/resources

---

**Q3.** In the context of this course, which THREE areas are the focus of the networking lecture?
- A) Software Engineering, Networks, Web
- B) Networking basics, Networks inside Data Centers, Virtual Networks
- C) TCP/IP, OSI, Ethernet
- D) VMs, Containers, Physical Networks

---

### Section 2: Communication Models (OSI & TCP/IP)

**Q4.** The OSI model was developed by which organization?
- A) IEEE
- B) IETF
- C) ISO
- D) 3GPP

---

**Q5.** How many layers does the OSI model have?
- A) 4
- B) 5
- C) 6
- D) 7

---

**Q6.** How many layers does the TCP/IP model have?
- A) 3
- B) 4
- C) 5
- D) 7

---

**Q7.** Which of the following best describes the TCP/IP model compared to OSI?
- A) More complex and theoretical
- B) Simpler structure and protocol-driven (practical)
- C) Standardized by ISO
- D) Has more layers than OSI

---

**Q8.** In the TCP/IP model, which OSI layers are merged into the "Application Layer"?
- A) Physical and Data Link
- B) Network and Transport
- C) Application, Presentation, and Session
- D) Transport and Network

---

**Q9.** In the TCP/IP model, which OSI layers are merged into the "Network Access (Link Layer)"?
- A) Application, Presentation, Session
- B) Transport and Network
- C) Data Link and Physical
- D) Session and Transport

---

**Q10.** What is the correct mapping of the "Internet Layer" in TCP/IP to the OSI model?
- A) Transport Layer
- B) Data Link Layer
- C) Network Layer
- D) Application Layer

---

**Q11.** When loading "www.google.com", the sequence starts at which layer on the HOST side?
- A) Physical Layer
- B) Network Layer
- C) Application Layer (HTTP)
- D) Transport Layer

---

**Q12.** When a browser sends an HTTP request to load www.google.com, what is the FIRST step at the network level?
- A) Open TCP connection (Handshake)
- B) Send TCP message of the request
- C) Ask DNS for target IP
- D) Send IP packet to destination

---

**Q13.** In the TCP connection process (Handshake), which two messages are exchanged?
- A) GET and POST
- B) SYN and SYN-ACK
- C) PUSH and ACK
- D) FIN and FIN-ACK

---

**Q14.** At the Network Layer, what does the system do when sending a SYN packet?
- A) Calls DNS for IP resolution
- B) Makes a System Call for NIC access to send data
- C) Waits for an HTTP response
- D) Opens a socket on port 443

---

**Q15.** After the TCP handshake, what does the client do next?
- A) Render the HTML page
- B) Ask DNS again
- C) Send TCP message of the actual request with sequence IDs
- D) Close the connection

---

**Q16.** TCP acknowledgment packets (ACKs) travel at which layer?
- A) Application Layer (HTTP)
- B) Data Link Layer
- C) Network Layer (IP packets carrying TCP data)
- D) Physical Layer only

---

**Q17.** In the full communication model diagram (slide 11), NFS is an example of a protocol at which layer?
- A) Transport Layer
- B) Network Layer
- C) Application Layer
- D) Data Link Layer

---

**Q18.** Which transport-layer protocols are shown in the TCP/IP model?
- A) HTTP and FTP
- B) UDP and TCP
- C) IP and ICMP
- D) ARP and RARP

---

**Q19.** ARP (Address Resolution Protocol) sits between which two layers in the TCP/IP model?
- A) Application and Transport
- B) Transport and Internet
- C) Internet and Network Interface
- D) Physical and Data Link

---

**Q20.** Which routing protocols are shown in the Internet Layer?
- A) HTTP, FTP, SMTP
- B) UDP, TCP
- C) RIP, OSPF, BGP, EGP
- D) Ethernet, Wi-Fi

---

### Section 3: Application Layer (Layer 5 in TCP/IP)

**Q21.** The Application Layer answers which fundamental question?
- A) How raw bits are transferred?
- B) How data reaches the destination?
- C) How to provide network services to end-user applications?
- D) How to provide end-to-end communication?

---

**Q22.** Application Layer protocols are used by:
- A) NICs and modems
- B) APIs
- C) IP routing tables
- D) Physical switches

---

**Q23.** Which of the following is NOT listed as an Application Layer protocol in the lecture?
- A) HTTP
- B) WebSocket
- C) TCP
- D) SSH

---

**Q24.** Which protocol is used for file sharing according to the lecture's Application Layer?
- A) HTTP
- B) NFS
- C) SMTP
- D) WebSocket

---

### Section 4: Transport Layer (Layer 4)

**Q25.** The Transport Layer answers which fundamental question?
- A) How raw bits are transferred?
- B) How data reaches the destination?
- C) How to provide end-to-end communication?
- D) How to provide network services to applications?

---

**Q26.** In the Transport Layer, TCP/UDP ports identify:
- A) The physical location of a server
- B) Which application is sending/receiving the data
- C) The MAC address of the destination
- D) The routing path through the internet

---

**Q27.** TCP is characterized as:
- A) Connectionless
- B) Connection-oriented
- C) Broadcast-based
- D) Stateless

---

**Q28.** UDP is characterized as:
- A) Connection-oriented
- B) Reliable with ACKs
- C) Connectionless
- D) Requires handshake

---

**Q29.** What does TCP prioritize over UDP?
- A) Speed and efficiency
- B) Reliability
- C) Lower overhead
- D) Broadcast capability

---

**Q30.** What does UDP prioritize over TCP?
- A) Reliability
- B) Ordered delivery
- C) Efficiency
- D) Error correction

---

**Q31.** In the TCP handshake, which of the following is the correct sequence?
- A) SYN → ACK → SYN-ACK
- B) SYN-ACK → SYN → ACK
- C) SYN → SYN-ACK → SYN (confirmation)
- D) ACK → SYN → SYN-ACK

---

**Q32.** In a UDP exchange, the server can:
- A) Only send one response
- B) Wait for a SYN before responding
- C) Send multiple responses without establishing a connection
- D) Only receive but never send

---

**Q33.** Source port 50000 in the slide example is associated with:
- A) Email communicating
- B) FTP Uploading
- C) Web browsing
- D) SSH tunneling

---

### Section 5: Network Layer (Layer 3)

**Q34.** The Network Layer answers which fundamental question?
- A) How to provide end-to-end communication?
- B) How data reaches the destination?
- C) How raw bits are transferred?
- D) How to provide network services?

---

**Q35.** Private IP addresses in a home/office network are generated by:
- A) The ISP
- B) The DHCP Server (assigned dynamically) via the Router
- C) The modem directly from the internet
- D) Each device independently

---

**Q36.** Public IP addresses are generated by:
- A) The DHCP server on the router
- B) The ISP
- C) The DNS server
- D) The local switch

---

**Q37.** What does DHCP stand for?
- A) Dynamic Host Connection Protocol
- B) Dynamic Host Configuration Protocol
- C) Distributed Host Communication Protocol
- D) Direct Hardware Configuration Protocol

---

**Q38.** In the slide example, the private IPs shown (192.168.1.1 to 192.168.1.4) are generated by:
- A) The ISP
- B) The DNS server
- C) The Router
- D) Each device itself

---

**Q39.** What does NAT stand for?
- A) Network Access Technology
- B) Network Address Translator
- C) Node Allocation Table
- D) Network Aggregation Tool

---

**Q40.** NAT's primary function is:
- A) Routing messages between application-layer services
- B) Translating private IPs to public IPs and vice versa
- C) Encrypting all network traffic
- D) Assigning MAC addresses to devices

---

**Q41.** In the DNS resolution process for "www.example.com", which server provides the final authoritative IP address?
- A) Root DNS Server
- B) ISP's Recursive Server
- C) Top Level Domain (TLD) DNS Server
- D) Authoritative DNS Server

---

**Q42.** What is the correct sequence of DNS resolution steps?
- A) Ask Root → Ask TLD → Ask Authoritative → Get IP from Recursive Server
- B) Ask Recursive → Ask Root → Ask TLD → Ask Authoritative → Return IP to client
- C) Ask Authoritative directly
- D) Ask TLD → Ask Root → Get IP

---

**Q43.** In the lecture example, the DNS resolution query returns IP:
- A) 192.168.1.1
- B) 82.129.80.111
- C) 142.251.142.206
- D) 217.64.213.12

---

**Q44.** How do routers determine the path for an IP packet?
- A) They broadcast to all connected devices
- B) Each router has a routing table to pass the message to the next best node
- C) They always use the shortest physical path
- D) The DNS server provides routing instructions

---

**Q45.** IP routing at the network layer involves packets traveling through:
- A) A single dedicated path predetermined at connection start
- B) Multiple routers, each forwarding to the next best node
- C) Only the ISP's infrastructure
- D) A direct physical cable from source to destination

---

### Section 6: Data Link Layer (Layer 2)

**Q46.** The Data Link Layer answers which fundamental question?
- A) How to provide end-to-end communication?
- B) How data reaches the destination?
- C) How is data transferred?
- D) How to provide network services?

---

**Q47.** Which IEEE standard corresponds to Ethernet?
- A) IEEE 802.11
- B) IEEE 802.15.1
- C) IEEE 802.3
- D) IEEE 802.15.4

---

**Q48.** Which IEEE standard corresponds to Wi-Fi?
- A) IEEE 802.3
- B) IEEE 802.11
- C) IEEE 802.15.1
- D) IEEE 802.15.4

---

**Q49.** Which standard corresponds to Bluetooth?
- A) IEEE 802.3
- B) IEEE 802.11
- C) IEEE 802.15.4
- D) IEEE 802.15.1

---

**Q50.** Which standard corresponds to Zigbee?
- A) IEEE 802.15.1
- B) IEEE 802.15.4
- C) IEEE 802.11
- D) 3GPP LTE R8

---

**Q51.** 3GPP LTE R8 corresponds to which mobile generation?
- A) 2G
- B) 3G
- C) 4G
- D) 4.5G

---

**Q52.** 3GPP LTE R10 corresponds to which mobile generation?
- A) 3G
- B) 4G
- C) 4.5G
- D) 5G

---

**Q53.** 3GPP LTE R13 corresponds to which mobile generation?
- A) 4G
- B) 5G
- C) 4.5G
- D) 3G

---

**Q54.** In an Ethernet frame, what is the purpose of the Preamble field?
- A) Error detection using a hash code
- B) Synchronization and notification for the receiver
- C) Identifying the destination MAC address
- D) Specifying payload size

---

**Q55.** What does SFD stand for in an Ethernet frame, and what is its value?
- A) Start Frame Delimiter — "10101011"
- B) Source Frame Data — "11001100"
- C) Signal Frame Detection — "11111111"
- D) Start Frame Data — "10101010"

---

**Q56.** How many bytes is a MAC address in an Ethernet frame?
- A) 4 bytes
- B) 2 bytes
- C) 6 bytes
- D) 8 bytes

---

**Q57.** In an Ethernet frame, the CRC field is:
- A) 7 bytes — synchronization
- B) 2 bytes — payload size
- C) 4 bytes — 32-bit hash code for error detection
- D) 6 bytes — MAC address

---

**Q58.** The Length field in an Ethernet frame indicates:
- A) The duration of the transmission
- B) The payload size
- C) The source IP address
- D) The number of hops

---

**Q59.** The data payload in an Ethernet Type II frame is:
- A) Fixed at 512 bytes
- B) 46 to 1500 bytes
- C) 7 bytes
- D) Always exactly 1500 bytes

---

**Q60.** In an Ethernet Type II frame, the total frame size is:
- A) 14 to 512 bytes
- B) 64 to 1518 bytes
- C) 128 to 2048 bytes
- D) 46 to 1500 bytes

---

**Q61.** The MAC Header in an Ethernet Type II frame consists of:
- A) Destination MAC + Source MAC + EtherType = 14 bytes
- B) Preamble + SFD = 8 bytes
- C) Source MAC + CRC = 10 bytes
- D) Destination IP + Source IP = 8 bytes

---

**Q62.** Manchester encoding in the Data Link layer is used for:
- A) Routing packets between networks
- B) Encoding/Decoding bits for transmission
- C) Compressing payload data
- D) Assigning IP addresses dynamically

---

**Q63.** Newer Ethernet protocols have:
- A) Fewer signal levels
- B) Only binary encoding
- C) Multiple signal levels (more than two)
- D) No encoding at all

---

**Q64.** In simplex transmission mode:
- A) Data can flow in both directions simultaneously
- B) Data flows only in one direction
- C) Data alternates directions on a shared medium
- D) Data is broadcast to all nodes

---

**Q65.** Full-duplex transmission means:
- A) Data flows in one direction only
- B) Both parties can send and receive simultaneously
- C) Only one party can transmit at a time
- D) Data is sent in half-speed alternating bursts

---

**Q66.** Half-duplex transmission means:
- A) Data flows only one direction permanently
- B) Both ends can communicate but only one at a time, sharing the medium
- C) Full simultaneous bidirectional communication
- D) Data sent in broadcast mode

---

### Section 7: Physical Layer (Layer 1)

**Q67.** The Physical Layer answers which fundamental question?
- A) How to provide end-to-end communication?
- B) How data reaches the destination?
- C) How raw bits are transferred over physical media?
- D) How to provide network services?

---

**Q68.** Which of the following is NOT listed as a physical media example in the lecture?
- A) Optical Fibers
- B) Physical Cables
- C) Radio Frequency
- D) Satellite Links

---

**Q69.** Which hardware components handle data conversion and raw transmission at the Physical Layer?
- A) Routers and switches
- B) NICs and modems
- C) Firewalls and load balancers
- D) DNS servers and gateways

---

### Section 8: Network Devices

**Q70.** A Network Interface Card (NIC) operates at which layer?
- A) Network Layer
- B) Data Layer
- C) Physical Layer
- D) Application Layer

---

**Q71.** How does a computer send/receive data through a NIC?
- A) Through HTTP requests only
- B) Via the PCI Bus connecting Host DMA, Memory, and Net Send/Recv DMA to the network
- C) By directly accessing the router's routing table
- D) Using DNS system calls

---

**Q72.** A Modem's primary function is:
- A) Routing packets between networks
- B) Broadcasting data to all devices
- C) Converting digital data (Computer) to analogue (Fiber/Coaxial) and vice versa
- D) Assigning dynamic IP addresses

---

**Q73.** "Modem" is short for:
- A) Modern Networking Device
- B) Modulator/Demodulator
- C) Module/Demodule
- D) Motor/Demotivator

---

**Q74.** A Repeater operates at which layer?
- A) Network Layer
- B) Data Link Layer
- C) Physical Layer
- D) Application Layer

---

**Q75.** What does a Repeater do?
- A) Routes packets between different networks
- B) Amplifies/Regenerates the signal strength within the same network
- C) Translates private IPs to public IPs
- D) Directs traffic only to the intended destination

---

**Q76.** A Hub is best described as:
- A) A multi-port connector that sends data only to the destination device
- B) A multi-port Repeater that broadcasts data to all attached devices
- C) A device that routes messages between networks
- D) A device that converts analogue to digital signals

---

**Q77.** A Hub operates at which layer?
- A) Data Layer
- B) Network Layer
- C) Physical Layer
- D) Application Layer

---

**Q78.** When Host A wants to send a message to Host E through a Hub (5 hosts connected), the Hub will:
- A) Send only to Host E
- B) Send to Host A and Host E only
- C) Broadcast to ALL connected hosts (B, C, D, E)
- D) Look up a routing table and forward selectively

---

**Q79.** A Bridge operates at which layer?
- A) Physical Layer
- B) Data Layer (Data Link)
- C) Network Layer
- D) Application Layer

---

**Q80.** A Bridge is characterized as:
- A) A multi-port repeater
- B) A two-port connector that passes messages to the target segment
- C) A device that routes between different IP networks
- D) A multi-network connector

---

**Q81.** What does a Bridge join?
- A) Different IP networks
- B) Any two sub-networks or host segments
- C) Application layer services
- D) Physical cables to wireless networks

---

**Q82.** A Switch operates at which layer?
- A) Physical Layer
- B) Data Layer (Data Link)
- C) Network Layer
- D) Application Layer

---

**Q83.** The key difference between a Switch and a Hub is:
- A) A Switch operates at the Physical layer; a Hub does not
- B) A Switch sends data only to the destination device; a Hub broadcasts to all
- C) A Switch cannot handle multiple ports
- D) A Hub uses MAC addresses; a Switch does not

---

**Q84.** When Host A sends a message to Host E through a Switch:
- A) All connected hosts receive the message
- B) Only Host E receives the message
- C) The message is dropped if Host E is offline
- D) The message is broadcast then filtered by each host

---

**Q85.** A Router operates at which layer?
- A) Physical Layer
- B) Data Layer
- C) Network Layer
- D) Application Layer

---

**Q86.** A Router is best described as:
- A) A two-port connector between sub-networks
- B) A multi-port repeater
- C) A multi-network connector that moves data between networks and provides traffic control
- D) A device that converts analogue to digital

---

**Q87.** In the Router diagram, what separates the two sub-networks?
- A) A Bridge
- B) A Switch
- C) A Router connecting 192.168.1.X and 41.68.220.X
- D) A Hub

---

**Q88.** A NAT device operates at which layer?
- A) Physical Layer
- B) Data Layer
- C) Network Layer
- D) Application Layer

---

**Q89.** In the NAT example, a host with source IP 10.0.0.1 sends a packet to 200.100.10.1. After passing through the NAT (Router+NAT at 150.150.0.1), the source IP in the packet reaching the server becomes:
- A) 10.0.0.1
- B) 200.100.10.1
- C) 150.150.0.1
- D) 192.168.1.1

---

**Q90.** When the server at 200.100.10.1 responds back through NAT, the destination IP in the packet arriving at the host is:
- A) 150.150.0.1
- B) 200.100.10.1
- C) 10.0.0.1
- D) 192.168.0.1

---

**Q91.** An Access Point operates at which layer?
- A) Physical Layer
- B) Data Layer
- C) Network Layer
- D) Application Layer

---

**Q92.** Which of the following roles does an Access Point NOT perform?
- A) Switch
- B) DHCP server
- C) DNS resolver for external domains
- D) Firewall

---

**Q93.** A Gateway operates at which layer?
- A) Physical Layer
- B) Data Layer
- C) Network Layer
- D) Application (App) Layer

---

**Q94.** A Gateway is best described as:
- A) A two-port connector for sub-networks
- B) A multi-system connector for similar/dissimilar networks
- C) A device that amplifies signals
- D) A multi-port repeater

---

**Q95.** A Load Balancer operates at which layer?
- A) Transport Layer
- B) Network Layer
- C) Data Layer
- D) Application (App) Layer

---

**Q96.** The primary function of a Load Balancer is:
- A) Translating private IPs to public IPs
- B) Routing packets between networks
- C) Distributing incoming traffic across a group of servers
- D) Amplifying signal strength

---

**Q97.** A Firewall operates at which layer?
- A) Physical Layer
- B) Data Layer
- C) Network Layer
- D) Application (App) Layer

---

**Q98.** A Firewall's primary function is:
- A) Converting analogue to digital signals
- B) Distributing traffic across servers
- C) Routing between subnets
- D) Controlling incoming/outgoing traffic based on security rules

---

**Q99.** Which of the following correctly matches devices to their layers?
- A) Hub → Network Layer; Router → Data Layer
- B) Switch → Data Layer; Router → Network Layer; Load Balancer → App Layer
- C) Bridge → Physical Layer; Switch → Network Layer
- D) NIC → Data Layer; Modem → Application Layer

---

### Section 9: Network Topology

**Q100.** How many standard network topologies are shown in the lecture?
- A) 4
- B) 5
- C) 6
- D) 7

---

**Q101.** In which topology does data travel in a circular path through all devices?
- A) Bus
- B) Star
- C) Ring
- D) Mesh

---

**Q102.** In which topology are all devices connected to a central device (hub/switch)?
- A) Bus
- B) Ring
- C) Tree
- D) Star

---

**Q103.** In a Bus topology, all devices connect to:
- A) A central hub
- B) Each other directly
- C) A single shared backbone cable
- D) A ring of routers

---

**Q104.** A Mesh topology is characterized by:
- A) One central device
- B) A linear backbone
- C) Every device connected to every other device
- D) A hierarchical tree structure

---

### Section 10: Cloud Network Structure

**Q105.** In a cloud data center, TOR stands for:
- A) Transfer Of Route
- B) Top-of-Rack
- C) Traffic Overhead Router
- D) Trunked Output Router

---

**Q106.** TOR switches operate at what speed range?
- A) 100Mbps to 1Gbps
- B) 1 to 10Gbps
- C) 40 to 100Gbps
- D) 1Tbps

---

**Q107.** The primary function of TOR switches is to:
- A) Connect sectors together and the internet
- B) Connect racks to the internet directly
- C) Connect servers within the same rack together
- D) Route traffic between VMs globally

---

**Q108.** Core Switches in a cloud data center operate at approximately:
- A) 1Gbps
- B) 10Gbps
- C) 100Gbps
- D) 1Tbps

---

**Q109.** Core Switches are used to:
- A) Connect servers within the same rack
- B) Connect racks together (within a sector)
- C) Connect sectors together and the internet
- D) Translate private IPs to public IPs

---

**Q110.** Layer 3 Switches/Routers in a cloud data center are used to:
- A) Connect servers within racks
- B) Connect racks within a sector
- C) Connect sectors together and the internet
- D) Manage VLAN assignments

---

**Q111.** In-Rack traffic refers to communication:
- A) Between sectors
- B) Between servers in different racks within the same sector
- C) Between servers in the SAME rack
- D) Between the data center and the internet

---

**Q112.** East-West traffic in a cloud data center refers to:
- A) Traffic between sectors or the internet
- B) Traffic between servers in the SAME sector (different racks)
- C) Traffic between servers in the same rack
- D) Traffic from end-users to the data center

---

**Q113.** North-South traffic refers to:
- A) Traffic between servers in the same rack
- B) Traffic between servers in the same sector
- C) Traffic between sectors or to/from the internet
- D) Internal VM-to-VM communication

---

**Q114.** The correct hierarchy of cloud network structure from bottom to top is:
- A) Layer 3 Switch → Core Switch → TOR → Servers
- B) Servers → TOR → Core Switch → Layer 3 Switch
- C) Servers → Core Switch → TOR → Layer 3 Switch
- D) TOR → Servers → Core Switch → Layer 3 Switch

---

### Section 11: Network Virtualization Concepts

**Q115.** In cloud data centers, virtual entities (VMs/Containers) communicate through:
- A) Direct physical NIC connections only
- B) PNIC (Physical NIC) via the Hypervisor Kernel and VM Network
- C) External routers only
- D) The internet backbone directly

---

**Q116.** Which of the following is TRUE about virtual networks in cloud data centers?
- A) Virtual networks must use dedicated physical resources
- B) Virtual networks are always public
- C) Virtual networks are isolated and can share the same underlying physical resources
- D) Each virtual network requires a separate physical switch

---

**Q117.** A Network Hypervisor is best described as:
- A) A physical router with special firmware
- B) An abstraction layer that represents nodes/links in a virtual network and controls resources
- C) A software firewall
- D) A load balancer for VMs

---

**Q118.** Which of the following is NOT a function of the Network Hypervisor?
- A) Control bandwidth
- B) Control virtual network capacity
- C) Isolate and secure virtual networks
- D) Assign public IP addresses from the ISP

---

**Q119.** Internal Virtualization addresses which question?
- A) How VMs on different servers communicate?
- B) How VMs on the SAME server communicate?
- C) How physical switches route VLAN traffic?
- D) How NAT translates between private and public IPs?

---

**Q120.** In Internal Virtualization, the VMM Hypervisor creates:
- A) Physical NICs and physical switches
- B) Virtual NICs (VNICs) and virtual switches
- C) TOR switches and Core switches
- D) VXLAN tunnels

---

**Q121.** In Internal Virtualization, when a VM triggers a network system call (e.g., sendmsg()), the hypervisor:
- A) Ignores the call and passes it to the physical NIC directly
- B) Traps the system call and emulates the operation using Virtual NICs
- C) Broadcasts the call to all VMs on the server
- D) Escalates the call to the ISP router

---

**Q122.** A Virtual NIC defines:
- A) The routing table for the physical server
- B) The VM's connectivity and bandwidth
- C) The DNS configuration for the host
- D) The MAC addresses for physical switches

---

**Q123.** In Internal Virtualization (Emulate Network Function), network requests are forwarded to the Hypervisor's virtual switch which then:
- A) Sends them directly to the physical NIC without inspection
- B) Routes network messages to the target Virtual NIC
- C) Broadcasts to all VMs on all servers
- D) Drops packets that have no routing entry

---

**Q124.** In the Docker networking example, what subnet is created for the virtual network?
- A) 10.0.0.0/8
- B) 192.168.0.0/16
- C) 172.19.0.0/16
- D) 10.10.0.0/24

---

**Q125.** In the Docker networking example, what does Docker create to connect the virtual network to the external LAN?
- A) A physical bridge
- B) A virtual bridge (mybridge)
- C) A VXLAN tunnel
- D) A NAT gateway at the ISP

---

**Q126.** External Virtualization addresses which question?
- A) How VMs on the SAME server communicate?
- B) How VMs on DIFFERENT servers communicate?
- C) How physical routers are configured?
- D) How DNS resolves VM hostnames?

---

**Q127.** In External Virtualization, the Hypervisor holds:
- A) Physical routing tables only
- B) Virtual iptables with the physical servers hosting the target VMs
- C) VLAN configuration for all external switches
- D) DNS records for all VMs

---

### Section 12: VLAN

**Q128.** A VLAN (Virtual LAN) allows:
- A) Routing between different IP networks
- B) Grouping devices into separate, isolated sub-groups regardless of physical location
- C) Converting digital to analogue signals
- D) Distributing traffic across multiple servers

---

**Q129.** Which IEEE standard defines the VLAN tagging in Ethernet frames?
- A) IEEE 802.3
- B) IEEE 802.11
- C) IEEE 802.1Q
- D) IEEE 802.15.1

---

**Q130.** In the IEEE 802.1Q frame, the VLAN Tag (802.1Q Tag) is inserted between:
- A) Preamble and SFD
- B) Source Address and Length/Type fields
- C) Length/Type and Data fields
- D) Data and CRC

---

**Q131.** The 802.1Q VLAN tag contains a VID field of how many bits?
- A) 3 bits
- B) 1 bit
- C) 12 bits
- D) 16 bits

---

**Q132.** In the 802.1Q tag, what does TPID stand for?
- A) Tagged Protocol Identification
- B) Tag Protocol IDentifier
- C) Transfer Protocol ID
- D) Trunk Port Identification

---

**Q133.** The maximum number of VLANs supported by IEEE 802.1Q is:
- A) 256
- B) 1024
- C) 4096
- D) 65536

---

**Q134.** In a VLAN-aware network, devices in the SAME VLAN:
- A) Require inter-VLAN routing to communicate
- B) Cannot communicate without a router
- C) Form a group and communicate directly
- D) Must use VXLAN for communication

---

**Q135.** Devices from DIFFERENT VLANs require:
- A) A new physical cable
- B) Inter-VLAN routing
- C) A Hub to broadcast between groups
- D) A modem to convert signals

---

**Q136.** Which of the following is listed as a PRO of VLANs?
- A) Simplifies configuration
- B) No need for managed switches
- C) Security through network traffic isolation
- D) No inter-VLAN routing needed

---

**Q137.** Which of the following is listed as a CON of VLANs?
- A) Better security
- B) Interoperability issues with legacy/non-aware devices
- C) Reduced bandwidth
- D) Requires physical separation of networks

---

### Section 13: VXLAN

**Q138.** Why is VXLAN needed over traditional VLAN (IEEE 802.1Q)?
- A) VLAN supports too many segments
- B) VLAN IDs are 12 bits (only 4096 segments) — not enough for cloud data centers
- C) VLAN cannot support Ethernet
- D) VLAN does not support multicast

---

**Q139.** The "Overlay Network" in VXLAN refers to:
- A) The physical network connection moving data between switches
- B) The virtualized VLAN connection between two Layer-2 switches
- C) The TCP/IP stack on each VM
- D) The management network for the hypervisor

---

**Q140.** The "Underlay Network" in VXLAN refers to:
- A) The virtualized VLAN connection
- B) The VM-to-VM communication layer
- C) The physical network connection moving data from one switch to another
- D) The application-level virtual network

---

**Q141.** VXLAN virtualizes VLAN using which type of devices?
- A) Layer-1 Physical repeaters
- B) Layer-2 switches only
- C) Layer-3 Switches/Routers
- D) Application-layer gateways

---

**Q142.** In VXLAN, the original Ethernet frame is encapsulated in:
- A) A TCP segment
- B) A UDP message with a VXLAN header
- C) An ICMP packet
- D) An HTTP request

---

**Q143.** The VXLAN header's primary purpose is to:
- A) Provide encryption for the data
- B) Identify servers in the same VXLAN group (VNI)
- C) Assign public IP addresses
- D) Perform NAT translation

---

**Q144.** VNI in VXLAN stands for:
- A) Virtual Network Infrastructure
- B) VXLAN Network Identifier
- C) Virtual Node Interface
- D) VLAN Network Index

---

**Q145.** In the VXLAN packet flow diagram (6 steps), in step 3 which entity encapsulates the original packet into a UDP/VXLAN packet?
- A) The destination VM
- B) The VTEP (VXLAN Tunnel Endpoint) on the source side
- C) The Layer 3 switch in the underlay
- D) The DNS server

---

**Q146.** VTEP stands for:
- A) Virtual Tunnel Endpoint Protocol
- B) VXLAN Tunnel End Point
- C) Virtual Transfer Encoding Protocol
- D) VLAN Topology Extension Point

---

### Section 14: DVS and VPC

**Q147.** A Distributed Virtual Switch (DVS) is:
- A) A physical switch distributed across multiple data centers
- B) Multiple Network Hypervisors emulating the operation of a switch across multiple host machines
- C) A Layer-3 router that handles VXLAN tunnels
- D) A software load balancer

---

**Q148.** Which of the following is a PRO of a DVS?
- A) Requires no configuration
- B) Provides virtual switch ports that are configurable (e.g., control data rate)
- C) Eliminates the need for physical switches
- D) Directly replaces Layer 3 routing

---

**Q149.** In a DVS, LAN ports with the same attributes can form:
- A) A VXLAN
- B) A VLAN
- C) A VPC
- D) A NAT table

---

**Q150.** VPC stands for:
- A) Virtual Processing Cloud
- B) Virtual Private Cloud
- C) Virtualized Protocol Controller
- D) Variable Public Connection

---

**Q151.** A VPC creates:
- A) Physical dedicated networks in public cloud
- B) Private virtual networks inside public cloud
- C) Public IP address pools for cloud customers
- D) Hardware-level isolation between data centers

---

**Q152.** Which of the following components is found in a VPC (as shown in the AWS VPC example)?
- A) Physical TOR switches
- B) Internet Gateway, NAT Gateway, Route Tables, Subnets
- C) Manchester encoding circuits
- D) IEEE 802.3 Ethernet frames only

---

**Q153.** In the AWS VPC example, a Public VPC Subnet has which IP range?
- A) 172.16.0.0/16
- B) 10.0.0.0/24
- C) 192.168.1.0/24
- D) 10.10.0.0/16

---

**Q154.** Which VPC component is identified as "Gateways" in the lecture?
- A) Route Tables
- B) Internet Gateway and NAT Gateway
- C) Subnets
- D) VPN Connection

---

**Q155.** Which VPC component is identified as "VLAN Segmentation" in the lecture?
- A) Internet Gateway
- B) NAT Gateway
- C) Route Tables (public/private subnets)
- D) VPN Gateway

---

**Q156.** Which of the following is listed as a PRO of VPCs in the lecture?
- A) No need for any gateways
- B) Eliminates routing entirely
- C) Traffic Control (Gateways), Security & Isolation (VLAN), Flexible Network as a Service
- D) Requires dedicated physical hardware

---

**Q157.** In the AWS VPC example, which service allows connectivity between the VPC and a Corporate Data Center?
- A) Internet Gateway
- B) NAT Gateway
- C) VPN Gateway + VPN Connection + Customer Gateway
- D) Load Balancer

---

**Q158.** In a VPC, "Virtual Routers" correspond to which VPC component shown in the lecture diagram?
- A) Internet Gateway
- B) Subnets
- C) Route Tables
- D) VPN Connection

---

### Section 15: Mixed Tricky Questions

**Q159.** Which device would you use to connect two physically separate office networks that use different IP address ranges?
- A) Hub
- B) Repeater
- C) Router
- D) Bridge

---

**Q160.** A company wants to segment its employees into HR, Engineering, and Finance departments with isolated traffic, all sharing the same physical switches. Which technology should be used?
- A) VXLAN
- B) VLAN
- C) DVS
- D) VPC

---

**Q161.** A cloud provider needs to support millions of tenant virtual networks on the same physical infrastructure. Traditional VLANs (802.1Q) are insufficient because:
- A) VLANs are too fast
- B) VLAN IDs are limited to 4096 segments (12-bit VID)
- C) VLANs require dedicated physical hardware per tenant
- D) VLANs don't support Layer 3 routing

---

**Q162.** In the TCP/IP model, when a VM makes a `sendmsg()` system call, the hypervisor traps it at which conceptual layer?
- A) Application Layer
- B) Internet Layer
- C) Transport Layer
- D) Network Access Layer (using virtual NICs acting at the physical/data link boundary)

---

**Q163.** What is the correct order of events when a browser loads www.google.com, from first to last?
- A) Render HTML → Send HTTP → DNS → TCP SYN
- B) DNS query → TCP handshake → Send HTTP request → Wait for response → Render HTML
- C) TCP handshake → DNS query → Send HTTP → Render HTML
- D) Send HTTP → DNS → TCP handshake → Render HTML

---

**Q164.** Which of the following correctly pairs a network concept with its description?
- A) VTEP → physical router endpoint
- B) VXLAN Underlay → the virtual overlay tunnel
- C) PNIC → Physical Network Interface Card on the host server
- D) VNIC → the physical card in a Cloud switch

---

**Q165.** In the cloud data center hierarchy, a server in Rack 1 communicating with a server in Rack 3 (same sector) produces what type of traffic?
- A) North-South
- B) In-Rack
- C) East-West
- D) Internet-bound

---

**Q166.** Which IEEE 802.1Q sub-field is 3 bits and is used for Priority Code Point?
- A) CFI
- B) VID
- C) PRI
- D) TPID

---

**Q167.** In an Ethernet frame, the Preamble is:
- A) 1 byte — Start Frame
- B) 7 bytes — Synchronization/Notification for Receiver
- C) 6 bytes — MAC Address
- D) 4 bytes — CRC

---

**Q168.** Which protocol at the Internet layer is responsible for mapping IP addresses to MAC addresses?
- A) ICMP
- B) ARP (Address Resolution Protocol)
- C) OSPF
- D) BGP

---

**Q169.** RARP (Reverse Address Resolution Protocol) does which of the following?
- A) Maps IP to MAC
- B) Maps MAC to IP
- C) Routes packets between networks
- D) Resolves domain names to IPs

---

**Q170.** In a DVS setup across 3 host machines, the virtual switch spans:
- A) Only one host machine
- B) The physical switch layer only
- C) All host machines through coordinated hypervisors
- D) The internet backbone

---
