# 🌐 Types of Computer Networks

> *"Computer networks are classified based on their geographical coverage, communication technologies, ownership, and purpose. Understanding different network types helps network engineers design scalable, efficient, and secure communication infrastructures."*

---

# 📖 Table of Contents

- Introduction
- Network Classification
- Personal Area Network (PAN)
- Local Area Network (LAN)
- Wireless Local Area Network (WLAN)
- Campus Area Network (CAN)
- Comparison Table
- Summary

---

# 📚 Introduction

Computer networks vary in size, purpose, ownership, and geographical coverage. A small Bluetooth connection between a phone and headphones is considered a network, just as the global Internet connecting billions of devices is also a network.

To better understand and design these systems, networks are classified into different categories based on:

- Geographic coverage
- Ownership
- Communication technology
- Performance
- Intended use

Each network type serves a different purpose and uses different technologies to provide communication between devices.

Selecting the appropriate network type depends on several factors including the number of users, required speed, budget, scalability, and security requirements.

---

# 🎯 Why Network Classification Matters

Understanding network types helps organizations:

- Design efficient infrastructures
- Reduce deployment costs
- Improve performance
- Enhance scalability
- Implement appropriate security controls
- Select suitable networking equipment

---

# 📊 Network Classification

Computer networks are commonly divided into:

| Network Type | Coverage Area |
|--------------|---------------|
| PAN | Personal Devices |
| LAN | Building or Office |
| WLAN | Wireless Local Network |
| CAN | Campus |
| MAN | City |
| WAN | Country or Globe |
| SAN | Storage Infrastructure |
| VPN | Secure Virtual Network |

---

# 📱 Personal Area Network (PAN)

---

## 📖 Overview

A **Personal Area Network (PAN)** is the smallest type of computer network.

It connects devices located within a few meters of an individual user.

Typical communication range:

```
1–10 meters
```

PANs are commonly used for connecting personal electronic devices.

---

## 🏗️ PAN Architecture

```text
        Smart Watch
              │
              │ Bluetooth
              │
Laptop ───── Smartphone ───── Earbuds
              │
         Fitness Band
```

---

## Technologies

- Bluetooth
- USB
- NFC
- Infrared (IR)
- Zigbee

---

## Characteristics

- Short range
- Low power consumption
- Personal ownership
- Easy setup
- Low cost

---

## Advantages

- Simple installation
- Portable
- Energy efficient
- No complex infrastructure
- Convenient for personal devices

---

## Disadvantages

- Very limited range
- Low bandwidth
- Limited number of connected devices
- Interference from nearby wireless devices

---

## Security Risks

- Bluetooth Spoofing
- Bluejacking
- Bluesnarfing
- Unauthorized pairing

---

## Best Practices

- Disable Bluetooth when not in use
- Use strong pairing methods
- Keep device firmware updated
- Avoid connecting to unknown devices

---

## Real-World Examples

- Wireless earbuds
- Smart watches
- Fitness trackers
- Wireless keyboards
- Mobile payment devices

---

# 🏢 Local Area Network (LAN)

---

## 📖 Overview

A **Local Area Network (LAN)** connects computers and devices within a limited geographic area such as:

- Home
- School
- Office
- Laboratory
- Building

LANs are the most commonly deployed networks worldwide.

---

## LAN Architecture

```text
                Router
                   │
             ┌──────────┐
             │ Switch   │
             └──────────┘
           /     |      \
       PC-1    PC-2   Printer
                  │
              File Server
```

---

## Technologies

- Ethernet
- Fiber Optic
- Wi-Fi
- VLAN
- Gigabit Ethernet

---

## Characteristics

- High speed
- Low latency
- Privately owned
- Reliable communication
- Easy management

---

## Advantages

- Fast communication
- Resource sharing
- Centralized management
- Low operating cost
- High reliability

---

## Disadvantages

- Limited coverage
- Initial installation cost
- Requires maintenance
- Single-site deployment

---

## Security Risks

