# 🌐 Network Devices

> *"Network devices are the building blocks of modern communication systems. They connect computers, forward data, improve network performance, provide Internet access, and enforce security policies. Understanding how these devices operate is essential for designing, managing, and securing computer networks."*

---

# 📖 Table of Contents

- Introduction
- What are Network Devices?
- Why Network Devices are Important
- Types of Network Devices
- Hub
- Switch
- Bridge
- Comparison Table
- Summary

---

# 📚 Introduction

A computer network consists of more than just computers and cables. To enable communication between devices, specialized networking hardware is required. These hardware components are known as **network devices**.

Network devices perform different functions depending on their role in the network. Some devices forward data, some connect different networks together, while others improve security or increase communication speed.

Without network devices, modern communication over local networks (LANs), metropolitan networks (MANs), and the Internet would not be possible.

Understanding the operation of networking devices is one of the most important skills for network engineers, cybersecurity analysts, cloud architects, and system administrators.

---

# 🌍 What are Network Devices?

Network devices are hardware components that facilitate communication between computers and other connected devices.

They are responsible for tasks such as:

- Connecting devices
- Forwarding packets
- Switching frames
- Routing traffic
- Extending network coverage
- Filtering malicious traffic
- Providing wireless connectivity
- Improving network performance

Each device operates at one or more layers of the OSI Model.

---

# 🎯 Why Network Devices are Important

Network devices provide several essential functions:

## Device Connectivity

They allow computers, printers, servers, and other devices to communicate.

---

## Resource Sharing

Users can share:

- Internet connections
- Files
- Printers
- Applications

---

## Traffic Management

Switches and routers manage data flow efficiently.

---

## Security

Firewalls, IDS, and IPS protect the network against cyber threats.

---

## Scalability

Additional devices can be added as the network grows.

---

# 📊 Network Devices and Their OSI Layers

| Device | Primary OSI Layer |
|----------|-------------------|
| Hub | Layer 1 |
| Repeater | Layer 1 |
| Bridge | Layer 2 |
| Switch | Layer 2 |
| Layer 3 Switch | Layer 3 |
| Router | Layer 3 |
| Firewall | Layer 3–7 |
| Gateway | Layer 7 |
| Access Point | Layer 2 |
| Modem | Layer 1/2 |
| IDS | Layer 3–7 |
| IPS | Layer 3–7 |

---

# 🔌 Hub

---

## 📖 Overview

A **Hub** is one of the simplest networking devices. It operates at the **Physical Layer (Layer 1)** of the OSI Model.

A hub receives electrical signals from one device and broadcasts the same signal to every other connected device without examining the destination address.

Since it does not perform intelligent forwarding, hubs are considered inefficient and are rarely used in modern networks.

---

## 🏗️ Architecture

```text
          Hub
      ┌────┼────┐
      │    │    │
    PC1   PC2  PC3
           │
         Printer
```

---

## ⚙️ Working Process

1. A device sends data.
2. The hub receives the electrical signal.
3. The hub copies the signal.
4. Every connected device receives the data.
5. Only the intended device processes the information.

---

## 🎯 Characteristics

- Layer 1 Device
- No MAC Address Table
- Broadcasts all traffic
- No packet filtering
- Shared bandwidth
- Half Duplex communication

---

## ✅ Advantages

- Low cost
- Easy installation
- Simple configuration
- Useful for learning purposes

---

## ❌ Disadvantages

- High collision rate
- Poor performance
- Low security
- Shared bandwidth
- Broadcasts every packet

---

## 🔐 Security Risks

- Packet Sniffing
- Data Leakage
- Network Congestion
- Denial of Service (DoS)

---

## 🛡️ Best Practices

Since hubs provide no traffic isolation, they should generally be replaced with switches in production environments.

---

## 🌍 Real-World Applications

Historically used in:

- Small laboratories
- Educational environments
- Legacy Ethernet networks

Today they are rarely deployed.

---

# 🔀 Switch

---

## 📖 Overview

A **Switch** is the most common networking device used in Local Area Networks (LANs). It operates primarily at the **Data Link Layer (Layer 2)** and forwards Ethernet frames based on **MAC addresses**.

Unlike a hub, a switch learns the MAC addresses of connected devices and forwards traffic only to the intended destination. This greatly improves performance and reduces unnecessary traffic.

