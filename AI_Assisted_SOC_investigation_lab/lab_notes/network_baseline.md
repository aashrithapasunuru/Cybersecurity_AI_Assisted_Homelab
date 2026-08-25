## Lab Topology
``` text
                 Internet
                    │
                 OPNsense
              Firewall/Gateway
                    │
             ───────┴───────
             Lab Network
             │             │
        Windows VM      Kali VM
          Victim         Analyst

```
### VM IP address (sanitized)
- OPNsense IP : 192.168.10.1 (OPNsense acting as default gateway)
- Windows VM : 192.168.10.100
- kali VM : 192.168.10.122
- Network : 192.168.10.0/24
