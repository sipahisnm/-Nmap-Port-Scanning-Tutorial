# -Nmap-Port-Scanning-Tutorial
This tutorial demonstrates how to use the **Nmap** command to scan for open ports on a server. The steps cover installation, basic scanning, scanning specific ports, and testing with applications.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installing Nmap](#installing-nmap)
- [Setting Up the Test Environment](#setting-up-the-test-environment)
- [Basic Nmap Scan](#basic-nmap-scan)
- [Scanning Specific Ports](#scanning-specific-ports)
- [Testing Open Ports with Applications](#testing-open-ports-with-applications)
- [Fast Scans](#fast-scans)
- [Scanning Domains](#scanning-domains)
- [Conclusion](#conclusion)

---

## Prerequisites
- Two servers: one for executing Nmap, one as the target.
- Basic knowledge of Linux commands.
- `ufw` firewall installed (optional for testing closed/open ports).

---

## Installing Nmap
If Nmap is not installed, you can install it using:

```bash
sudo apt install nmap