Modern enterprise switches may also support Layer 3 features such as routing between VLANs.

---

## 🏗️ Architecture

```text
                 Switch
             ┌────┼────┐
             │    │    │
           PC1   PC2  PC3
             │
          File Server
```

---

## ⚙️ How a Switch Works

1. A device sends an Ethernet frame.
2. The switch reads the source MAC address.
3. It updates its MAC Address Table.
4. It checks the destination MAC address.
5. The frame is forwarded only to the correct port.

If the destination MAC is unknown, the switch floods the frame to all ports except the source.

---

## 📋 MAC Address Table Example

| MAC Address | Port |
|-------------|------|
| AA:BB:CC:11:22:33 | Port 1 |
| DD:EE:FF:44:55:66 | Port 2 |
| 00:11:22:33:44:55 | Port 3 |

---

## 🎯 Characteristics

- Layer 2 Device
- Intelligent forwarding
- MAC learning
- Dedicated bandwidth
- Full Duplex communication
- Collision-free operation

---

## ✅ Advantages

- High performance
- Reduced collisions
- Better security than hubs
- Efficient bandwidth utilization
- Supports VLANs
- Easy scalability

---

## ❌ Disadvantages

- More expensive than hubs
- Vulnerable to MAC flooding attacks
- Requires configuration in enterprise environments

---

## 🔐 Common Attacks

- MAC Flooding
- ARP Spoofing
- VLAN Hopping
- CAM Table Overflow

---

## 🛡️ Security Best Practices

- Enable Port Security
- Configure VLAN Segmentation
- Enable DHCP Snooping
- Use Dynamic ARP Inspection (DAI)
- Disable Unused Ports
- Monitor Switch Logs

---

## 🌍 Real-World Applications

Switches are used in:

- Home networks
- Offices
- Schools
- Universities
- Hospitals
- Data centers
- Enterprise LANs

---

# 🌉 Bridge

---

## 📖 Overview

A **Bridge** is a Layer 2 networking device that connects two or more LAN segments. It forwards or filters traffic based on MAC addresses, reducing unnecessary traffic and improving network performance.

Bridges were widely used before modern switches became common. Today, their functionality is largely integrated into switches.

---

## 🏗️ Architecture

```text
LAN Segment A
      │
   ┌───────┐
   │ Bridge│
   └───────┘
      │
LAN Segment B
```

---

## ⚙️ Working Process

1. The bridge receives a frame.
2. It examines the destination MAC address.
3. If the destination is on the same segment, the frame is filtered.
4. If the destination is on another segment, the frame is forwarded.

---

## 🎯 Characteristics

- Layer 2 Device
- MAC Address Learning
- Traffic Filtering
- Collision Domain Separation

---

## ✅ Advantages

- Reduces unnecessary traffic
- Improves network performance
- Connects LAN segments
- Filters frames intelligently

---

## ❌ Disadvantages

- Slower than modern switches
- Limited scalability
- Mostly replaced by switches

---

## 🔐 Security Risks

- MAC Spoofing
- Broadcast Storms
- ARP Spoofing

---

## 🛡️ Security Best Practices

- Segment networks using VLANs
- Monitor MAC address tables
- Restrict unauthorized devices

---

## 🌍 Real-World Applications

Bridges are still found in:

- Legacy Ethernet environments
- Industrial control networks
- Specialized network segmentation scenarios

---

# 📊 Hub vs Switch vs Bridge

| Feature | Hub | Bridge | Switch |
|---------|-----|--------|--------|
| OSI Layer | 1 | 2 | 2 |
| Address Used | None | MAC | MAC |
| Collision Domain | One | Separate | Separate per Port |
| Broadcast Traffic | All Ports | Filtered | Intelligent Forwarding |
| Speed | Low | Medium | High |
| Security | Low | Medium | High |
| Duplex | Half | Half/Full | Full |
| Modern Usage | Rare | Limited | Very Common |

---

# 🌐 Router

---

## 📖 Overview

A **Router** is a Layer 3 (Network Layer) device responsible for connecting multiple networks and forwarding packets based on **IP addresses**. Routers determine the most efficient path for data to travel between networks, making them one of the most important devices in modern networking.

Unlike switches, which operate within a Local Area Network (LAN), routers connect different networks such as home networks, enterprise networks, and the Internet.

