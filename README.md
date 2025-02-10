# Cybersecurity and Linux System Administration Guide

## Table of Contents
- [Network Fundamentals](#network-fundamentals)
- [Cybersecurity Basics](#cybersecurity-basics)
- [DNS and Network Architecture](#dns-and-network-architecture)
- [Security Frameworks and Concepts](#security-frameworks-and-concepts)
- [Getting Started with Cybersecurity](#getting-started-with-cybersecurity)
- [Essential Linux Commands](#essential-linux-commands)

## Network Fundamentals

### Network Types
- **WAN** (Wide Area Network)
- **MAN** (Metropolitan Area Network)
- **LAN** (Local Area Network)
  - Uses blocks like 192.168.10.10
  - Typically for local networks

Network Hierarchy: WAN contains MAN, which contains LAN

### Key Networking Concepts
- Hub connectivity
- Latency issues
- Browsing performance
- IPv4 (depleted in Asia)
- IPv6 (current standard)

## Cybersecurity Basics

### Historical Timeline
- 1950s: Term "Cyber" originated
- 1990s: "Cyberspace" concept emerged
- 1950s: First computer crimes recorded
- Notable event: Creation of Creeper virus by Mr. BOB

### Components of Cyberspace
1. Information
2. Physical Infrastructure
3. Cognitive Actions
4. People

### CIA Triad
- **Confidentiality**: Preventing information disclosure
- **Integrity**: Maintaining data accuracy
- **Availability**: Ensuring service accessibility

### Notable Security Incidents
- Major breaches: Microsoft, Facebook, LinkedIn, Accenture, Acer
- Apple iCloud breaches
- "Dirty Cow" vulnerability

## DNS and Network Architecture

### DNS Overview
- Created to simplify IP addressing
- Makes name representation easier
- .com was the first TLD (Top Level Domain)

### Attack Types
- SQL injection
- Cross-site scripting
- Remote execution
- Data clipping
- Zero-day attacks (unknown vulnerabilities)

## Security Frameworks and Concepts

### Security Assessment Types
- Vulnerability Assessment
- Penetration Testing
- Security Auditing

### Attack Classifications
- DoS (Denial of Service)
- DGA (Domain Generation Algorithm)
- Ransomware

### Security Measures
1. Preventive
2. Detective
3. Corrective

## Getting Started with Cybersecurity

### Required Skills
- Coding proficiency
- System administration
- Application security
- Networking knowledge

### Career Paths
- Defensive Security
- Offensive Security
- General Security

### Certification Recommendations
- CompTIA certifications
- Starting salary range: 25-50k BDT
- Career progression: Potential for 300k+ BDT after 10 years (defensive security)

## Essential Linux Commands

### File and Directory Operations
```bash
ls -lash         # List files with details
chmod 754 file   # Change file permissions
chown user file  # Change file ownership
touch file       # Create empty file
mkdir dir        # Create directory
cp source dest   # Copy files
mv source dest   # Move files
```

### System Information
```bash
whoami           # Show current user
hostname         # Display system name
pwd              # Print working directory
date             # Show system date/time
```

### Text Processing
```bash
cat file         # Display file contents
grep pattern file # Search for pattern
less file        # View file contents page by page
tail -f file     # Monitor file in real-time
```

### Network Commands
```bash
nmap -sS IP      # Port scanning
ss -plantu       # Socket statistics
systemctl status service # Check service status
```

### File Permissions
- Read (4)
- Write (2)
- Execute (1)
- Total permission = sum of values (e.g., 7 = 4+2+1)

## Additional Resources
- Lab Environment: https://wiki.apnictraining.net/
- Recommended Linux Distributions: Mandriva, SUSE
- Various security tools and frameworks

---
*Note: This guide is compiled from training materials and personal notes. Always verify commands and security practices before implementation in a production environment.*
