# Wazuh SIEM Lab

## 1. Overview
This project demonstrates the deployment and configuration using
the open-source security tool Wazuh SIEM platform,
virusTotal integration and automation.

## 2. Objectives
- Deploy Wazuh: Manager & Dashboard
- Set Up Endpoints: Windows 11, Fedora
- Install Wazuh Server: Kali Linux
- Collect Endpoint Logs: Monitor endpoint activity
- Generate Events: Simulate security threats
- Detect Activity: Identify suspicious behaviour
- Investigate Alerts: Analyze Wazuh alerts
- Integrate VirusTotal: Malware analysis
- Automate Response: Delete detected malware

## 3. Architecture
| Component      | Details          |
|----------------|------------------|
| SIEM           | Wazuh            |
| Agent          | Windows 11       |
| Agent          | Fedora Linux     |
| Server         | Kali Linux       |
| Virtualization | KVM/QEMU         |
| Network        | Host-only        |

![lab diagram](https://github.com/lapointek/wazuh-siem-lab/blob/main/screenshots/lab-diagram.png)

## 4. Installation & Configuration
### 4.1 Wazuh Server
- Deploy Wazuh in a virtualized environment using KVM/Qemu
- Create a username and password when prompted
- Access Wazuh dashboard
- Install and register endpoint agents

### 4.2 Log Collection
Explain what logs/data are being collected.
- Malware
- File changes
- Registry changes

## 5. Detection Testing

### Test 1 — Registry Changes
**Objective:** Detect registry changes

**Action:**
Installed packages using Winget

**Result:**
Wazuh File Integrity Monitoring (FIM) showing registry changes

![registry logs](https://github.com/lapointek/wazuh-siem-lab/blob/main/screenshots/registry-logs.png)

## 6. Incident Response

1. Identify affected endpoint
2. Investigate the activity
3. Contain the endpoint
4. Remove the threat
5. Recover
6. Document findings

## 7. Conclusion