Every time you browse a website or access a cloud application, your data passes through one or more routers.

---

## 🏗️ Architecture

```text
                Internet
                    │
             ┌─────────────┐
             │   Router    │
             └─────────────┘
                │       │
         Office LAN   Guest LAN
             │            │
         Switches     Access Point
```

---

## ⚙️ How a Router Works

1. Receives an IP packet.
2. Reads the destination IP address.
3. Consults the routing table.
4. Selects the best available route.
5. Forwards the packet to the next hop.

---

## 📋 Routing Table Example

| Destination Network | Next Hop | Interface |
|---------------------|----------|-----------|
| 192.168.1.0/24 | Direct | Gig0/0 |
| 10.10.0.0/16 | 192.168.1.1 | Gig0/1 |
| 0.0.0.0/0 | ISP Gateway | WAN |

---

## 🎯 Characteristics

- Layer 3 Device
- Uses IP Addresses
- Connects Multiple Networks
- Supports NAT
- Supports DHCP
- Supports Routing Protocols

---

## ✅ Advantages

- Connects different networks
- Supports Internet access
- Provides network segmentation
- Improves security
- Supports VPNs

---

## ❌ Disadvantages

- Higher cost than switches
- More complex configuration
- Routing introduces processing overhead

---

## 🔐 Common Attacks

- IP Spoofing
- Routing Table Poisoning
- BGP Hijacking
- DoS Attacks

---

## 🛡️ Security Best Practices

- Disable unused services
- Update firmware regularly
- Configure ACLs
- Enable secure routing protocols
- Use VPNs for remote access

---

## 🌍 Real-World Applications

- Home Routers
- Enterprise Networks
- ISP Infrastructure
- Cloud Networks
- Data Centers

---

# 📡 Modem

---

## 📖 Overview

A **Modem** (Modulator/Demodulator) converts digital data from computers into signals suitable for transmission over communication lines and converts incoming signals back into digital data.

Although many home devices combine modem and router functionality, their roles are different.

---

## 🎯 Responsibilities

- Connect to ISP
- Signal conversion
- Internet connectivity
- WAN communication

---

## 🌐 Types of Modems

- DSL Modem
- Cable Modem
- Fiber ONT
- Cellular Modem
- Satellite Modem

---

## ✅ Advantages

- Internet connectivity
- Supports broadband communication
- Easy installation

---

## ❌ Disadvantages

- Dependent on ISP infrastructure
- Performance varies by connection type

---

## 🌍 Real-World Applications

- Home Internet
- Office Internet
- Fiber Networks
- Mobile Broadband

---

# 📶 Wireless Access Point (WAP)

---

## 📖 Overview

A **Wireless Access Point (WAP)** enables wireless devices to connect to a wired network using Wi-Fi standards such as IEEE 802.11.

Access Points extend wireless coverage and allow laptops, smartphones, and tablets to communicate with the network.

---

## 🏗️ Architecture

```text
               Router
                  │
             Ethernet
                  │
          ┌────────────┐
          │ Access Pt. │
          └────────────┘
            ))   ))   ))
         Laptop Phone Tablet
```

---

## 🎯 Responsibilities

- Wireless connectivity
- Client authentication
- Signal broadcasting
- Roaming support

---

## 🌐 Wi-Fi Standards

| Standard | Frequency | Maximum Speed |
|-----------|-----------|---------------|
| 802.11a | 5 GHz | 54 Mbps |
| 802.11b | 2.4 GHz | 11 Mbps |
| 802.11g | 2.4 GHz | 54 Mbps |
| 802.11n | 2.4 / 5 GHz | 600 Mbps |
| 802.11ac | 5 GHz | Several Gbps |
| 802.11ax (Wi-Fi 6) | 2.4 / 5 GHz | Higher throughput and efficiency |

---

## 🔐 Common Attacks

- Evil Twin
- Rogue Access Point
- Deauthentication Attack
- WPA Password Cracking

---

## 🛡️ Security Best Practices

- WPA3 Encryption
- Strong Wi-Fi Passwords
- Disable WPS
- MAC Filtering
- Guest Network Isolation

---

# 📢 Repeater

---

## 📖 Overview

A **Repeater** is a Layer 1 device that regenerates weakened electrical or optical signals to extend the communication distance.

It does not inspect or modify data—it simply amplifies and retransmits the signal.