- Insider attacks
- ARP Spoofing
- MAC Flooding
- Unauthorized access

---

## Security Best Practices

- VLAN segmentation
- Port security
- Strong authentication
- Network monitoring
- Firewalls

---

## Real-World Examples

- Corporate offices
- Universities
- Schools
- Hospitals
- Data centers

---

# 📶 Wireless Local Area Network (WLAN)

---

## 📖 Overview

A **Wireless Local Area Network (WLAN)** provides the same functionality as a traditional LAN but uses wireless communication instead of Ethernet cables.

Devices communicate through Wireless Access Points using IEEE 802.11 standards.

---

## WLAN Architecture

```text
              Router
                 │
          Wireless Access Point
           ))      ))      ))
        Laptop   Phone   Tablet
```

---

## Common Standards

| Standard | Frequency |
|-----------|-----------|
| 802.11a | 5 GHz |
| 802.11b | 2.4 GHz |
| 802.11g | 2.4 GHz |
| 802.11n | 2.4 / 5 GHz |
| 802.11ac | 5 GHz |
| 802.11ax (Wi-Fi 6) | 2.4 / 5 GHz |

---

## Advantages

- Mobility
- Easy installation
- Flexible deployment
- Reduced cabling costs

---

## Disadvantages

- Signal interference
- Lower speed than wired LAN
- Security concerns
- Coverage limitations

---

## Security Risks

- Evil Twin Access Points
- Rogue Access Points
- Deauthentication Attacks
- WPA Password Cracking

---

## Security Best Practices

- WPA3 Encryption
- Strong Wi-Fi Passwords
- Disable WPS
- Guest Network Isolation
- Regular Firmware Updates

---

## Real-World Examples

- Coffee shops
- Airports
- Hotels
- Smart homes
- Enterprise wireless networks

---

# 🏫 Campus Area Network (CAN)

---

## 📖 Overview

A **Campus Area Network (CAN)** connects multiple Local Area Networks within a limited campus or institutional environment.

It is larger than a LAN but smaller than a Metropolitan Area Network (MAN).

CANs are commonly deployed by universities, hospitals, military bases, and corporate campuses.

---

## Campus Architecture

```text
      Building A
          │
      Core Switch
      /         \
Building B   Building C
      │           │
     LAN         LAN
```

---

## Characteristics

- High-speed fiber backbone
- Centralized administration
- Multiple buildings
- Private ownership

---

## Advantages

- High performance
- Efficient resource sharing
- Centralized security
- Easy expansion

---

## Disadvantages

- Higher deployment cost
- Complex infrastructure
- Requires dedicated IT staff

---

## Security Considerations

- VLAN Segmentation
- Access Control Lists
- Firewalls
- IDS/IPS
- Network Monitoring

---

## Real-World Examples

- University campuses
- Corporate headquarters
- Hospital campuses
- Government institutions

---

# 📊 PAN vs LAN vs WLAN vs CAN

| Feature | PAN | LAN | WLAN | CAN |
|----------|-----|-----|------|------|
| Coverage | Personal | Building | Building | Campus |
| Range | 1–10 m | Up to 1 km | Up to 100 m | Several km |
| Speed | Low | High | Medium–High | High |
| Ownership | Personal | Private | Private | Private |
| Technologies | Bluetooth | Ethernet | Wi-Fi | Fiber + Ethernet |
| Common Use | Personal Devices | Offices | Wireless Access | Universities |

---

# 🌆 Metropolitan Area Network (MAN)

---

## 📖 Overview

A **Metropolitan Area Network (MAN)** is a high-speed network that connects multiple Local Area Networks (LANs) across a city or metropolitan region.

A MAN covers a larger geographical area than a Campus Area Network (CAN) but is smaller than a Wide Area Network (WAN).

These networks are commonly deployed by:

- Internet Service Providers (ISPs)
- Government agencies
- Universities
- Financial institutions
- Large enterprises

MANs often use high-speed fiber optic links to interconnect buildings and offices.

---

