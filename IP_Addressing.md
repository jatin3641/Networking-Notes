# 🌍 IP Addressing

> *"Every device connected to a network requires a unique identity. IP addresses provide this identity, enabling devices to locate, identify, and communicate with each other across local and global networks."*

---

# 📖 Table of Contents

- Introduction
- What is an IP Address?
- Why IP Addressing is Important
- Types of IP Addresses
- IPv4 Addressing
- IPv4 Structure
- IPv4 Address Classes
- Public vs Private IP Addresses
- Reserved IP Addresses
- Summary

---

# 📚 Introduction

Every computer, smartphone, server, router, printer, or IoT device connected to a network requires a unique identifier to communicate. This identifier is called an **Internet Protocol (IP) Address**.

An IP address allows devices to send and receive data across networks. Without IP addressing, routers would not know where to forward packets, and communication over the Internet would be impossible.

IP addressing is one of the most fundamental concepts in computer networking. It forms the basis of routing, network segmentation, cloud communication, and cybersecurity.

Whether you're accessing a website, connecting to cloud services, or sending an email, IP addresses are used behind the scenes to deliver information accurately.

---

# 🌍 What is an IP Address?

An **IP Address** is a unique numerical identifier assigned to a device connected to a network.

Its primary purpose is to identify the source and destination of network traffic.

Think of an IP address like a postal address:

- A house address helps a postal service deliver letters.
- An IP address helps routers deliver data packets.

Without unique addresses, communication between devices would not be possible.

---

# 🎯 Functions of an IP Address

An IP address performs several important functions:

### Device Identification

Every network device must have a unique IP address.

Examples:

- Laptop
- Desktop
- Smartphone
- Printer
- Router
- Web Server

---

### Routing

Routers use IP addresses to determine the best path for forwarding packets.

---

### Network Communication

IP addresses enable communication between devices across local and global networks.

---

### Network Management

Administrators use IP addresses to monitor, configure, and troubleshoot devices.

---

# 📦 Types of IP Addresses

There are two major versions of Internet Protocol:

## IPv4

- 32-bit address
- Four decimal octets
- Approximately 4.3 billion unique addresses
- Most widely used today

Example:

```text
192.168.1.10
```

---

## IPv6

- 128-bit address
- Eight hexadecimal groups
- Massive address space
- Designed to replace IPv4

Example:

```text
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

---

# 🏗️ IPv4 Address Structure

An IPv4 address contains **32 bits** divided into **4 octets**.

Each octet contains **8 bits**.

Example:

```text
192.168.10.25
```

Binary representation:

```text
11000000.10101000.00001010.00011001
```

Structure:

```text
+---------+---------+---------+---------+
| Octet 1 | Octet 2 | Octet 3 | Octet 4 |
+---------+---------+---------+---------+
```

Each octet ranges from:

```text
0 - 255
```

---

# 🎯 IPv4 Address Classes

IPv4 originally used classful addressing to organize networks based on size.

---

## Class A

Range:

```text
1.0.0.0 – 126.255.255.255
```

Default Subnet Mask:

```text
255.0.0.0
```

Binary Prefix:

```text
0xxxxxxx
```

Supports:

- Very large organizations
- Internet Service Providers

Example:

```text
10.1.5.25
```

---

## Class B

Range:

```text
128.0.0.0 – 191.255.255.255
```

Default Mask:

```text
255.255.0.0
```

Binary Prefix:

```text
10xxxxxx
```

Commonly used by:

- Universities
- Medium-sized enterprises

Example:

```text
172.20.5.10
```

---

## Class C

Range:

```text
192.0.0.0 – 223.255.255.255
```

Default Mask:

```text
255.255.255.0
```

Binary Prefix:

```text
110xxxxx
```

Commonly used by:

- Homes
- Small offices
- Schools

Example:

```text
192.168.1.15
```

---

## Class D

Purpose:

```text
Multicast Communication
```

Range:

```text
224.0.0.0 – 239.255.255.255
```

Used for:

- Video conferencing
- IPTV
- Streaming

---

## Class E

Reserved for:

- Experimental networking
- Research

Range:

```text
240.0.0.0 – 255.255.255.255
```

---

# 🌐 Public vs Private IP Addresses

## Public IP Address

A public IP address is globally unique and accessible over the Internet.

Characteristics:

- Assigned by Internet Service Providers (ISPs)
- Routable on the Internet
- Required for public-facing services

Example:

```text
203.0.113.25
```

---

## Private IP Address

Private IP addresses are used inside local networks and are not directly routable on the Internet.

Advantages:

- Conserves public IP addresses
- Improves internal network security
- Supports NAT (Network Address Translation)

Private address ranges:

| Range | CIDR |
|--------|------|
| 10.0.0.0 – 10.255.255.255 | /8 |
| 172.16.0.0 – 172.31.255.255 | /12 |
| 192.168.0.0 – 192.168.255.255 | /16 |

---

# 📌 Reserved IPv4 Addresses

Certain IPv4 addresses are reserved for special purposes.

| Address | Purpose |
|----------|---------|
| 127.0.0.1 | Loopback (Localhost) |
| 0.0.0.0 | Default Route / Unknown Address |
| 255.255.255.255 | Limited Broadcast |
| 169.254.x.x | APIPA (Automatic Private IP Addressing) |

---

## 🌍 Real-World Example

Imagine a home network:

```text
               Internet
                   │
           Public IP
                   │
             Home Router
        192.168.1.1
             /   |   \
            /    |    \
