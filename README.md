# Basic Vulnerability Scan on Your PC (Task-3)

This repository contains instructions for performing a **basic vulnerability assessment** on your personal computer using **OpenVAS Community Edition** . The goal is to identify potential security risks and learn fundamental cybersecurity assessment techniques.

---

## Objective
The primary aim is to:
- Learn how to **scan a system for vulnerabilities** using free security tools.
- Understand **how vulnerabilities are reported** and categorized.
- Identify **potential fixes or mitigations** for detected issues.
---

## Tools Required

-**openVAS** (an open-source vulnerability scanner and management tool. It is part of the Greenbone Vulnerability Management (GVM))
-or
-**Nessus Essentials** (free tier of the popular Nessus vulnerability scanner developed by Tenable, Inc.)

## Prerequisites
Before proceeding, ensure that you have:
- A **Windows/Linux machine** (or a virtual machine if preferred).
- Installed either:
  - ✅ [OpenVAS Community Edition](https://www.openvas.org/)
  - ✅ [Nessus Essentials](https://www.tenable.com/products/nessus/nessus-essentials)
- Basic knowledge of **IP addresses and system security**.

---
## Installation!
### Update the system
```bash
sudo apt update && sudo apt full-upgrade -y
```
### Install GVM (openVAS)
```bash
sudo apt install -y gvm
```
### Run the setup script
```bash
sudo gvm-setup
```
### To create your own password
```bash
sudo gvmd --user=admin --new-password=<YourNewPassword>
```
### Start GVM services
```bash
sudo gvm-check-setup
```
```bash
sudo gvm-start
```
## Working!
### Finding system’s IP address
```bash
ip a
```
### Access the default interface
```bash
https://127.0.0.1:9392
```
or
```bash
https://localhost:9392
```

### Log in using the credentials you configured:
user:- admin
password:- *****(password you set-up)

### If you encounter a "Potential Security Risk Ahead" warning

Click on **Advanced** and proceed to the site.

### After logging in
1. Navigate to the Tasks section.
2. Click on Create New Task.
3. Enter your system’s local IP (e.g., 192.168.2.123).
4. Set the scan configuration to Full and Fast.
5. Wait for the scan to complete.
6. When the status shows Completed, your scan is finished and the results are available.
7. Download and analyze the report to review any discovered vulnerabilities.

---

## Additional Attachments
### REPORT (xml)
This XML-based file serves as a scan report outlining various assessments conducted on the host **192.168.2.123**. It encompasses a range of tests focused on identifying vulnerabilities and gathering asset inventory information.
### VULNERABILITIES (xml)
This XML-based text file contains the results of a vulnerability scan, organized in a structured format. It includes detailed information about identified vulnerabilities such as their names, severity levels, timestamps, and the associated hosts.



