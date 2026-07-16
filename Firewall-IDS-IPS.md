# 🔥 Firewalls, Intrusion Detection Systems (IDS), and Intrusion Prevention Systems (IPS)

> *"Modern computer networks face millions of cyber threats every day. Firewalls, Intrusion Detection Systems (IDS), and Intrusion Prevention Systems (IPS) form the first line of defense by monitoring, filtering, detecting, and preventing malicious network activities."*

---

# 📖 Table of Contents

- Introduction
- Network Security Overview
- What is a Firewall?
- Why Firewalls are Important
- Firewall Architecture
- Types of Firewalls
- Packet Filtering Firewall
- Stateful Inspection Firewall
- Proxy Firewall
- Next Generation Firewall (NGFW)
- Firewall Rule Processing
- Summary

---

# 📚 Introduction

As organizations become increasingly dependent on digital infrastructure, protecting computer networks has become one of the highest priorities in information security.

Cybercriminals continuously attempt to exploit vulnerabilities through malware, ransomware, phishing campaigns, denial-of-service attacks, unauthorized access, and data theft.

To defend against these threats, organizations deploy multiple security technologies. Among the most important are:

- Firewalls
- Intrusion Detection Systems (IDS)
- Intrusion Prevention Systems (IPS)

These technologies work together to monitor network traffic, enforce security policies, detect suspicious behavior, and prevent attacks before they reach critical systems.

This chapter explores how these technologies operate, their architecture, deployment models, strengths, limitations, and real-world use cases.

---

# 🌍 Network Security Overview

Modern enterprise networks are protected using a layered security approach known as **Defense in Depth**.

Instead of relying on a single security device, organizations deploy multiple layers of protection.

Example:

```text
                 Internet
                     │
              Edge Router
                     │
              Next-Gen Firewall
                     │
               IDS / IPS Sensor
                     │
             Core Network Switch
                     │
        ┌────────────┼────────────┐
        │            │            │
   User VLAN     Server VLAN   Guest VLAN
```

Each device contributes to protecting the network by filtering traffic, monitoring activity, or blocking attacks.

---

# 🔥 What is a Firewall?

A **Firewall** is a hardware device, software application, or cloud-based service that monitors and controls incoming and outgoing network traffic according to predefined security rules.

Its primary objective is to prevent unauthorized access while allowing legitimate communication.

A firewall acts as a gatekeeper, examining traffic before it reaches internal systems.

---

# 🎯 Why Firewalls Are Important

Firewalls help organizations:

- Prevent unauthorized access
- Restrict unnecessary services
- Block malicious traffic
- Protect internal resources
- Monitor network activity
- Enforce organizational security policies
- Reduce the attack surface

Without firewalls, internal systems would be directly exposed to Internet-based threats.

---

# 🏗️ Firewall Architecture

```text
                Internet
                    │
         ┌────────────────────┐
         │    Firewall        │
         └────────────────────┘
            │              │
        DMZ Network    Internal LAN
            │              │
      Web Server      Employees
      Mail Server     File Server
```

---

# 📌 Firewall Components

A modern firewall consists of several logical components.

## Rule Engine

Processes firewall rules and determines whether traffic is allowed or denied.

---

## Packet Inspection Engine

Analyzes incoming and outgoing packets.

---

## Logging System

Records connection attempts, blocked traffic, and policy violations.

---

## NAT Engine

Performs Network Address Translation.

---

## VPN Module

Provides encrypted remote access for users.

---

## Management Console

Allows administrators to configure and monitor firewall policies.

---

# 🛡️ Types of Firewalls

Firewalls have evolved significantly over the years.

The major types include:

- Packet Filtering Firewall
- Stateful Inspection Firewall
- Circuit-Level Gateway
- Proxy Firewall
- Next Generation Firewall (NGFW)

---

# 📦 Packet Filtering Firewall

## Overview

Packet filtering is the oldest firewall technology.

