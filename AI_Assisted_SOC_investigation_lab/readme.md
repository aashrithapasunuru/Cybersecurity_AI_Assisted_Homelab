# Lab 1 — Network Security Monitoring & Traffic Analysis

A hands-on cybersecurity lab focused on **network security monitoring, traffic analysis, firewall monitoring, reconnaissance detection, and AI-assisted investigation**.

This lab simulates a basic SOC investigation using an isolated virtual network environment.

---

## 🎯 Objective

The main objective of this lab is to practice how a SOC analyst monitors and investigates network activity from detection to final assessment.

The lab focuses on:

* Establishing a network baseline
* Understanding normal network communication
* Generating controlled network activity
* Monitoring firewall activity
* Analyzing network traffic
* Investigating suspicious connections
* Identifying reconnaissance activity
* Assessing security risk
* Using AI to assist investigation
* Validating AI-generated findings
* Documenting the investigation

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
         Windows VM          Kali Linux
              |                 |
              -------------------
                       |
                Network Traffic
                       |
              -------------------
              |                 |
         OPNsense Logs      Wireshark
              |                 |
              ----------- -----------
                         |
                  Investigation
                         |
                  AI-Assisted
                     Analysis
```

---

## 🧰 Tools & Technologies

### Virtualization & Operating Systems

* VirtualBox
* Windows VM
* Kali Linux

### Network Security & Monitoring

* OPNsense
* Wireshark
* Nmap
* TCP/IP
* ARP
* ICMP
* Network traffic analysis
* Firewall monitoring

### AI

* AI-assisted network traffic analysis
* AI-assisted security investigation
* AI-assisted risk assessment
* AI-assisted finding interpretation
* AI-assisted security reporting

---

## 🔄 SOC Investigation Workflow

```text
Network Baseline
       ↓
Controlled Network Activity
       ↓
Detection
       ↓
Traffic Analysis
       ↓
Evidence Collection
       ↓
Investigation
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

---

## 🧪 Lab Phases

### 1. Network Baseline

Establish normal network behavior before investigating suspicious activity.

Activities include:

* Identify lab systems
* Verify IP addresses
* Verify connectivity
* Review normal network traffic
* Review OPNsense firewall activity
* Identify expected network communication

---

### 2. Controlled Network Activity

Generate authorized network activity within the isolated lab environment.

Activities include:

* Host discovery
* Port scanning
* Service enumeration
* Network communication testing

Tools:

* Nmap
* Kali Linux
* OPNsense
* Wireshark

The objective is to understand how network reconnaissance and connection attempts appear from a defensive monitoring perspective.

---

### 3. Network Traffic Analysis

Analyze network traffic generated during the lab.

Activities include:

* Identify source and destination IP addresses
* Examine TCP connections
* Analyze SYN and ACK packets
* Observe ARP traffic
* Identify connection attempts
* Analyze unusual or unexpected traffic

Wireshark is used to inspect the network packets and understand the communication between systems.

---

### 4. Firewall Monitoring

Review OPNsense firewall activity related to the generated network traffic.

Activities include:

* Review firewall logs
* Identify source and destination addresses
* Identify ports and protocols
* Determine whether traffic was allowed or blocked
* Understand how traffic crosses the firewall

---

### 5. Investigation

Correlate network evidence from multiple sources.

Evidence may include:

* OPNsense firewall logs
* Wireshark packet captures
* Nmap scan results
* Source and destination IP addresses
* Ports and protocols
* Timestamps

Key investigation questions:

* What happened?
* Which system generated the activity?
* Which system was targeted?
* What ports were involved?
* Was the activity expected?
* Is there evidence of reconnaissance?
* What is the potential security impact?

---

### 6. AI-Assisted Analysis

AI is used as an **investigation assistant**, not as a replacement for analyst judgment.

AI may be used to:

* Explain network traffic
* Interpret suspicious indicators
* Identify possible attack techniques
* Suggest additional investigation steps
* Assist with risk assessment
* Help summarize findings

AI-generated findings are validated against the actual lab evidence before reaching a final conclusion.

---

## 🎯 Skills Practiced

### SOC Operations

* Security Monitoring
* Network Traffic Analysis
* Alert Investigation
* Evidence Collection
* Threat Detection
* Risk Assessment
* Incident Investigation

### Networking

* TCP/IP
* ARP
* ICMP
* TCP connections
* Ports and protocols
* Network troubleshooting

### Security Tools

* OPNsense
* Wireshark
* Nmap
* Kali Linux

### AI-Assisted Security

* AI-assisted investigation
* AI-assisted traffic analysis
* AI-assisted risk assessment
* AI finding validation

---

## 🚧 Lab Status

### In Progress

The lab is being developed through small hands-on investigations.

Completed activities and evidence will be documented with:

- network_baseline.md
- reconnaissance.md
- AI-Assisted-analysis.md

---

## ⚠️ Disclaimer

All testing is performed in a controlled and authorized laboratory environment for educational and defensive cybersecurity purposes.

