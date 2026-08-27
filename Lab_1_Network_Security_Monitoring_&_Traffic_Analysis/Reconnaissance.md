# Reconnaissance

## Objective

Perform controlled reconnaissance against the Windows VM to identify reachable network services and observe the activity from a defensive perspective.

## Target

- Windows VM

## Findings

- Windows VM was reachable using ICMP ping.
- An Nmap scan was performed against the Windows VM.
- No open ports were identified during the scan.
- No network services were identified as reachable during the scan.

## Initial Assessment

The Windows VM is reachable on the network, but no externally reachable services were identified during the reconnaissance activity.

Further investigation is required to determine whether host firewall configuration or network controls are affecting service visibility.

## Defensive Observation

OPNsense was monitored during the reconnaissance activity to identify whether the scanning traffic was visible in firewall activity/logs.

## OPNsense Observation

OPNsense was monitored during the reconnaissance activity.

The Live View displayed WAN-related logs, but corresponding LAN traffic from the Kali VM to the Windows VM was not visible.

The OPNsense LAN interface was confirmed as `192.168.1.1/24`. Firewall rules were currently disabled during the test.

Further investigation of OPNsense logging and firewall configuration will be performed in a later lab iteration.

## OPNsense Observation - 2

The reconnaissance traffic from Kali to Windows was not visible in OPNsense logs.

This was expected because both systems are on the same LAN subnet (`192.168.1.0/24`). The traffic is delivered directly between the two hosts at Layer 2 and does not traverse the OPNsense firewall.

This demonstrates the difference between:

- **Same-subnet traffic:** Host-to-host communication occurs directly.
- **Inter-subnet traffic:** Traffic must pass through a router/firewall such as OPNsense.

### Observations

- ICMP echo request and reply packets were observed, confirming that the Windows VM was reachable.
- Multiple TCP SYN packets were observed without completed TCP three-way handshakes.
- ARP request and reply packets were observed later in the capture.
- The TCP SYN pattern was consistent with port reconnaissance activity.

### Initial Assessment

The packet capture provides network-level evidence of reconnaissance activity from the Kali VM toward the Windows VM.
The repeated TCP SYN packets and incomplete handshakes indicate probing of TCP ports rather than normal application communication.

## Representative TCP Probe

- **Source IP:** `192.168.10.122` (Kali)
- **Destination IP:** `192.168.10.100` (Windows)
- **Destination Port:** `40185`
- **TCP Flag:** `SYN`

### Interpretation

The packet is a TCP SYN probe sent from the Kali VM to the Windows VM. A SYN packet is used to initiate a TCP connection and, when repeated across multiple destination ports, can provide evidence of TCP port reconnaissance.

### TCP Reconnaissance Observation

Wireshark showed multiple TCP packets from the Kali VM to the Windows VM targeting destination port `40185`.

## Observed packets included:

- `59855 → 40185` — SYN