It examines only the packet headers and decides whether to allow or deny traffic based on predefined rules.

The firewall evaluates information such as:

- Source IP Address
- Destination IP Address
- Source Port
- Destination Port
- Protocol (TCP/UDP/ICMP)

---

## Decision Process

```text
Incoming Packet
        │
        ▼
Read Header
        │
        ▼
Compare With Rules
        │
   ┌────┴────┐
Allow     Deny
```

---

## Advantages

- Fast processing
- Low resource usage
- Easy to configure
- Suitable for simple networks

---

## Disadvantages

- No payload inspection
- Cannot detect application attacks
- Vulnerable to spoofing
- Limited security visibility

---

## Real-World Example

Allow HTTPS traffic while blocking Telnet.

```text
ALLOW TCP Port 443

DENY TCP Port 23
```

---

# 🔄 Stateful Inspection Firewall

## Overview

Stateful firewalls maintain a **State Table** containing information about active connections.

Instead of inspecting every packet independently, the firewall verifies whether packets belong to an established session.

---

## Connection Tracking

```text
Client
   │
 SYN
   │
Firewall
   │
Connection Table
   │
Server
```

The firewall stores:

- Source IP
- Destination IP
- Port Numbers
- Connection State
- Session Timeout

---

## Advantages

- Better security
- Tracks active sessions
- Blocks unsolicited traffic
- Reduces spoofing attacks

---

## Disadvantages

- Higher memory usage
- More processing overhead
- Larger attack surface than packet filtering

---

# 🌐 Proxy Firewall

## Overview

A Proxy Firewall acts as an intermediary between internal users and external servers.

Clients never communicate directly with Internet servers.

Instead:

Client

↓

Proxy Firewall

↓

Internet

This hides internal network details and provides additional inspection capabilities.

---

## Advantages

- High security
- User anonymity
- Content filtering
- Malware protection
- Caching

---

## Disadvantages

- Higher latency
- More resource intensive
- Complex configuration

---

## Common Applications

- Corporate Web Filtering
- Secure Internet Browsing
- Email Security Gateways

---

# 🚀 Next Generation Firewall (NGFW)

## Overview

A **Next Generation Firewall (NGFW)** combines traditional firewall capabilities with advanced security features.

Unlike older firewalls, NGFWs inspect not only packet headers but also application traffic and encrypted sessions.

---

## Features

- Deep Packet Inspection (DPI)
- Application Awareness
- Intrusion Prevention
- Malware Detection
- SSL/TLS Inspection
- URL Filtering
- User Identity Awareness
- Threat Intelligence Integration

---

## Enterprise Architecture

```text
              Internet
                  │
           Next-Gen Firewall
          ┌───────┼────────┐
          │       │        │
      Web Filter IPS     VPN
          │       │        │
      Internal Network
```

---

## Advantages

- Excellent visibility
- Advanced threat detection
- Centralized management
- Supports Zero Trust Architecture
- Application-level security

---

## Disadvantages

- Expensive
- Requires skilled administrators
- Increased processing requirements

---

# 📋 Firewall Rule Processing

Firewalls evaluate rules from top to bottom.

Example:

```text
Rule 1

ALLOW HTTPS

↓

Rule 2

ALLOW DNS

↓

Rule 3

ALLOW SSH

↓

Rule 4

DENY ALL
```

Once a packet matches a rule, processing stops.

For this reason, rule order is extremely important.

---

# 🚨 Intrusion Detection System (IDS)

---

## 📖 Overview

An **Intrusion Detection System (IDS)** is a security solution that continuously monitors network traffic, system logs, and user activities to identify suspicious behavior, malicious attacks, or policy violations.

Unlike a firewall, which primarily controls traffic flow, an IDS focuses on **detecting** threats that have bypassed other security controls.

When suspicious activity is detected, the IDS generates alerts, logs the event, and provides valuable information for security analysts. However, it does **not** automatically block malicious traffic.

