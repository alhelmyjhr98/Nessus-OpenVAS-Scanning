# Nessus & OpenVAS Vulnerability Scanning

## 📌 Overview
This repository documents the process of setting up, running, and analyzing vulnerability scans using **Nessus** and **OpenVAS**. The project aims to demonstrate hands-on experience with vulnerability management, security hardening, and remediation strategies.

## 🎯 Objectives
- Install and configure **Nessus** and **OpenVAS** on a Kali Linux VM.
- Perform full vulnerability scans on a test network or local machine.
- Analyze findings and prioritize vulnerabilities based on **CVSS scores**.
- Document mitigation strategies for identified vulnerabilities.

## 🛠️ Tools & Technologies
- **Operating System**: Kali Linux (Virtual Machine)
- **Scanning Tools**:
  - [Nessus](https://www.tenable.com/products/nessus)
  - [OpenVAS](https://www.openvas.org/)
- **Additional Tools**:
  - Linux CLI
  - Python (optional for automation)

## 🚀 Setup Guide
### 1️⃣ Install Nessus
```bash
curl -o Nessus.deb https://www.tenable.com/downloads/api/v1/public/pages/nessus/downloads/####/download?i_agree_to_tenable_license_agreement=true
sudo dpkg -i Nessus.deb
sudo systemctl start nessusd
```
- Access Nessus via: `https://localhost:8834`
- Register with a **Tenable** account.

### 2️⃣ Install OpenVAS
```bash
sudo apt update && sudo apt install openvas
sudo gvm-setup
sudo gvm-start
```
- Access OpenVAS via: `https://localhost:9392`

## 🔍 Performing a Scan
### **Nessus Scan**
1. Open the Nessus web UI.
2. Create a **New Scan** > Select **Basic Network Scan**.
3. Configure scan targets (e.g., local machine or subnet `192.168.1.0/24`).
4. Run the scan and wait for results.

### **OpenVAS Scan**
1. Log into **Greenbone Security Assistant** (`https://localhost:9392`).
2. Configure a **Target** and **Scan Task**.
3. Start the scan and monitor progress.

## 📊 Results & Analysis
- 📂 **Reports/** _(CSV, JSON, PDF scans)_
- 🖼️ **Screenshots/** _(show scanning process)_
- 📝 **Remediation_Plan.md** _(List vulnerabilities & fixes)_

## ✅ Key Learnings
- Hands-on experience with industry-standard vulnerability scanners.
- Understanding CVSS scoring and vulnerability prioritization.
- Security hardening techniques based on findings.

## 📂 Repository Structure
```
Nessus-OpenVAS-Scanning/
│-- Reports/
│   ├── nessus_scan_report.pdf
│   ├── openvas_scan_report.json
│-- Screenshots/
│   ├── nessus_dashboard.png
│   ├── openvas_results.png
│-- Remediation_Plan.md
│-- README.md
```

## 📢 Disclaimer
⚠️ **This project is for educational and ethical purposes only. Do NOT scan networks you do not own or have explicit permission to assess.**

---

💡 **Want to contribute?** Feel free to open issues or submit pull requests to improve this project! 🚀

