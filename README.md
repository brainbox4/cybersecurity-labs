# Lab Project 1 – Network Vulnerability Assessment

## Overview
This project documents a hands-on vulnerability assessment conducted against a deliberately vulnerable machine (Metasploitable2) using industry-standard security tools in a controlled lab environment.

The goal of this lab was to simulate a real-world vulnerability assessment workflow, from reconnaissance to vulnerability scanning and analysis.

---

## Lab Environment
- **Attacker / Scanner:** Kali Linux
- **Target Machine:** Metasploitable2
- **Vulnerability Scanner:** Nessus Essentials
- **Reconnaissance Tool:** Nmap
- **Target IP Address:** 192.168.56.103
- **Network Configuration:** Host-Only / NAT Virtual Lab

---

## Objectives
- Perform network reconnaissance using Nmap
- Identify open ports and running services
- Conduct a vulnerability scan using Nessus Essentials
- Analyze and document discovered vulnerabilities
- Understand real-world security risks and remediation strategies

---

## Methodology

### 1. Network Reconnaissance (Nmap)
Nmap was used to discover open ports and identify services running on the target machine.

Example scan:nmap -sV -A 192.168.56.103

---

### 2. Vulnerability Scanning (Nessus)
A basic network scan was configured in Nessus Essentials targeting the Metasploitable2 IP address.

Scan configuration:
- Scan Type: Basic Network Scan
- Target: 192.168.56.103
- Credentials: None (unauthenticated scan)

---

## Key Findings

### Critical Vulnerabilities
- SSL Version 2 and 3 Protocol Detection
- Bind Shell Backdoor (Port 1524)
- Apache Tomcat End-of-Life (≤ 5.5.x)
- Debian OpenSSL Random Number Generator Weakness

### High Severity Vulnerabilities
- Samba Badlock Vulnerability
- ISC BIND Service Downgrade / Reflected DoS

---

## Impact
The identified vulnerabilities could allow an attacker to:
- Gain unauthorized shell access
- Perform man-in-the-middle attacks
- Compromise cryptographic communications
- Disrupt critical services
- Achieve full system compromise

---

## Recommendations
- Disable deprecated SSL protocols (SSLv2 / SSLv3)
- Upgrade unsupported and outdated services
- Remove unauthorized services and backdoors
- Regenerate cryptographic keys generated with weak entropy
- Apply vendor security patches and updates

---

## Disclaimer
This project was conducted strictly in a controlled lab environment for educational and ethical purposes only. No production systems were harmed.