Laptop   Phone  Smart TV
192.168.1.10
192.168.1.20
192.168.1.30
```

The router has a **public IP** assigned by the ISP and **private IPs** assigned to devices within the home network.

---

# 🌍 IPv6 Addressing

---

## 📖 Overview

As the Internet rapidly expanded, the limited address space of IPv4 became insufficient to accommodate the growing number of connected devices. To overcome this limitation, the **Internet Engineering Task Force (IETF)** developed **Internet Protocol Version 6 (IPv6)**.

IPv6 is the successor to IPv4 and provides a vastly larger address space while improving routing efficiency, security, and network performance.

Unlike IPv4, IPv6 was designed to support the future growth of the Internet, cloud computing, Internet of Things (IoT), and next-generation networking technologies.

---

# 🎯 Why IPv6 Was Introduced

IPv4 provides approximately:

```
4.3 Billion Addresses
```

While this seemed sufficient decades ago, today's Internet includes:

- Smartphones
- Smart TVs
- IoT Devices
- Cloud Servers
- Smart Cities
- Industrial Automation
- Autonomous Vehicles

IPv6 solves the address exhaustion problem by providing approximately:

```
340 Undecillion Addresses

340,282,366,920,938,463,463,374,607,431,768,211,456
```

---

# 🏗️ IPv6 Address Structure

IPv6 uses **128 bits**, divided into **8 groups**, with each group containing **16 bits** represented in hexadecimal.

Example:

```text
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

Structure:

```text
+--------+--------+--------+--------+
|16 bits |16 bits |16 bits |16 bits |
+--------+--------+--------+--------+
|16 bits |16 bits |16 bits |16 bits |
+--------+--------+--------+--------+
```

Each block is called a **hextet**.

---

# ✂️ IPv6 Address Compression

Long IPv6 addresses can be shortened.

Original:

```text
2001:0db8:0000:0000:0000:ff00:0042:8329
```

Compressed:

```text
2001:db8::ff00:42:8329
```

Rules:

- Remove leading zeros.
- Replace one continuous sequence of all-zero blocks with `::`.
- `::` can be used only once in an address.

---

# 🌐 Types of IPv6 Addresses

### Global Unicast

Public IPv6 addresses used on the Internet.

Example:

```
2001::/16
```

---

### Link-Local

Used only within the local network.

Prefix:

```
FE80::/10
```

Routers do not forward Link-Local addresses.

---

### Unique Local Address (ULA)

Private addressing equivalent to IPv4 private addresses.

Prefix:

```
FC00::/7
```

---

### Multicast

Used to send data to multiple devices.

Prefix:

```
FF00::/8
```

IPv6 does **not** use broadcast addresses.

---

### Anycast

Allows multiple devices to share the same address.

Traffic automatically reaches the nearest device.

