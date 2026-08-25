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

## 🏗️ Lab Architecture

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

  ```
## Security Domains

This homelab covers multiple areas of practical cybersecurity.

### Network Security

- Firewall configuration and administration
- Network segmentation
- TCP/IP and network troubleshooting
- DNS and DHCP
- Network traffic analysis
- ARP monitoring
- Network discovery and enumeration

### Security Monitoring & SIEM

- Security log collection
- Log analysis
- Security event monitoring
- Alert investigation
- Event correlation
- Detection rules
- Security dashboards

### Endpoint Security

- Windows security monitoring
- Endpoint telemetry
- Authentication event analysis
- Process and activity monitoring
- EDR concepts
- Suspicious activity investigation

### Vulnerability Management

- Network discovery
- Port scanning
- Service enumeration
- Vulnerability scanning
- Vulnerability analysis
- Risk prioritization
- Security remediation

### SOC Operations

- Alert triage
- Security event investigation
- Threat detection
- Incident analysis
- Evidence collection
- Risk assessment
- Incident documentation

### AI-Assisted Cybersecurity

- AI-assisted alert analysis
- AI-assisted log analysis
- Threat analysis
- Security event summarization
- Risk assessment
- Investigation support
- Security automation
- AI-assisted reporting

---

## Tools & Technologies

### Network Security

- OPNsense
- Nmap
- Wireshark
- Kali Linux
- VirtualBox

### SIEM & Monitoring

- Splunk
- Wazuh
- Windows Event Logs
- Linux Logs

### Vulnerability & Security Testing

- Nessus
- Metasploitable
- VulnHub
- OWASP Juice Shop
- TryHackMe

### Development & Automation

- Python
- Flask
- SQLite
- REST APIs
- Git
- GitHub

### AI

- AI-assisted security analysis
- AI-assisted threat detection
- AI-assisted log analysis
- AI-assisted incident investigation
- AI-assisted security automation

---

## Security Labs

### Network Security

- Firewall and network configuration
- Network discovery
- Nmap scanning
- Wireshark traffic analysis
- DNS and DHCP troubleshooting
- ARP analysis
- Network security monitoring

### SIEM & SOC

- Log collection and analysis
- Security alert investigation
- Authentication event investigation
- Threat detection
- Incident investigation
- SOC alert triage

### Vulnerability Management

- Vulnerability scanning
- Service enumeration
- Web application testing
- Vulnerability analysis
- Risk assessment

### AI Security

- AI-assisted alert investigation
- AI-assisted log analysis
- AI-generated security explanations
- AI-assisted risk analysis
- AI-assisted investigation workflows
- Python + AI security automation

---

## AI-Assisted Security Workflow

AI is used as an analyst-support capability to help analyze security data and improve investigation workflows.

```text
Security Event
      ↓
Log / Data Collection
      ↓
Detection
      ↓
Alert Triage
      ↓
AI-Assisted Analysis
      ↓
Threat & Risk Assessment
      ↓
Analyst Validation
      ↓
Response / Recommendation
      ↓
Documentation

```

## Security Investigation Methodology

Each investigation follows a structured cybersecurity workflow:

1. Identify the security event
2. Collect relevant logs and evidence
3. Analyze network and endpoint activity
4. Determine whether the activity is suspicious
5. Identify potential attack techniques
6. Assess severity and risk
7. Validate findings using available evidence
8. Recommend or perform defensive actions
9. Document the investigation and findings

---

## Automation

Python is used to automate repetitive security tasks and support cybersecurity operations.

Automation areas include:

- Security monitoring
- Log processing
- Data collection
- Alert generation
- API integrations
- Threat analysis
- Risk scoring
- Security reporting
- AI-assisted security workflows

---

## Learning Approach

Each lab follows a practical workflow:

```text
Learn
  ↓
Build
  ↓
Configure
  ↓
Test
  ↓
Troubleshoot
  ↓
Detect
  ↓
Investigate
  ↓
Automate
  ↓
Analyze with AI
  ↓
Document

```

## Disclaimer

All security testing and experimentation in this repository is performed in controlled laboratory environments for educational and defensive cybersecurity purposes.

Do not use security tools, techniques, or scripts against systems without proper authorization.

Project Status

## 🚧 Active Development

This homelab is continuously evolving as new cybersecurity tools, security scenarios, automation projects, detection techniques, SOC investigations, and AI-assisted workflows are added.

## Focus

### Cybersecurity • Network Security • SOC • Automation • AI

The goal of this project is to develop practical cybersecurity skills and understand how modern security teams can combine security tools, automation, and AI-assisted analysis to improve detection, investigation, and response