IDS solutions are widely used in Security Operations Centers (SOCs), enterprise networks, cloud environments, and critical infrastructure.

---

# 🎯 Objectives of IDS

The primary goals of an IDS include:

- Detect cyberattacks
- Monitor network traffic
- Identify policy violations
- Generate security alerts
- Assist incident response
- Collect forensic evidence
- Improve network visibility

---

# 🏗️ IDS Architecture

```text
               Internet
                   │
            Next Generation Firewall
                   │
             ┌──────────────┐
             │     IDS      │
             └──────────────┘
                   │
             Core Network Switch
             /       |        \
          Users   Servers   Database
```

The IDS receives a copy of network traffic and analyzes it without interrupting communication.

---

# 📡 Types of IDS

## 1️⃣ Network Intrusion Detection System (NIDS)

A **Network IDS** monitors packets traveling across the network.

Deployment Locations:

- Core Switch
- Data Center
- Internet Gateway
- DMZ
- Cloud Networks

Examples:

- Snort
- Suricata
- Zeek (Bro)

### Advantages

- Monitors entire network
- Detects external attacks
- Centralized monitoring
- High visibility

### Limitations

- Cannot inspect encrypted traffic without decryption
- Large networks generate high volumes of alerts

---

## 2️⃣ Host Intrusion Detection System (HIDS)

A **Host IDS** runs directly on an individual computer or server.

It monitors:

- System Logs
- File Integrity
- Running Processes
- Registry Changes
- User Activity

Examples:

- Wazuh
- OSSEC
- Tripwire

### Advantages

- Detailed host visibility
- Detects insider threats
- File integrity monitoring
- Detects privilege escalation

### Limitations

- Protects only the installed device
- Higher management overhead

---

# 🔍 IDS Detection Techniques

Modern IDS solutions use multiple detection methods.

---

## Signature-Based Detection

Signature-based IDS compares traffic against a database of known attack patterns.

Example:

Known SQL Injection Pattern

↓

IDS Signature Match

↓

Alert Generated

### Advantages

- Fast detection
- Accurate for known threats
- Low false positives

### Disadvantages

- Cannot detect unknown attacks
- Requires frequent signature updates

---

## Anomaly-Based Detection

Instead of looking for known signatures, anomaly detection establishes a baseline of normal network behavior.

If activity deviates significantly from the baseline, an alert is generated.

Example:

Normal Login Attempts:

5 per hour

↓

Observed Login Attempts:

500 per minute

↓

Alert Generated

### Advantages

- Detects Zero-Day attacks
- Identifies insider threats
- Detects unusual behavior

### Disadvantages

- Higher false positives
- Requires training period

---

## Behavior-Based Detection

Behavior-based systems monitor long-term activity patterns.

Examples include:

- Abnormal file access
- Suspicious process creation
- Unusual network communication
- Unauthorized privilege escalation

---

# 📊 Detection Technique Comparison

| Feature | Signature | Anomaly | Behavior |
|----------|-----------|----------|-----------|
| Detects Known Threats | ✅ | ⚠️ | ⚠️ |
| Detects Unknown Threats | ❌ | ✅ | ✅ |
| False Positives | Low | Higher | Moderate |
| Learning Required | No | Yes | Yes |
| Performance | Fast | Moderate | Moderate |

---

# 🛡️ Intrusion Prevention System (IPS)

---

## 📖 Overview

An **Intrusion Prevention System (IPS)** extends IDS functionality by actively preventing attacks.

Unlike IDS, which only monitors traffic, IPS sits **inline** with network communication and can automatically block malicious activity.

An IPS examines every packet before it reaches the destination.

If malicious traffic is detected, the IPS can:

- Drop packets
- Reset connections
- Block IP addresses
- Update firewall rules
- Generate alerts

---

# 🏗️ IPS Architecture