Commonly used in:

- DNS Servers
- CDN Networks
- Cloud Infrastructure

---

# 📊 IPv4 vs IPv6 Comparison

| Feature | IPv4 | IPv6 |
|----------|------|------|
| Address Length | 32-bit | 128-bit |
| Address Format | Decimal | Hexadecimal |
| Address Space | 4.3 Billion | 340 Undecillion |
| NAT Required | Yes | No |
| Broadcast | Supported | Not Supported |
| Multicast | Yes | Yes |
| IPSec | Optional | Built-in Support |
| Header Size | Variable | Fixed |
| Configuration | Manual / DHCP | SLAAC / DHCPv6 |

---

# 🎭 Subnet Mask

A **Subnet Mask** identifies which portion of an IP address belongs to the network and which belongs to the host.

Example:

IP Address

```
192.168.1.25
```

Subnet Mask

```
255.255.255.0
```

This means:

```
Network Portion = 192.168.1
Host Portion = 25
```

---

# 🧮 Binary Representation

Decimal:

```
255.255.255.0
```

Binary:

```
11111111.11111111.11111111.00000000
```

The **1s** represent the network bits.

The **0s** represent the host bits.

---

# 🌐 Network ID and Host ID

An IP address consists of two parts:

```
Network ID
```

Identifies the network.

```
Host ID
```

Identifies the device.

Example:

```
IP Address

192.168.10.55

Subnet Mask

255.255.255.0
```

Network ID:

```
192.168.10.0
```

Host ID:

```
55
```

---

# 📏 CIDR (Classless Inter-Domain Routing)

CIDR replaced the older classful addressing system.

Instead of using fixed address classes, CIDR specifies the number of network bits.

Example:

```
192.168.1.0/24
```

The `/24` indicates that:

- 24 bits belong to the network.
- 8 bits belong to hosts.

Common CIDR Prefixes:

| CIDR | Subnet Mask |
|------|--------------|
| /8 | 255.0.0.0 |
| /16 | 255.255.0.0 |
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |
| /29 | 255.255.255.248 |
| /30 | 255.255.255.252 |

---

# 🔢 Binary Conversion

Networking professionals frequently convert decimal values into binary.

Example:

Decimal:

```
192
```

Binary:

```
11000000
```

Another example:

```
168

=

10101000
```

Binary conversion is essential for:

- Subnetting
- CIDR Calculations
- Network Design
- Routing

---

# 🌐 Introduction to Subnetting

Subnetting is the process of dividing a larger network into multiple smaller networks.

Example:

Original Network

```
192.168.1.0/24
```

Can be divided into:

```
192.168.1.0/26

192.168.1.64/26

192.168.1.128/26

192.168.1.192/26
```

Benefits include:

- Better Performance
- Improved Security
- Reduced Broadcast Traffic
- Easier Management
- Efficient IP Utilization

---

# 📊 Example Subnet

```
Network

192.168.1.0/24

Hosts

254
```

Divide into:

```
192.168.1.0/25

Hosts

126

+

192.168.1.128/25

Hosts

126
```

---

# 🌐 Network Address Translation (NAT)

---

## 📖 Overview

Network Address Translation (NAT) is a technique used by routers and firewalls to translate private IP addresses into public IP addresses, allowing devices within a private network to communicate with the Internet.

Since IPv4 provides a limited number of public IP addresses, NAT enables multiple devices to share a single public IP address.

NAT has become a standard feature in home routers, enterprise gateways, and cloud environments.

---

## 🎯 Why NAT is Required

Without NAT:

- Every device would require a unique public IP address.
- IPv4 addresses would be exhausted much faster.
- Internal networks would be directly exposed to the Internet.

With NAT:

- Multiple devices share one public IP.
- Internal addresses remain hidden.
- Better utilization of IPv4 addresses.

---

## 🏗️ NAT Working Process

```text
          Internet
              │
      Public IP
       203.0.113.10
              │
        ┌──────────┐
        │  Router  │
        │   NAT    │
        └──────────┘
      /      |      \
     /       |       \
192.168.1.10
192.168.1.20
192.168.1.30
```

The router replaces private IP addresses with its public IP before forwarding packets to the Internet.

