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
```


Setting Up the Test Environment

Enable the firewall on the target server to close all ports:
``` 
sudo ufw enable

---

Warning: This may disrupt SSH connections.

Confirm that no ports are open. This provides a known starting point for scans.

Basic Nmap Scan

To scan all default 1,000 ports:

nmap <target-ip>


This may take some time as Nmap checks each port.

Press Enter to see progress.

If all ports are filtered, the firewall is blocking them.

Scanning Specific Ports

To scan a specific port or range:

nmap -p 1-100 <target-ip>


Quicker than scanning all ports.

Example: Port 17 may appear closed if no application is listening.

Testing Open Ports with Applications

Simulate an application listening on a port using Netcat:

nc -l 17


Scan that specific port:

nmap -p 17 <target-ip>


The port should now show as open.

Install a real service (e.g., Nginx):

sudo apt install nginx


Nginx typically opens port 80 (HTTP) and 443 (HTTPS).

Fast Scans

Use the -F flag for a faster scan of common ports:

nmap -F <target-ip>


Scans fewer ports but completes quickly.

Make sure the firewall is disabled if ports appear filtered:

sudo ufw disable

Scanning Domains

You can scan domain names instead of IP addresses:

nmap <domain-name>


Example: Google usually has ports 80 (HTTP) and 443 (HTTPS) open.

Conclusion

This tutorial demonstrates:

Installing and using Nmap.

Performing basic and fast scans.

Scanning specific ports.

Detecting open ports with or without listening applications.