```text
              Internet
                  │
             Next-Gen Firewall
                  │
             ┌────────────┐
             │    IPS     │
             └────────────┘
                  │
             Internal Network
```

Unlike IDS, IPS becomes part of the communication path.

---

# 📡 Types of IPS

## Network IPS (NIPS)

Protects the entire network.

Deployment:

- Internet Gateway
- Data Center
- Core Network

---

## Host IPS (HIPS)

Installed directly on endpoints.

Protects:

- Workstations
- Servers
- Virtual Machines

---

## Wireless IPS (WIPS)

Monitors wireless networks.

Detects:

- Rogue Access Points
- Evil Twin Attacks
- Deauthentication Attacks

---

## Network Behavior Analysis (NBA)

Focuses on:

- DDoS Attacks
- Worm Propagation
- Network Scanning
- Botnet Activity

---

# ⚙️ IPS Decision Process

```text
Incoming Packet
       │
       ▼
Packet Inspection
       │
       ▼
Threat Analysis
       │
 ┌─────┴─────┐
 │           │
Safe      Malicious
 │           │
 ▼           ▼
Allow      Block
```

---

# 🚨 Common Attacks Detected

IDS and IPS can detect a wide range of attacks, including:

### Network Attacks

- Port Scanning
- SYN Flood
- UDP Flood
- ICMP Flood
- ARP Spoofing

---

### Web Attacks

- SQL Injection
- Cross-Site Scripting (XSS)
- Directory Traversal
- Remote Code Execution

---

### Malware

- Ransomware
- Worms
- Trojans
- Botnets

---

### Authentication Attacks

- Brute Force
- Credential Stuffing
- Password Spraying

---

# 🌍 Enterprise Deployment Example

```text
                    Internet
                        │
                  Edge Router
                        │
             Next Generation Firewall
                        │
                  Network IPS
                        │
                Core Switch Stack
             ┌────────┼────────┐
             │        │        │
         User VLAN Server VLAN Guest VLAN
             │        │        │
           HIDS     HIDS     Wireless IPS
```

This layered architecture ensures multiple levels of visibility and protection.

---

# 🔐 Best Practices

For effective IDS/IPS deployment:

- Keep signatures updated.
- Regularly tune detection rules.
- Monitor alerts continuously.
- Integrate with SIEM platforms.
- Encrypt sensitive traffic.
- Perform routine threat hunting.
- Reduce false positives through policy tuning.
- Test detection capabilities using simulated attacks.

---
# 📊 Firewall vs IDS vs IPS

Understanding the differences between Firewalls, Intrusion Detection Systems (IDS), and Intrusion Prevention Systems (IPS) is essential for designing a secure network architecture.

Although these technologies often work together, they perform different security functions.

| Feature | Firewall | IDS | IPS |
|----------|----------|-----|-----|
| Primary Function | Controls network traffic | Detects malicious activity | Detects and blocks malicious activity |
| Blocks Attacks | ✅ Yes | ❌ No | ✅ Yes |
| Generates Alerts | ⚠️ Limited | ✅ Yes | ✅ Yes |
| Deployment | Network Edge / Internal | Passive Monitoring | Inline with Traffic |
| Traffic Inspection | Packet, Session, Application | Packet and Behavior Analysis | Packet and Behavior Analysis |
| Performance Impact | Moderate | Low | Moderate to High |
| Typical Use | Access Control | Threat Detection | Threat Prevention |

---

# 🏢 Defense in Depth

## 📖 Overview

**Defense in Depth** is a cybersecurity strategy that uses multiple layers of security controls rather than relying on a single protection mechanism.

If one layer fails, additional layers continue to protect the organization.

---

## Enterprise Security Architecture

```text
                    Internet
                        │
                  Edge Router
                        │
              Next Generation Firewall
                        │
                  Intrusion Prevention
                        │
                 Core Layer Switch
               ┌────────┼────────┐
               │        │        │
         User VLAN  Server VLAN  DMZ
               │        │        │
             HIDS      HIDS   Web Server
               │        │        │
             SIEM Monitoring Platform
```