---

## 🏗️ Architecture

```text
PC ───── Repeater ───── Switch
```

---

## Advantages

- Extends network distance
- Reduces signal degradation
- Low cost

---

## Disadvantages

- Cannot filter traffic
- No security functions
- Does not reduce collisions

---

## Real-World Applications

- Long Ethernet runs
- Fiber optic links
- Industrial networks

---

# 🌉 Gateway

---

## 📖 Overview

A **Gateway** connects networks that use different communication protocols or architectures.

Unlike routers, gateways can translate between different protocols, allowing otherwise incompatible systems to communicate.

---

## Responsibilities

- Protocol Translation
- Network Interconnection
- Data Conversion
- Security Enforcement

---

## Examples

- Email Gateway
- VoIP Gateway
- Cloud Gateway
- IoT Gateway

---

## Security Best Practices

- Authentication
- Encryption
- Logging
- Protocol Validation

---

# 🌍 Proxy Server

---

## 📖 Overview

A **Proxy Server** acts as an intermediary between clients and external servers.

Instead of clients connecting directly to the Internet, requests pass through the proxy.

---

## Benefits

- User anonymity
- Web filtering
- Content caching
- Malware protection
- Access control

---

## Types of Proxy

- Forward Proxy
- Reverse Proxy
- Transparent Proxy
- Anonymous Proxy

---

## Common Attacks

- Proxy Bypass
- Misconfiguration
- Credential Theft

---

## Security Best Practices

- Authentication
- HTTPS Inspection
- Logging
- Access Policies

---

# ⚖️ Load Balancer

---

## 📖 Overview

A **Load Balancer** distributes incoming network traffic across multiple servers to improve performance, reliability, and availability.

Instead of sending all requests to one server, the load balancer intelligently distributes requests based on predefined algorithms.

---

## 🏗️ Architecture

```text
              Internet
                  │
          ┌─────────────┐
          │ Load Balancer│
          └─────────────┘
          /      |      \
     Web1     Web2     Web3
```

---

## Load Balancing Algorithms

- Round Robin
- Least Connections
- Least Response Time
- Weighted Round Robin
- IP Hash

---

## Advantages

- High Availability
- Scalability
- Fault Tolerance
- Better Performance

---

## Security Features

- SSL Offloading
- DDoS Protection
- Health Monitoring
- Rate Limiting

---

## Real-World Applications

- Cloud Platforms
- Banking Systems
- E-commerce Websites
- Streaming Services

---

# 📊 Device Comparison

| Device | OSI Layer | Address Used | Primary Function |
|----------|-----------|--------------|------------------|
| Router | 3 | IP | Connects Networks |
| Modem | 1–2 | N/A | ISP Connectivity |
| Access Point | 2 | MAC | Wireless Access |
| Repeater | 1 | None | Signal Regeneration |
| Gateway | 7 | Protocol-Based | Protocol Translation |
| Proxy Server | 7 | URL/IP | Intermediary Communication |
| Load Balancer | 4–7 | IP/Ports | Traffic Distribution |

---

# 🔥 Firewall

---

## 📖 Overview

A **Firewall** is a network security device that monitors, filters, and controls incoming and outgoing network traffic based on predefined security rules.

It acts as a protective barrier between trusted internal networks and untrusted external networks, such as the Internet.

Modern firewalls can inspect traffic at multiple layers of the OSI model and provide advanced security features including application awareness, intrusion prevention, VPN support, and malware detection.

---

## 🏗️ Firewall Architecture

```text
                 Internet
                     │
             ┌────────────────┐
             │    Firewall    │
             └────────────────┘
                     │
        ┌────────────┼────────────┐
        │            │            │
     LAN Users    Web Server   Database
```

---

## 🎯 Functions

- Packet Filtering
- Stateful Inspection
- Application Filtering
- VPN Support
- Network Address Translation (NAT)
- Access Control
- Traffic Monitoring

---

## Types of Firewalls

### Packet Filtering Firewall

- Examines packet headers
- Uses IP addresses and port numbers
- Fast but limited inspection

---

### Stateful Firewall

- Tracks active sessions
- Allows only legitimate return traffic
- More secure than packet filtering

---

### Proxy Firewall

- Acts as an intermediary
- Hides internal network
- Filters application traffic

---

