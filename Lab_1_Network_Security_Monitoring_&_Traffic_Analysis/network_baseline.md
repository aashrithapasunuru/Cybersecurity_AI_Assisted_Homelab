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

## Connectivity verification
- Verified network connectivity between kali, OPNsense and windows VM using ICMP ping test.
- OPNsense - kali -- Successful
- OPNsense - windows VM -- Successful
- kali -- windows VM -- Successful
  
- The OPNsense console confirmed the firewall interface configuration, and the Windows VM confirmed OPNsense as the default gateway. All three systems are configured within the same lab subnet.

## DNS & Internet Connectivity

DNS and Internet connectivity were verified from the Kali Linux VM.

Kali → OPNsense: Successful
Kali → External IP: Successful
Kali → Domain resolution: Successful
DNS server: OPNsense
Internet connectivity: Verified
The Kali VM was able to communicate with the OPNsense gateway, reach an external IP address, and resolve external domain names successfully.