# 🏗️ MAN Architecture

```text
            Office A
               │
        Fiber Backbone
               │
        ┌─────────────┐
        │ Core Router │
        └─────────────┘
          /     |      \
         /      |       \
 Office B   Office C   Data Center
```

---

# 🌐 Technologies Used

- Metro Ethernet
- Fiber Optic
- MPLS
- SDH / SONET
- DWDM

---

# 🎯 Characteristics

- City-wide coverage
- High bandwidth
- Fiber backbone
- Multiple interconnected LANs
- Centralized administration

---

# ✅ Advantages

- High-speed communication
- Reliable connectivity
- Efficient resource sharing
- Supports large organizations
- Easy inter-office communication

---

# ❌ Disadvantages

- High deployment cost
- Complex infrastructure
- Requires specialized networking equipment
- Dependent on service providers

---

# 🔐 Security Risks

- Fiber tapping
- Unauthorized access
- Routing attacks
- Distributed Denial-of-Service (DDoS)

---

# 🛡️ Security Best Practices

- VPN encryption
- MPLS security
- Firewalls
- IDS/IPS deployment
- Network segmentation

---

# 🌍 Real-World Examples

- City government networks
- University campuses across a city
- Bank branch connectivity
- ISP metropolitan networks

---

# 🌍 Wide Area Network (WAN)

---

## 📖 Overview

A **Wide Area Network (WAN)** connects multiple LANs, CANs, or MANs over large geographical areas, including countries and continents.

The Internet is the world's largest WAN.

Organizations use WANs to connect branch offices, cloud services, and remote employees.

---

# 🏗️ WAN Architecture

```text
        Branch Office A
              │
         MPLS / Internet
              │
       ┌─────────────┐
       │ ISP Network │
       └─────────────┘
          /      \
         /        \
 Branch B       Head Office
                  │
             Data Center
```

---

# 🌐 Technologies Used

- MPLS
- VPN
- Leased Lines
- Fiber Optic
- Satellite
- SD-WAN
- Internet

---

# 🎯 Characteristics

- Global coverage
- Connects multiple networks
- Managed by ISPs
- Supports remote access
- Higher latency than LAN

---

# ✅ Advantages

- Worldwide connectivity
- Remote collaboration
- Cloud integration
- Centralized services
- Business continuity

---

# ❌ Disadvantages

- Higher latency
- Expensive leased links
- Complex management
- ISP dependency

---

# 🔐 Security Risks

- Data interception
- BGP hijacking
- DDoS attacks
- Route manipulation
- Man-in-the-Middle (MITM)

---

# 🛡️ Security Best Practices

- IPSec VPN
- Zero Trust Network Access
- Encryption
- Firewalls
- Continuous monitoring

---

# 🌍 Real-World Examples

- The Internet
- Global enterprise networks
- International banking systems
- Cloud service providers

---

# 💾 Storage Area Network (SAN)

---

## 📖 Overview

A **Storage Area Network (SAN)** is a dedicated high-speed network designed specifically for connecting servers to centralized storage devices.

Unlike traditional LANs, SANs focus on storage traffic, providing high performance, low latency, and reliable access to shared storage resources.

SANs are commonly found in enterprise data centers where applications require fast access to large volumes of data.

---

# 🏗️ SAN Architecture

```text
             Storage Array
                  │
          Fibre Channel Switch
             /           \
            /             \
      Database Server   Backup Server
```

---

# 🌐 Technologies Used

- Fibre Channel (FC)
- Fibre Channel over Ethernet (FCoE)
- iSCSI
- NVMe over Fabrics

---

# 🎯 Characteristics

- Dedicated storage network
- Very high throughput
- Low latency
- Centralized storage management
- Highly scalable

---

# ✅ Advantages

- Fast storage access
- Improved data availability
- Centralized backups
- High scalability
- Reduced server storage requirements

---

# ❌ Disadvantages

- High implementation cost
- Specialized hardware
- Complex configuration
- Requires skilled administrators

---