Each security component provides a different level of protection.

---

# 🌐 Demilitarized Zone (DMZ)

## 📖 What is a DMZ?

A **Demilitarized Zone (DMZ)** is a separate network segment that hosts public-facing services while isolating the internal network.

Servers commonly placed in a DMZ include:

- Web Servers
- Mail Servers
- DNS Servers
- Reverse Proxies

---

## DMZ Architecture

```text
                Internet
                    │
            External Firewall
                    │
                 DMZ Network
          ┌─────────┼─────────┐
          │         │         │
      Web Server Mail Server DNS Server
                    │
            Internal Firewall
                    │
            Corporate Network
```

Benefits:

- Isolates public services
- Reduces attack surface
- Protects internal resources
- Supports layered security

---

# 📜 Example Firewall Rules

Firewall rules determine how traffic is processed.

### Allow HTTPS

```text
ALLOW TCP FROM ANY TO WEB_SERVER PORT 443
```

---

### Allow DNS

```text
ALLOW UDP FROM INTERNAL TO DNS_SERVER PORT 53
```

---

### Allow SSH from Admin Network

```text
ALLOW TCP FROM 192.168.10.0/24 TO FIREWALL PORT 22
```

---

### Block Telnet

```text
DENY TCP FROM ANY TO ANY PORT 23
```

---

### Default Rule

```text
DENY ALL
```

A **default deny** policy ensures that any traffic not explicitly permitted is automatically blocked.

---

# 🚨 Real-World Attack Scenarios

## Scenario 1 — Port Scanning

**Attack:**

An attacker scans a server using Nmap.

**Detection:**

- IDS identifies repeated connection attempts.
- IPS blocks the attacker's IP after detecting suspicious behavior.

---

## Scenario 2 — SQL Injection

**Attack:**

Malicious SQL commands are sent through a web application's login form.

**Detection:**

- NGFW detects unusual application-layer traffic.
- IPS blocks the request.
- SIEM records the event for investigation.

---

## Scenario 3 — SYN Flood

**Attack:**

An attacker sends thousands of TCP SYN packets to exhaust server resources.

**Protection:**

- Firewall rate limits connections.
- IPS detects abnormal traffic patterns.
- Server remains available to legitimate users.

---

## Scenario 4 — Malware Download

**Attack:**

A user attempts to download a malicious executable.

**Protection:**

- Proxy firewall blocks access to known malicious domains.
- IPS detects malware signatures.
- Endpoint protection quarantines the file.

---

# 🔐 Security Best Practices

To build a secure enterprise network:

- Follow the Principle of Least Privilege.
- Enable logging on all security devices.
- Review firewall rules regularly.
- Keep IDS/IPS signatures updated.
- Segment networks using VLANs.
- Secure the DMZ.
- Enable Multi-Factor Authentication (MFA).
- Perform regular vulnerability assessments.
- Conduct penetration testing.
- Integrate IDS/IPS with a SIEM solution.

---

# 🌍 Enterprise Security Workflow

```text
Incoming Traffic
        │
        ▼
Firewall
        │
        ▼
IPS Inspection
        │
        ▼
IDS Monitoring
        │
        ▼
Internal Network
        │
        ▼
SIEM Logging & Alerting
```

This layered workflow improves visibility, detection, and response capabilities.

---

# 💼 Interview Questions

## Beginner

1. What is a firewall?
2. What is the difference between IDS and IPS?
3. What is a DMZ?
4. What is packet filtering?
5. Why are firewalls important?

---

## Intermediate

6. Explain stateful inspection.
7. What is Deep Packet Inspection (DPI)?
8. Compare Host IDS and Network IDS.
9. What is an NGFW?
10. Explain signature-based detection.

---

## Advanced

