#  SOC Monitoring Lab with Splunk

## Overview
This project simulates a real-world Security Operations Center (SOC) environment using Splunk as a SIEM platform. The goal is to collect logs from Windows and Linux systems, analyze them, and detect common cyberattacks such as brute force attempts, port scanning, and suspicious logins.

---

##  Objectives
- Build a centralized log monitoring system
- Collect Windows and Linux logs in Splunk
- Simulate real cyberattacks
- Create detection rules for threats
- Visualize security events using dashboards

---

##  Architecture

![SOC Architecture](architecture.png)

---
<img width="429" height="654" alt="image" src="https://github.com/user-attachments/assets/b66f9669-869d-4324-9acc-a62a9ea2bba5" />


##  Tools & Technologies
- Splunk Enterprise (SIEM)
- Windows 10 (log source)
- Lubuntu Linux VM (log source)
- Splunk Universal Forwarder
- Sysmon (Windows logging enhancement)

---

## 📡 Data Sources
- Windows Event Logs (Security, System)
- Linux Authentication Logs (/var/log/auth.log)
- Network connection logs

---

## Detected Threats

### 1. Brute Force Attack
- Multiple failed login attempts within a short time window
- Target: SSH (Linux) and Windows login attempts

### 2. Port Scanning
- High number of connection attempts across multiple ports
- Detected using rapid network activity patterns

### 3. Suspicious Login Activity
- Logins from unknown IP addresses
- Unusual login times or admin account usage

---

## Attack Simulations

- SSH brute force simulation using repeated failed login attempts
- Nmap port scan against Linux VM
- Invalid login attempts on Windows system

---

## Dashboards
Splunk dashboards were created to visualize:
- Failed login trends over time
- Top source IPs
- Network scanning activity
- Successful vs failed authentication attempts

---

## Project Structure
- `setup/` → Installation and configuration guides
- `detections/` → Splunk search queries for threat detection
- `simulations/` → Attack simulation steps and results
- `screenshots/` → Evidence of logs, alerts, and dashboards

---

## Key Learnings
- SIEM log ingestion and analysis
- Detection engineering basics
- Real-world SOC workflows
- Attack simulation and monitoring
- Security event correlation

---

## Future Improvements
- Add email alerting system
- Map detections to MITRE ATT&CK framework
- Add Splunk Enterprise Security features
- Automate threat detection rules