# 🔐 Security Risks

- Unauthorized storage access
- Data theft
- Misconfigured storage permissions
- Insider threats

---

# 🛡️ Security Best Practices

- Access control
- Storage encryption
- Network isolation
- Multi-factor authentication
- Regular auditing

---

# 🌍 Real-World Examples

- Enterprise data centers
- Banking infrastructure
- Cloud storage platforms
- Virtualization clusters

---

# 🔒 Virtual Private Network (VPN)

---

## 📖 Overview

A **Virtual Private Network (VPN)** creates a secure, encrypted tunnel over a public network such as the Internet.

VPNs allow users and branch offices to communicate securely without requiring dedicated private communication lines.

Organizations widely use VPNs to enable secure remote work and connect geographically separated offices.

---

# 🏗️ VPN Architecture

```text
          Remote User
               │
        Encrypted Tunnel
               │
           Internet
               │
         VPN Gateway
               │
        Corporate Network
```

---

# 🌐 Types of VPN

## Remote Access VPN

Provides secure access for individual users connecting from remote locations.

Commonly used by:

- Remote employees
- IT administrators
- Business travelers

---

## Site-to-Site VPN

Connects two or more office networks securely.

Example:

```text
Head Office
      │
Encrypted Tunnel
      │
Branch Office
```

---

## Cloud VPN

Connects on-premises infrastructure with cloud platforms such as AWS, Microsoft Azure, or Google Cloud.

---

# 🔐 VPN Protocols

| Protocol | Description |
|----------|-------------|
| IPSec | Secure IP communication |
| OpenVPN | Open-source VPN |
| WireGuard | Lightweight and modern |
| SSL/TLS VPN | Browser-based secure access |
| L2TP/IPSec | Legacy VPN implementation |

---

# ✅ Advantages

- Secure communication
- Data encryption
- Remote access
- Lower cost than leased lines
- Improved privacy

---

# ❌ Disadvantages

- Encryption overhead
- Internet dependency
- Potential performance impact
- Configuration complexity

---

# 🔐 Security Best Practices

- Use strong encryption (AES-256)
- Enable Multi-Factor Authentication (MFA)
- Rotate encryption keys
- Monitor VPN logs
- Restrict user access based on roles

---

# 🌍 Real-World Examples

- Remote employees connecting to corporate networks
- Secure branch office connectivity
- Cloud administration
- Secure public Wi-Fi usage

---

# 🏢 Enterprise Network Example

```text
                    Internet
                         │
                    VPN Gateway
                         │
                   Core Firewall
                         │
                 Core Network Switch
             ┌───────────┼───────────┐
             │           │           │
          Office      Data Center   SAN
             │
         Remote Users
        (VPN Connection)
```

---

# 📊 MAN vs WAN vs SAN vs VPN

| Feature | MAN | WAN | SAN | VPN |
|----------|-----|-----|-----|-----|
| Coverage | City | Global | Data Center | Virtual |
| Purpose | Connect City Networks | Connect Distant Networks | Storage Communication | Secure Communication |
| Ownership | Organization / ISP | ISP / Enterprise | Enterprise | Organization |
| Primary Technology | Fiber | MPLS / Internet | Fibre Channel | IPSec / SSL |
| Typical Use | City Networks | Enterprise Connectivity | Enterprise Storage | Remote Access |

---

# 🏢 Enterprise Network Design

---

## 📖 Overview

Modern organizations rarely rely on a single network type. Instead, they combine multiple network types to create scalable, secure, and highly available infrastructures.

For example, a multinational company may use:

- LAN inside office buildings
- WLAN for wireless users
- CAN to connect multiple campus buildings
- MAN for city-wide offices
- WAN to connect global branches
- SAN for centralized storage
- VPN for remote employees

This layered approach improves performance, flexibility, and security while supporting business growth.

---

# 🏗️ Enterprise Network Architecture

