# AI-Assisted SOC Investigation Lab

A hands-on SOC lab focused on **security monitoring, alert detection, log analysis, incident investigation, automation, and AI-assisted cybersecurity analysis**.

This lab simulates a basic SOC workflow using network, endpoint, firewall, SIEM, and AI-assisted investigation techniques.

---

## 🎯 Objective

The main objective of this lab is to practice how a SOC analyst investigates a security event from detection to final assessment.

The lab focuses on:

- Establishing a network baseline
- Generating controlled security activity
- Detecting suspicious activity
- Collecting security logs
- Investigating alerts
- Correlating security events
- Assessing security risk
- Using AI to assist investigation
- Validating AI-generated findings
- Documenting the investigation

---

## 🏗️ Lab Environment

The lab uses an isolated virtual environment.

```text
                    Internet
                       |
                   OPNsense
                Firewall / Gateway
                       |
              -------------------
              |                 |
         Windows VM          Kali / Linux
              |                 |
              -------------------
                       |
                 Security Events
                       |
          --------------------------
          |            |           |
      OPNsense       Wazuh       Windows
        Logs         Alerts       Events
          |            |           |
          ----------- Splunk -------
                       |
                SOC Investigation
                       |
                 AI-Assisted
                    Analysis
```

## 🧰 Tools & Technologies

### Virtualization & Operating Systems

- VirtualBox
- Windows VM
- Kali Linux
- Ubuntu/Linux VM

### Network Security

- OPNsense
- Nmap
- Wireshark

### SIEM & Security Monitoring

- Splunk
- Wazuh
- Windows Event Logs
- OPNsense Firewall Logs

### Security Testing

- Kali Linux
- Nmap
- Network traffic analysis
- Controlled reconnaissance

### Automation

- Python
- SQLite
- REST APIs

### AI

- AI-assisted alert analysis
- AI-assisted log analysis
- AI-assisted threat analysis
- AI-assisted risk assessment
- AI-assisted investigation support
- AI-assisted security reporting

---

## 🔄 SOC Investigation Workflow

```text
Network Baseline
       ↓
Reconnaissance
       ↓
Security Event
       ↓
Detection
       ↓
Alert Triage
       ↓
Evidence Collection
       ↓
Log Analysis
       ↓
Event Correlation
       ↓
AI-Assisted Analysis
       ↓
Analyst Validation
       ↓
Risk Assessment
       ↓
Final SOC Verdict
       ↓
Documentation

```
## 🧪 Lab Phases

### 1. Network Baseline

Establish normal network behavior before investigating suspicious activity.

Activities include:

- Identify lab systems
- Verify IP addresses
- Verify connectivity
- Review normal network traffic
- Review OPNsense firewall activity
- Identify normal services
- Observe normal security logs

---

### 2. Reconnaissance

Perform controlled reconnaissance against authorized systems within the lab environment.

Activities include:

- Host discovery
- Port scanning
- Service enumeration
- Network mapping

Tools:

- Nmap
- Kali Linux
- OPNsense
- Wireshark

The objective is to understand how reconnaissance activity appears from a defensive monitoring perspective.

---

### 3. Detection

Identify suspicious or unexpected activity using available security telemetry.

Detection sources include:

- OPNsense firewall logs
- Wazuh alerts
- Windows Security Events
- Splunk
- Network traffic

Examples include:

- Repeated connection attempts
- Port scanning
- Failed authentication attempts
- Suspicious network connections
- Unexpected services
- Unusual endpoint activity

---

### 4. Alert Triage

Determine whether a security alert requires further investigation.

Key questions include:

- What triggered the alert?
- When did it occur?
- Which host is involved?
- Which user is involved?
- What is the source?
- What is the destination?
- Is the activity expected?
- Are there related events?
- What is the severity?

---

### 5. Investigation

Investigate suspicious activity using multiple sources of evidence.

Evidence may include:

- OPNsense logs
- Splunk events
- Wazuh alerts
- Windows Event Logs
- Nmap results
- Wireshark captures
- Network information


### 🎯 Skills Practiced
SOC Operations
Alert Triage
SIEM & Log Analysis
Network Security
Threat Detection
Incident Investigation
Python Automation
AI-Assisted Cybersecurity
🚧 Lab Status

### In Progress

Hands-on investigations, evidence, screenshots, automation, and AI-assisted analysis will be added as the lab develops.

### ⚠️ Disclaimer

All testing is performed in a controlled and authorized laboratory environment for educational and defensive cybersecurity purposes.