### Next Generation Firewall (NGFW)

Features include:

- Deep Packet Inspection
- Intrusion Prevention
- Malware Detection
- SSL Inspection
- Application Awareness

---

## Advantages

- Blocks unauthorized access
- Protects internal resources
- Monitors network traffic
- Supports VPN connections

---

## Common Attacks

- Firewall Evasion
- Rule Misconfiguration
- Application Layer Attacks

---

## Security Best Practices

- Apply the principle of least privilege
- Review firewall rules regularly
- Update firmware
- Enable logging
- Remove unused rules

---

# 🚨 Intrusion Detection System (IDS)

---

## 📖 Overview

An **Intrusion Detection System (IDS)** monitors network or host activity to identify suspicious or malicious behavior.

Unlike a firewall, an IDS does **not** block attacks automatically. It generates alerts so that administrators can investigate and respond.

---

## Types of IDS

### Network IDS (NIDS)

Monitors traffic flowing through the network.

Example:

- Snort
- Suricata
- Zeek

---

### Host IDS (HIDS)

Monitors activity on an individual computer.

Examples:

- OSSEC
- Wazuh

---

## Detection Methods

### Signature-Based Detection

Detects known attack patterns.

Advantages

- Fast
- Accurate for known threats

Disadvantages

- Cannot detect unknown attacks

---

### Anomaly-Based Detection

Detects behavior that differs from normal activity.

Advantages

- Detects Zero-Day attacks
- Detects insider threats

Disadvantages

- Higher false positives

---

## Advantages

- Detects attacks early
- Provides visibility into network activity
- Supports forensic investigations

---

## Limitations

- Does not automatically stop attacks
- Requires tuning to reduce false positives

---

# 🛡️ Intrusion Prevention System (IPS)

---

## 📖 Overview

An **Intrusion Prevention System (IPS)** performs the same monitoring functions as an IDS but can also **take immediate action** to block malicious traffic.

An IPS is deployed inline with network traffic, allowing it to prevent attacks before they reach their targets.

---

## Actions Performed

- Block malicious packets
- Reset connections
- Drop traffic
- Update firewall rules
- Generate alerts

---

## Advantages

- Prevents attacks in real time
- Reduces manual intervention
- Protects critical systems

---

## Challenges

- False positives can block legitimate traffic
- Requires regular signature updates

---

# 📊 IDS vs IPS Comparison

| Feature | IDS | IPS |
|----------|-----|-----|
| Detects Threats | ✅ | ✅ |
| Blocks Attacks | ❌ | ✅ |
| Generates Alerts | ✅ | ✅ |
| Inline Deployment | ❌ | ✅ |
| Performance Impact | Low | Moderate |
| False Positive Risk | Medium | Higher |

---

# 💻 Network Interface Card (NIC)

---

## 📖 Overview

A **Network Interface Card (NIC)** enables a computer or server to connect to a wired or wireless network.

Every NIC contains a unique **MAC Address**, which identifies the device at the Data Link Layer.

Modern motherboards typically include an integrated NIC, while servers often use dedicated high-speed NICs.

---

## Responsibilities

- Physical network connection
- MAC addressing
- Frame transmission
- Frame reception
- Error checking

---

## Types

- Ethernet NIC
- Wireless NIC
- Fiber NIC
- Virtual NIC

---

## Real-World Examples

- Laptop Ethernet Adapter
- Wi-Fi Adapter
- Server 10G NIC
- Virtual Machine Adapter

---

# 🏢 Enterprise Network Architecture Example

```text
                     Internet
                         │
                  ISP Modem/ONT
                         │
                    Edge Router
                         │
                  Next-Gen Firewall
                         │
                 Core Layer Switch
                 ┌────────┴────────┐
                 │                 │
          Distribution Switch  Distribution Switch
             │        │             │        │
         Access    Servers      Access    Wireless AP
         Switches               Switches
             │                     │
         PCs, Printers         Laptops, Phones
```

---

# 🔐 Security Best Practices

To build secure and reliable enterprise networks:

- Deploy firewalls at network boundaries.
- Enable IDS and IPS for monitoring and prevention.
- Segment networks using VLANs.
- Disable unused switch ports.
- Secure wireless networks with WPA3.
- Update firmware regularly.
- Monitor logs using a SIEM platform.
- Use strong authentication and MFA.
- Implement Network Access Control (NAC).
- Follow the principle of least privilege.