```text
                         Internet
                             │
                       ISP Connection
                             │
                    Next Generation Firewall
                             │
                          Edge Router
                             │
                    Core Layer Switch
              ┌──────────────┼──────────────┐
              │              │              │
         Office LAN       Server LAN     SAN Network
              │              │              │
         Wireless AP     Database       Storage Array
              │
         Employee Devices
              │
         Remote Users
         (VPN Connection)
```

---

# 🌍 Real-World Network Examples

---

## 🏠 Home Network

Typical Components:

- Router
- Wi-Fi Access Point
- Laptop
- Smartphone
- Smart TV
- Printer

Network Types:

- LAN
- WLAN
- PAN

---

## 🏢 Small Business

Components:

- Router
- Firewall
- Switch
- Access Point
- NAS Storage
- Desktop PCs

Network Types:

- LAN
- WLAN
- VPN

---

## 🎓 University Campus

Components:

- Core Routers
- Distribution Switches
- Fiber Backbone
- Student Wi-Fi
- Data Center

Network Types:

- CAN
- LAN
- WLAN
- SAN

---

## 🏦 Banking Network

Components:

- Branch Offices
- MPLS WAN
- VPN
- Data Centers
- Disaster Recovery Site

Network Types:

- WAN
- MAN
- SAN
- VPN

---

## ☁️ Cloud Environment

Components:

- Virtual Networks
- Cloud Firewalls
- VPN Gateway
- Load Balancers
- Storage Clusters

Network Types:

- WAN
- VPN
- SAN

---

# 📊 Complete Comparison of Network Types

| Feature | PAN | LAN | WLAN | CAN | MAN | WAN | SAN | VPN |
|----------|-----|-----|------|-----|-----|-----|-----|-----|
| Coverage | Personal | Building | Building | Campus | City | Global | Data Center | Virtual |
| Ownership | Personal | Private | Private | Private | Enterprise / ISP | Enterprise / ISP | Enterprise | Enterprise |
| Speed | Low | High | Medium–High | High | High | Medium | Very High | Depends on Internet |
| Primary Technology | Bluetooth | Ethernet | Wi-Fi | Fiber | Metro Ethernet | MPLS / Internet | Fibre Channel | IPSec / SSL |
| Security Level | Low | Medium | Medium | High | High | High | Very High | High |
| Typical Users | Individual | Office | Mobile Users | Universities | City Offices | Global Companies | Data Centers | Remote Workers |

---

# 🔐 Security Considerations

Each network type presents unique security challenges and requires different protection mechanisms.

| Network Type | Common Risks | Recommended Security Controls |
|--------------|-------------|-------------------------------|
| PAN | Bluetooth attacks | Secure pairing, firmware updates |
| LAN | Insider attacks | VLANs, ACLs, Port Security |
| WLAN | Rogue APs, Wi-Fi cracking | WPA3, Strong passwords, Guest isolation |
| CAN | Unauthorized access | IDS/IPS, Segmentation, Monitoring |
| MAN | Fiber tapping | VPNs, Encryption, Firewalls |
| WAN | DDoS, Routing attacks | IPSec, Zero Trust, SD-WAN security |
| SAN | Storage theft | Encryption, Access Control, Auditing |
| VPN | Credential theft | MFA, Strong encryption, Logging |

---

# 📚 Best Practices

Organizations should follow these practices when designing and maintaining networks:

- Choose the appropriate network type for business requirements.
- Segment networks using VLANs.
- Encrypt sensitive traffic.
- Deploy firewalls and IDS/IPS.
- Use Multi-Factor Authentication (MFA).
- Monitor network activity continuously.
- Keep network devices updated.
- Perform regular vulnerability assessments.
- Implement backup and disaster recovery plans.
- Follow the Principle of Least Privilege.

---

# 🌍 Case Study

## Scenario

A company has:

- Headquarters in Mumbai
- Branch offices in Delhi and Bengaluru
- Remote employees working from home
- A centralized data center
- Cloud-hosted applications

### Network Design

