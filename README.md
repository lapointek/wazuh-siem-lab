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

### 4.2 Log Collection

- Malware
- File changes
- Registry changes

## 🚨 Detection Testing

### Test 1 — Registry Changes

**Objective:** Detect registry changes

**Action:**
Installed packages using Winget

**Result:**
Wazuh File Integrity Monitoring (FIM) displayed registry changes

![registry logs](https://github.com/lapointek/wazuh-siem-lab/blob/main/screenshots/registry-logs.png)

### Test 2 — Malware Detection

**Objective:** Detect Malware

**Action:**
- Integrate VirusTotal into Wazuh
- Installed eicar malware into /tmp/malware/ directory

**Result:**
Wazuh threat hunting monitoring displayed alert for eicar file

![threat logs](https://github.com/lapointek/wazuh-siem-lab/blob/main/screenshots/threat-logs.png)

## 🕵️ Incident Response

1. Identify affected endpoint
2. Investigate the activity
3. Contain the endpoint
4. Remove the threat
5. Recover
6. Document findings

## 🏁 Conclusion