---

## Types of NAT

### Static NAT

One private IP maps permanently to one public IP.

Example:

```
192.168.1.10

↓

203.0.113.10
```

Used for:

- Web Servers
- Mail Servers
- Public Services

---

### Dynamic NAT

Maps private addresses to a pool of available public addresses.

Advantages:

- Better address utilization
- Suitable for medium-sized organizations

---

### PAT (Port Address Translation)

Also called **NAT Overload**.

Many private devices share one public IP by using different port numbers.

Example:

```
192.168.1.10:5000

↓

203.0.113.10:40001
```

PAT is the most common NAT implementation in home and enterprise networks.

---

# 🌍 DHCP (Dynamic Host Configuration Protocol)

---

## 📖 Overview

DHCP automatically assigns network configuration information to devices when they connect to a network.

Instead of manually configuring every device, administrators deploy DHCP servers to distribute:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server
- Lease Time

---

## DHCP Process (DORA)

The DHCP communication process consists of four steps:

```text
Client                   DHCP Server

Discover  ------------->

           <------------- Offer

Request   ------------->

           <------------- Acknowledge
```

### D – Discover

The client broadcasts a request for an IP address.

### O – Offer

The DHCP server offers an available IP address.

### R – Request

The client requests the offered address.

### A – Acknowledge

The server confirms the lease.

---

## Advantages of DHCP

- Automatic IP assignment
- Reduces configuration errors
- Simplifies administration
- Centralized management
- Efficient address allocation

---

# 🌍 DNS (Domain Name System)

---

## 📖 Overview

Humans prefer domain names such as:

```
www.github.com
```

Computers communicate using IP addresses.

DNS translates human-readable domain names into IP addresses.

---

## DNS Resolution Process

```text
User
 │
 ▼
DNS Resolver
 │
 ▼
Root Server
 │
 ▼
TLD Server (.com)
 │
 ▼
Authoritative DNS
 │
 ▼
IP Address Returned
```

Example:

```
github.com

↓

140.82.121.4
```

---

## Common DNS Record Types

| Record | Purpose |
|---------|----------|
| A | IPv4 Address |
| AAAA | IPv6 Address |
| MX | Mail Server |
| CNAME | Alias |
| NS | Name Server |
| TXT | Text Information |

---

# 🌍 APIPA (Automatic Private IP Addressing)

When a DHCP server is unavailable, Windows automatically assigns an address from:

```
169.254.0.0/16
```

Example:

```
169.254.45.12
```

APIPA allows communication within the local network but **does not provide Internet connectivity**.

---

# 🌍 Default Gateway

A Default Gateway is the router that forwards traffic from the local network to other networks.

Example:

```
PC

192.168.1.25

↓

Gateway

192.168.1.1

↓

Internet
```

Without a configured gateway, devices can communicate only with hosts on the same local network.

---

# 🔍 IP Troubleshooting Commands

### Windows

```cmd
ipconfig
```

Displays:

- IP Address
- Subnet Mask
- Default Gateway

---

### Linux

```bash
ip addr
```

Displays network interfaces and assigned addresses.

---

### Ping

```bash
ping google.com
```

Tests connectivity.

---

### Traceroute

Linux

```bash
traceroute google.com
```

Windows

```cmd
tracert google.com
```

Displays routing path.

---

### Nslookup

```bash
nslookup github.com
```

Queries DNS servers.

---

### ARP

```bash
arp -a
```

Displays the ARP cache.

---

# 🔐 Cybersecurity Perspective

IP addressing plays a crucial role in network security.

Common attacks include:

- IP Spoofing
- ARP Spoofing
- DHCP Starvation
- Rogue DHCP Servers
- DNS Spoofing
- DNS Cache Poisoning
- Man-in-the-Middle (MITM)

---

## Security Best Practices

- Enable DHCP Snooping
- Use Dynamic ARP Inspection (DAI)
- Configure Access Control Lists (ACLs)
- Deploy DNS Security Extensions (DNSSEC)
- Implement Network Segmentation
- Enable Firewalls
- Monitor IP Address Usage
- Use Secure VPNs

---

# 🌍 Real-World Example

