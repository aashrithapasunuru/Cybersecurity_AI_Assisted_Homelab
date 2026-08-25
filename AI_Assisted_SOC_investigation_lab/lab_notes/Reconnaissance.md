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
