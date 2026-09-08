# 🛡️ Wazuh SIEM Lab

## 📖 Overview

This project demonstrates the deployment and configuration using
the open-source security tool Wazuh SIEM platform,
virusTotal integration and automation.

## 🎯 Objectives

- Deploy Wazuh: Manager & Dashboard
- Set Up Endpoints: Windows 11, Fedora
- Install Wazuh Server: Kali Linux
- Collect Endpoint Logs: Monitor endpoint activity
- Generate Events: Simulate security threats
- Detect Activity: Identify suspicious behaviour
- Investigate Alerts: Analyze Wazuh alerts
- Integrate VirusTotal: Malware analysis
- Automate Response: Delete detected malware

## 🏗️ Lab Architecture

| Component      | Details      |
| -------------- | ------------ |
| SIEM           | Wazuh        |
| Agent          | Windows 11   |
| Agent          | Fedora Linux |
| Server         | Kali Linux   |
| Virtualization | KVM/QEMU     |
| Network        | Host-only    |

![lab diagram](https://github.com/lapointek/wazuh-siem-lab/blob/main/screenshots/lab-diagram.png)

## ⚙️ Installation & Configuration

### 4.1 Wazuh Server

- Deploy Wazuh in a virtualized environment using KVM/Qemu
- Create a username and password when prompted
- Access Wazuh dashboard
- Install and register endpoint agents

### 4.2 VirusTotal Integration

- Obtain VirusTotal API key and configure Wazuh manager
- Define directory in ossec.conf
- Enable realtime monitoring
- Setup Wazuh server to monitor changes in the Linux agent for malware

## 🧪 Detection Testing

### Test 1 — Registry Changes

**Objective:** Detect registry changes

**Action:**
Installed packages using Winget

**Result:**
Wazuh File Integrity Monitor (FIM) displayed registry changes

![registry logs](https://github.com/lapointek/wazuh-siem-lab/blob/main/screenshots/registry-logs.png)

### Test 2 — Malware Detection

**Objective:** Detect Malware

**Action:**
- Configure Wazuh manager to use VirusTotal API key
- Download eicar malware into /tmp/malware/ directory defined in the ossec.conf

**Result:**
- Wazuh threat hunting detected and displayed an alert for the EICAR malware sample using VirusTotal integration.
- Wazuh threat hunting detected and analyzed a file that was identified as containing no malware using VirusTotal integration.

![threat logs](https://github.com/lapointek/wazuh-siem-lab/blob/main/screenshots/threat-logs.png)

## 🚨 Detection Testing
 Incident Response
- Detection - SIEM alert triggered by activity
- Investigation - Review relevant logs to determine the source
- Containment - Isolate affected host from network and quarantine/remove identified malware
- Remediation - Restore system to trusted state, and reset compromised credentials
- Document findings - Record key findings, affected systems, indicators of compromise
- Lessons learned - Identify gaps in detection and determine improvments to prevent similar incidents

## 🏁 Conclusion




