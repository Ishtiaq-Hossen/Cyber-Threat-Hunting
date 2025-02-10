# Threat Hunting & Cyber Security Overview
## Table of Contents
- [Day 1 Note](#day-1-note)
- [Day 2 Note](#starting-from-10-02-2023)

# Day 1 Note
## Historic Overview of Threat Hunting

### References & Resources
- **Movie**: *Doctor Strange* (WW2) – Needs review
- **Book**: *Sanju: The Art of War*

## Agenda
1. **Concepts of Networking**
2. **DNS Ecosystem**
3. **Cyber Security**
4. **Threat Analytics & Hunting**

> "Don't believe everything you read on the Internet."  
> — Abraham Lincoln  

---

## Networking Basics
- **WAN (Wide Area Network)** → Encompasses MAN
- **MAN (Metropolitan Area Network)** → Encompasses LAN
- **LAN (Local Area Network)** → Uses private IP blocks like 192.168.x.x
- **IPv4** → Running out of addresses in Asia
- **IPv6** → The future of networking

**Key Concepts:** Hub, Latency, Browsing Speed

---

## Cyber Origins & Evolution
- **Cyber (1950s)** → Initial concept
- **Cyberspace (1990s)** → Interconnection of digital devices
- **Components of Cyberspace:**
  - Information
  - Physical
  - Cognitive Actions
  - People

### Cybercrime Evolution
- **War is a collective form of crime**
- **Cybercrime Emerged (1950s)** → Mr. Bob created "Creeper"; Rev unintentionally developed the first virus

---

## DNS & Its Importance
- **DNS simplifies IP representation** → Making domain names more user-friendly
- **.com was the first TLD (Top-Level Domain)**
- **DNS Tunneling** → Used for covert data transmission

---

## Cyber Security Evolution
- **Became a business model & political issue (1990s)**
- **Major Cyber Attacks:**
  - SQL Injection
  - Cross-Site Scripting (XSS)
  - Remote Attacks
  - Zero-Day Exploits
  - Apple iCloud Breach
- **Notable Security Incidents:**
  - "Dirty COW" exploit
  - Facebook, LinkedIn, Accenture breaches

**Quote:** _"Security is a myth. Once you're online, you're not secure."_

### Cyber Security Pillars (CIA Triad)
1. **Confidentiality (C)** → Prevent unauthorized access
2. **Integrity (I)** → Ensure data accuracy and trustworthiness
3. **Availability (A)** → Ensure service availability for clients

---

## Cyber Attacks & Prevention
- **DDoS Attack**: Overloading bandwidth to disrupt services
- **Risk Assessment Analogy:** The need for cybersecurity awareness increases after a cyber attack
- **Penetration Testing:**
  - Vulnerability Assessment
  - Exploit Execution
  - Post-Service Testing

---

## Cyber Security Framework
- **White Hat Hackers** → Ethical hacking & security testing
- **Offensive vs. Defensive Security**:
  - **Bug Bounty** → Part of offensive security
  - **Defensive Security** → Focused on mitigation & prevention

### Cybersecurity Mitigation Strategies
- **Preventive** → Reduce risks beforehand
- **Detective** → Identify threats in real-time
- **Corrective** → Fix vulnerabilities post-attack

---

## Cyber Security Learning Path
1. **Foundations:** Coding, Systems, Applications, Networking
2. **Certifications:** CompTIA, CEH, CISSP
3. **Practical Experience:** Lab exercises, real-world testing

**Linux Basics for Cyber Security:**
- Linux is highly case-sensitive
- **Essential Commands:**
  - `ls -lah` → List files with details
  - `chmod` → Modify file permissions
  - `chown` → Change file ownership
  - `sudo` → Execute admin commands
  - `nano`, `vim` → Text editors
  - `man` → Command manuals
  - `grep`, `cat`, `tail`, `more` → File handling

---

## Advanced Cyber Security Topics
- **Penetration Testing Lifecycle**
- **Security Tools & Measures:**
  - `nmap` → Network scanning
  - `lsof` → List open files
  - `netstat`, `ss` → Network status
- **Attack Techniques:**
  - DGA (Domain Generation Algorithm)
  - Zero-Input Validation

---

## Final Thoughts
- **Continuous Learning is Key** → Cyber threats evolve daily
- **Cybersecurity is not just offensive; it includes defense & risk management**
- **Security Awareness Matters!**

---

📌 **Lab Resources:** [APNIC Training Wiki](https://wiki.apnictraining.net/)




# Day 2 Note



# Threat Hunting and DNS Overview

# Starting from 10-02-2023

### DNS Overview
The **Domain Name System (DNS)** translates domain names into IP addresses, making internet navigation easier.
- **Example:** `iub.edu.bd` resolves to its corresponding IP address.
- **Internet Flow:** [Upstream → IAG → ISP]
- Most upstream connections in Bangladesh route through **Singapore**, leading to **lower latency** due to proximity.

### DNS Basics
- The home router serves as a **recursive DNS server**.
- Accessing `iub.edu.bd` requires resolving its IP address.
- **Caching:** Stores data temporarily for faster retrieval.
- **Root DNS Servers:** The world has **13 root DNS servers**.
- **TLD & ccTLD:** Manage top-level and country-specific domains.
- Before DNS, `robots.txt` maintained all IP mappings.

### Notable Events
- **2021 Akamai Outage:** A major CDN provider failure disrupted global access.
- **BGP (Border Gateway Protocol):** Essential for inter-data center connectivity; disabling BGP can bring networks down.
- **IUB's DNS Server:** Hosts one DNS server internally.

### DNS and Security
- **Google DNS Server:** `8.8.8.8`
- **DDoS Attacks via Open DNS:** Attackers often exploit open DNS servers.
- **Protocols:**
  - **TCP (Transmission Control Protocol):** Connection-oriented.
  - **UDP (User Datagram Protocol):** Connectionless, often used for fast data transfer.
  - **DNS Port:** `53`

### Understanding RFC
Before learning DNS technology, read **RFC (Request for Comments)**, which acts as the **user manual** or **man page**.

### DNS Hierarchy & Resolution
- **Parent of DNS:** ICANN (Internet Corporation for Assigned Names and Numbers).
- **TLD Example:** `.edu.bd`
- Querying `dig iub.edu.bd` twice can help trace the lookup process.

### DNS Components
- **IP Anycast:** A Cisco-invented technology that routes users to the closest server.
- If a domain lacks a valid IP, its emails may end up in spam.

### Resource Records (RRs) in a Zone File
- If `ns1.apnic.net` is modified, update the **serial number manually**.
- **Example:** Serial `2020072002` → `2020072003` after an update.
- **Refresh Value:** `7200`

### Delegating a Zone
- **Command:** `dig apnic.net +trace`
- **Cybersecurity Focus:** Be prepared to act as both a **DNS attacker** and **defender**.

### Checking DNS Information
- **Command:** `dig iub.edu.bd ANY`
- **IUB's DNS Servers:** 2 authoritative DNS servers.

### DNS Software
- **BIND (Berkeley Internet Name Domain):** Popular DNS server software.
- **Configuration Files:** `.conf` files manage DNS settings.
- To **prevent recursive queries** from localhost, configure settings carefully.

### Zones in a Recursive Server
- **Example IPs:** `192.168.100.99` & `100.168.192`

### Security Best Practices
- **Always keep yourself updated** on security trends.
- **Failure isn't a barrier; it's a learning step.**
- **DNS Tunneling:** A common offensive technique in cybersecurity.

### Zone Transfers (AXFR & IXFR)
- **AXFR (Full Zone Transfer):** Transfers the entire DNS zone.
- **IXFR (Incremental Zone Transfer):** Transfers only changes.

### Best Practices for DNS Hosting
- **Separate Recursive & Authoritative Servers:** 
  - Avoid hosting both on the **same server**.
  - Keep them on **different Linux OS instances**.
  - Follow the **single-service-per-host** principle.

### Network Fundamentals
- **Routers operate at the Data Link Layer**.
- Understanding **OSI Model layers** is crucial for networking.
- **Slide presentations** contain valuable diagrams—review them carefully.

---
This README is structured for clarity and engagement. Let me know if you need further refinements! 🚀


# Day 2 ends here 

# Networking & Cyber Security Essentials

## Router & Data Link Layer
- **Router** operates at the **Data Link Layer**.
- Understanding which components function at each layer is crucial.
- Refer to the **slide images** for detailed illustrations.

---

## MAC Address & Layer Functions
- **MAC Address** is unique for each device.
- **Key Protocols:**
  - **Transport & Session Layers** → Used in **IP Phones**.
  - **Network, Transport, and Session Layers** → Play crucial roles in data communication.

---

## Cyber Security Concepts
### **Spoofing & Identity Protection**
- **MAC Spoofing** → Manipulating MAC address to conceal identity.
- **Man-in-the-Middle Attack** → Intercepting communications.
- **Reconnaissance** → Gathering intelligence before an attack.
- **Session Hijacking** → Unauthorized session control.
- **DNS Exploits** → Changing primary to secondary settings.
- **Exploits in Action** → Editors manipulated key files.

---

## DNS Manipulation & Security
- **DNS Version Modification** → Can be altered.
- **Command:** `version = go to sleep`

---

## Regular Expressions (Regex)
- **Learning Resource:** Google & YouTube (Estimated time: **1 hour**)
- **Usage:** Sorting domains, data filtering, and security analysis.

---

## Domain & Telecommunication Analysis
- **Example Domain:** `sips._tcp.bd-grameenphone.rcs.telephony.gob`
- **Key Questions:**
  - What happens after this process?
  - Does it involve telecommunications?
  - What are TXT and SRV records?

---

## DNS Analysis & Root Servers
- **TXT & MX Records** → Used in email and authentication.
- **For Analysis:** Microsoft Excel can be used for data structuring.
- **Recursive DNS Servers** → Forward queries to **Root Servers** for resolution.

---




