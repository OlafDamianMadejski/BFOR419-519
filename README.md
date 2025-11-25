# BFOR419-519
Final Project

# **PHP-FPM Reverse Tunnel Exploitation & Persistence Demonstration**  
### *CVE-2019-11043 — Debian PHP-FPM Path Handling Vulnerability*

---

## **Project Overview**

In October 2019, Debian Security Advisory researchers **Emil Lerner** and **Andrew Danau** published a notice warning the Debian community about a critical vulnerability in PHP-FPM. Due to **insufficient validation in PHP-FPM’s path handling code**, attackers could manipulate specially crafted requests to achieve **remote arbitrary code execution** under certain NGINX + PHP-FPM configurations.

This lab demonstrates the exploitation of:

### **CVE-2019-11043**  
*A vulnerability affecting PHP-FPM running behind NGINX that, when triggered, can allow attackers to execute arbitrary code and establish persistence through reverse tunneling.*

The project recreates a vulnerable environment, executes the exploit chain, and evaluates how adversaries achieve persistence through tunneling techniques in real-world scenarios.

---

## **Project Relevance**

### **Why This Matters Today**
Reverse tunneling for persistence is a **high-frequency TTP (Tactic, Technique, Procedure)** used across APT groups, botnets, and ransomware operators. PHP-FPM remains widely deployed in production environments, and the misconfigurations exploited by CVE-2019-11043 are still observed in the wild.

This attack chain aligns directly with several high-impact **MITRE ATT&CK** techniques:

| MITRE ID | Technique Name |
|---------|-----------------------------|
| **T1071** | Application Layer Tunneling |
| **T1572** | Protocol Tunneling |
| **T1090** | Proxy / Reverse Proxy |
| **T1505** | Server-Side Components (PHP-FPM) |
| **T1574** | Hijacking Execution Flow |

These are not theoretical abstractions — they mirror the exact behaviors documented in active exploitation campaigns involving nation-state actors and ransomware groups.

---

## **Methodology**



---

## **Results**



---

## **Conclusion**

The exploitation of CVE-2019-11043 demonstrates how a single misconfiguration in PHP-FPM and NGINX can lead to **server takeover and persistent adversary access**.  
The Debian Security Advisory team confirmed that upgrading **php7.0 to version 7.0.33 or later** fully patches this vulnerability.

Proper patching, hardened NGINX configurations, and monitoring for tunneling behaviors are critical in preventing similar attacks in modern environments.

---

## **References**

- CVE Details – https://nvd.nist.gov/vuln/detail/cve-2019-11043  
- CVE Record – https://www.cve.org/CVERecord?id=CVE-2019-11043  
- Debian Security Advisory – https://lists.debian.org/debian-security-announce/2019/msg00204.html  

---