- **LAN** for office communication
- **WLAN** for employee wireless access
- **CAN** connecting buildings at headquarters
- **WAN** connecting branch offices
- **SAN** for centralized storage
- **VPN** for secure remote access

### Benefits

- Centralized management
- Secure communication
- High availability
- Efficient resource sharing
- Scalability

---

# 💼 Interview Questions

## Beginner

1. What is a computer network?
2. What is the difference between LAN and WAN?
3. What is PAN?
4. What is WLAN?
5. What is a VPN?

---

## Intermediate

6. Compare LAN and CAN.
7. Explain the purpose of a SAN.
8. What technologies are used in WANs?
9. Why is a VPN important?
10. Explain the advantages of MAN.

---

## Advanced

11. Design a secure enterprise network using multiple network types.
12. Compare MPLS and SD-WAN.
13. Explain how SAN improves data center performance.
14. What are the security challenges of WLANs?
15. Describe how a multinational organization would combine LAN, WAN, SAN, and VPN technologies.

---

# 📝 Multiple Choice Questions (MCQs)

### Question 1

Which network type covers a single office building?

- A. WAN
- B. LAN
- C. MAN
- D. PAN

**Answer:** B

---

### Question 2

Which network type is specifically designed for centralized storage?

- A. WAN
- B. SAN
- C. MAN
- D. WLAN

**Answer:** B

---

### Question 3

Which technology provides secure communication over the Internet?

- A. Ethernet
- B. Bluetooth
- C. VPN
- D. NFC

**Answer:** C

---

### Question 4

Which network type is commonly used by universities with multiple buildings?

- A. PAN
- B. CAN
- C. SAN
- D. WAN

**Answer:** B

---

### Question 5

Which network type typically has the largest geographic coverage?

- A. LAN
- B. MAN
- C. WAN
- D. PAN

**Answer:** C

---

# 🧪 Practical Labs

## Lab 1 — Design a Home Network

Draw a home network including:

- Router
- Laptop
- Smartphone
- Smart TV
- Wireless Access Point

Identify the network types used.

---

## Lab 2 — Enterprise Network Design

Using Cisco Packet Tracer:

- Create two LANs.
- Connect them with a router.
- Configure IP addresses.
- Verify connectivity using `ping`.

---

## Lab 3 — Configure a WLAN

Tasks:

- Configure an Access Point.
- Enable WPA3 security.
- Connect wireless clients.
- Test Internet access.

---

## Lab 4 — Simulate a Site-to-Site VPN

Using a network simulator:

- Create two branch offices.
- Configure routers.
- Establish a secure VPN tunnel.
- Verify encrypted communication.

---

## Lab 5 — Network Classification Exercise

For each scenario below, identify the correct network type:

1. Smartwatch connected to a smartphone
2. School computer lab
3. University campus
4. City-wide government offices
5. Global banking network
6. Enterprise storage infrastructure
7. Employee connecting securely from home

---

# 📚 Chapter Summary

In this chapter, we explored the major types of computer networks used in modern environments.

Topics covered include:

- Personal Area Network (PAN)
- Local Area Network (LAN)
- Wireless Local Area Network (WLAN)
- Campus Area Network (CAN)
- Metropolitan Area Network (MAN)
- Wide Area Network (WAN)
- Storage Area Network (SAN)
- Virtual Private Network (VPN)
- Enterprise network architecture
- Security considerations
- Real-world use cases
- Best practices
- Interview questions
- Multiple-choice questions
- Practical labs

Selecting the appropriate network type is a critical step in designing reliable, secure, and scalable communication infrastructures. In practice, organizations combine several network types to meet business, operational, and security requirements.

---

# 📚 Further Reading

Continue with:

➡ **03-Network-Topologies.md**

Topics include:

- Bus Topology
- Star Topology
- Ring Topology
- Mesh Topology
- Tree Topology
- Hybrid Topology
- Topology comparisons
- Enterprise deployment
- Security considerations

---

⬅️ **Previous:** `01-Computer-Networks.md`  
➡️ **Next:** `03-Network-Topologies.md`