---

# 🌍 Real-World Device Deployment

| Environment | Common Devices |
|-------------|----------------|
| Home Network | Modem, Router, Switch, Wi-Fi AP |
| Office | Router, Managed Switches, Firewall, AP |
| University | Core Switches, Routers, IDS, IPS |
| Hospital | Firewalls, VLANs, Load Balancers |
| Cloud Data Center | Routers, NGFWs, Load Balancers, Proxy Servers |

---

# 💼 Interview Questions

## Beginner

1. What is a network device?
2. What is the difference between a hub and a switch?
3. Which OSI layer does a router operate on?
4. What is the purpose of a modem?
5. What is a firewall?

---

## Intermediate

6. Explain how a switch learns MAC addresses.
7. What is the role of an Access Point?
8. Compare IDS and IPS.
9. Explain NAT on a router.
10. What is a proxy server?

---

## Advanced

11. Compare Layer 2 and Layer 3 switches.
12. How does a Next Generation Firewall differ from a traditional firewall?
13. Explain MAC flooding attacks.
14. Design a secure enterprise network architecture.
15. Explain how load balancing improves availability.

---

# 📝 Multiple Choice Questions

### Question 1

Which device operates primarily at Layer 3?

- A. Hub
- B. Switch
- C. Router
- D. Repeater

**Answer:** C

---

### Question 2

Which device broadcasts every incoming frame?

- A. Switch
- B. Hub
- C. Router
- D. Firewall

**Answer:** B

---

### Question 3

Which device blocks malicious traffic automatically?

- A. IDS
- B. IPS
- C. Bridge
- D. Modem

**Answer:** B

---

### Question 4

Which device translates domain names?

- A. Router
- B. DNS Server
- C. Switch
- D. Gateway

**Answer:** B

---

### Question 5

What uniquely identifies a NIC on a local network?

- A. IP Address
- B. Port Number
- C. MAC Address
- D. VLAN ID

**Answer:** C

---

# 🧪 Practical Labs

## Lab 1 — Identify Network Devices

Draw your home or office network and identify:

- Router
- Switch
- Access Point
- Firewall
- Connected devices

---

## Lab 2 — View MAC Address

### Windows

```cmd
ipconfig /all
```

### Linux

```bash
ip link show
```

Record the MAC address of your network interface.

---

## Lab 3 — Analyze ARP Table

```bash
arp -a
```

Observe the mapping between IP addresses and MAC addresses.

---

## Lab 4 — Capture Network Traffic

Tool:

- Wireshark

Capture packets and identify:

- ARP
- ICMP
- TCP
- HTTP/HTTPS

Determine which devices are involved in forwarding the traffic.

---

## Lab 5 — Simulate a Small Enterprise Network

Using Cisco Packet Tracer or GNS3:

- Add a router
- Add two switches
- Add a firewall
- Add a wireless access point
- Connect multiple PCs
- Configure IP addressing
- Verify connectivity with `ping`

---

# 📚 Chapter Summary

In this chapter, we explored the major networking devices used in modern computer networks.

Topics covered include:

- Hub
- Switch
- Bridge
- Router
- Modem
- Wireless Access Point
- Repeater
- Gateway
- Proxy Server
- Load Balancer
- Firewall
- Intrusion Detection System (IDS)
- Intrusion Prevention System (IPS)
- Network Interface Card (NIC)

We also examined:

- OSI layer mapping
- Device functions
- Enterprise deployment
- Security threats
- Best practices
- Interview questions
- MCQs
- Practical labs

A strong understanding of networking devices is essential for designing efficient, scalable, and secure networks. These devices form the foundation of enterprise infrastructure and are central to the work of network engineers and cybersecurity professionals.

---

# 📚 Further Reading

Continue to the next chapter:

➡ **08-Firewall-IDS-IPS.md**

Topics include:

- Firewall architecture
- Packet filtering
- Stateful inspection
- Proxy firewalls
- Next Generation Firewalls (NGFW)
- IDS types and detection methods
- IPS deployment
- Rule creation
- Packet analysis
- Real-world attack scenarios
- Practical labs

---

⬅️ **Previous:** `IP-Addressing.md`  
➡️ **Next:** `Firewall-IDS-IPS.md`
- 