Consider a user connecting a laptop to a home Wi-Fi network.

1. The laptop requests an IP address.
2. The router's DHCP server assigns:
   - IP Address
   - Subnet Mask
   - Default Gateway
   - DNS Server
3. The user opens a web browser.
4. DNS resolves the website name.
5. NAT translates the private IP to the router's public IP.
6. The packet travels across the Internet.
7. The website responds, and the browser displays the content.

This entire process occurs automatically within seconds.

---

# 💼 Interview Questions

## Beginner

1. What is an IP address?
2. What is the difference between IPv4 and IPv6?
3. What is a subnet mask?
4. What is NAT?
5. What is DHCP?

---

## Intermediate

6. Explain the DORA process.
7. What is the purpose of DNS?
8. What is APIPA?
9. Explain CIDR notation.
10. What is the difference between Public and Private IP addresses?

---

## Advanced

11. Explain PAT.
12. How does NAT improve IPv4 address utilization?
13. What are the security risks associated with DHCP?
14. Compare Static NAT and Dynamic NAT.
15. Explain DNS cache poisoning.

---

# 📝 Multiple Choice Questions (MCQs)

### Question 1

Which protocol automatically assigns IP addresses?

- A. DNS
- B. DHCP
- C. FTP
- D. SMTP

**Answer:** B

---

### Question 2

Which address range is reserved for APIPA?

- A. 10.0.0.0/8
- B. 169.254.0.0/16
- C. 192.168.0.0/16
- D. 172.16.0.0/12

**Answer:** B

---

### Question 3

Which DNS record maps a hostname to an IPv4 address?

- A. MX
- B. AAAA
- C. A
- D. TXT

**Answer:** C

---

### Question 4

What does NAT primarily accomplish?

- A. Encrypts data
- B. Translates IP addresses
- C. Compresses packets
- D. Filters spam

**Answer:** B

---

### Question 5

Which protocol translates domain names into IP addresses?

- A. DHCP
- B. FTP
- C. DNS
- D. SNMP

**Answer:** C

---

# 🧪 Practical Labs

## Lab 1 – View Network Configuration

Windows

```cmd
ipconfig /all
```

Linux

```bash
ip addr
```

Observe:

- IP Address
- Subnet Mask
- Gateway
- DNS Server

---

## Lab 2 – Test Connectivity

```bash
ping 8.8.8.8
```

Compare results with:

```bash
ping google.com
```

Discuss why one might succeed while the other fails.

---

## Lab 3 – DNS Lookup

```bash
nslookup github.com
```

Record:

- IPv4 Address
- IPv6 Address (if available)

---

## Lab 4 – Trace Route

```bash
traceroute github.com
```

Identify the network hops between your computer and the destination.

---

## Lab 5 – NAT Observation

Using a home router:

- Note the private IP of your device.
- Visit a site that displays your public IP.
- Compare the two addresses and explain how NAT is working.

---

# 📚 Chapter Summary

In this chapter, we explored the fundamentals of IP addressing and the technologies that enable devices to communicate across networks.

We covered:

- IPv4 and IPv6
- Public and Private IP addresses
- Address classes
- Subnet masks
- CIDR notation
- Network ID and Host ID
- Binary conversion
- Subnetting basics
- NAT and PAT
- DHCP and the DORA process
- DNS and name resolution
- APIPA and Default Gateway
- IP troubleshooting tools
- Security threats and best practices
- Practical labs and review questions

Understanding IP addressing is essential for network design, routing, troubleshooting, and cybersecurity. It provides the foundation for advanced topics such as routing protocols, VLANs, cloud networking, and enterprise network management.

---

# 📚 Further Reading

Continue to the next chapter:

➡ **07-Network-Devices.md**

Topics include:

- Hub
- Switch
- Bridge
- Router
- Modem
- Access Point
- Repeater
- Firewall
- IDS
- IPS
- Network Interface Card (NIC)
- Load Balancer
- Proxy Server
- Enterprise networking devices

---

⬅️ **Previous:** `TCP-IP-Model.md`  
➡️ **Next:** `Network-Devices.md`


- Binary Conversion
- Introduction to Subnetting
