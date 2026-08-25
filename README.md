# Cybersecurity AI Homelab

A hands-on cybersecurity home lab designed to build practical experience across **network security, firewalls, SIEM, EDR, vulnerability management, security monitoring, SOC operations, automation, and AI-assisted cybersecurity analysis**.

This repository documents the labs, configurations, troubleshooting, security investigations, automation scripts, and AI-assisted workflows developed throughout the learning process.

---

## 🎯 Project Goal

The goal of this homelab is to simulate a small enterprise security environment where different security technologies can be deployed, tested, monitored, and investigated.

The lab focuses on developing practical skills in:

- Network security
- Firewall administration
- Security monitoring
- SIEM
- EDR concepts
- Vulnerability management
- Threat detection
- Incident investigation
- SOC operations
- Security automation
- Python scripting
- AI-assisted security analysis
- Security documentation

The long-term objective is to build an environment where security events can be **generated → detected → logged → investigated → analyzed → automated**, with AI supporting the analyst throughout the workflow.

---

# 🏗️ Lab Architecture

The homelab uses virtual machines and security tools to create an isolated cybersecurity practice environment.

```text
                         Internet
                            |
                            |
                    Firewall / Gateway
                      OPNsense / Other
                            |
                     ----------------
                     |              |
                     |              |
                Windows VM       Linux VMs
                     |              |
                     |              |
                     ------ Network -
                            |
                   -------------------
                   |                 |
              Security Logs       Network Traffic
                   |                 |
                   -------------------
                            |
                  Security Monitoring
                            |
                 -----------------------
                 |          |            |
               SIEM        EDR       Detection
            Splunk/Wazuh   Tools      Tools
                 |          |            |
                 ------------------------
                            |
                     SOC Investigation
                            |
                     ----------------
                     |              |
                 Automation       AI Analysis
                    Python       AI-Assisted
                                  Detection