11. Design a secure enterprise network using Firewall, IDS, and IPS.
12. Explain how IPS blocks attacks.
13. What are the limitations of anomaly-based detection?
14. Describe how SIEM integrates with IDS/IPS.
15. Explain the Defense in Depth strategy.

---

# 📝 Multiple Choice Questions (MCQs)

### Question 1

Which device actively blocks malicious traffic?

- A. IDS
- B. Hub
- C. IPS
- D. Bridge

**Answer:** C

---

### Question 2

Which firewall type maintains a connection table?

- A. Packet Filtering Firewall
- B. Stateful Firewall
- C. Proxy Firewall
- D. NGFW

**Answer:** B

---

### Question 3

Which detection method is best at identifying unknown attacks?

- A. Signature-Based
- B. Port-Based
- C. Anomaly-Based
- D. Rule-Based

**Answer:** C

---

### Question 4

Which network segment is commonly used for public-facing servers?

- A. VLAN
- B. LAN
- C. DMZ
- D. WAN

**Answer:** C

---

### Question 5

What is the default best practice for firewall policies?

- A. Allow All
- B. Deny All
- C. Permit Internal Only
- D. Disable Logging

**Answer:** B

---

# 🧪 Practical Labs

## Lab 1 — Firewall Rule Simulation

**Objective:**

Create basic firewall rules.

Tasks:

- Allow HTTP (Port 80)
- Allow HTTPS (Port 443)
- Block Telnet (Port 23)
- Verify traffic using packet simulation

---

## Lab 2 — IDS Monitoring with Snort

**Tools:**

- Snort
- Kali Linux
- Ubuntu

Tasks:

- Install Snort
- Start IDS mode
- Generate network traffic
- Observe alerts

---

## Lab 3 — IPS Simulation

**Tools:**

- Suricata

Tasks:

- Configure IPS mode
- Generate a port scan using Nmap
- Verify that malicious traffic is blocked

---

## Lab 4 — Wireshark Packet Analysis

Capture network traffic and identify:

- TCP Three-Way Handshake
- DNS Queries
- HTTP Requests
- HTTPS Sessions
- ICMP Packets

---

## Lab 5 — Enterprise Security Design

Design a network containing:

- Internet
- Router
- Next Generation Firewall
- DMZ
- IDS
- IPS
- Core Switch
- VLANs
- Internal Servers
- Wireless Access Points

Document the purpose of each device and explain how traffic flows through the environment.

---

# 📚 Chapter Summary

This chapter explored the essential technologies used to protect modern computer networks.

Topics covered include:

- Firewall fundamentals
- Firewall architectures
- Packet Filtering Firewalls
- Stateful Firewalls
- Proxy Firewalls
- Next Generation Firewalls (NGFW)
- Intrusion Detection Systems (IDS)
- Intrusion Prevention Systems (IPS)
- Detection techniques
- Defense in Depth
- DMZ architecture
- Firewall rule processing
- Enterprise deployment
- Security best practices
- Practical labs
- Interview questions
- MCQs

Firewalls, IDS, and IPS complement one another rather than replacing one another. A firewall controls traffic, an IDS identifies suspicious activity, and an IPS actively prevents malicious traffic. Together, they form a layered security architecture that helps organizations defend against a wide range of cyber threats.

---

# 📚 Further Reading

Continue to the next chapter:

➡ **09-Network-Security.md**

Topics include:

- CIA Triad
- Authentication, Authorization, and Accounting (AAA)
- Cryptography
- VPN Technologies
- VLAN Security
- Zero Trust Architecture
- Network Segmentation
- Malware
- Phishing
- DoS & DDoS
- Man-in-the-Middle (MITM)
- ARP & DNS Spoofing
- Wireless Security
- Security Hardening
- SIEM & SOC
- Incident Response
- Best Practices

---

⬅️ **Previous:** `Network-Devices.md`  
➡️ **Next:** `Network-Security.md`


- Deployment architecture
- Real-world attack detection
