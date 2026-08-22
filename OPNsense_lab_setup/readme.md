# OPNsense Home Lab

Hands-on OPNsense home lab for firewall administration, network security, and SOC practice.

## Goal

Build a virtual WAN/LAN environment using OPNsense and a Windows VM to practice firewall administration, networking, troubleshooting, and security monitoring.

## Lab Setup

| Component | Detail |
|---|---|
| Hypervisor | Oracle VirtualBox |
| Firewall | OPNsense |
| Client | Windows 10 VM |
| OPNsense WAN | VirtualBox NAT |
| OPNsense LAN | Host-Only Adapter #2 |
| LAN subnet | 192.168.1.0/24 |
| OPNsense LAN IP | 192.168.1.1 |

## Network Topology

```
Internet
   |
VirtualBox NAT
   |
OPNsense WAN (em0)
   |
OPNsense LAN (em1) -- 192.168.1.1
   |
Host-Only Network
   |
Windows 10 VM
```

## Lab Log

### Session 1 — Initial Setup & Connectivity

**Completed**
- [x] Created OPNsense VM
- [x] Configured WAN and LAN adapters
- [x] Installed OPNsense to virtual disk
- [x] Removed installation ISO
- [x] Connected Windows VM to OPNsense LAN
- [x] Fixed WAN/LAN interface assignment
- [x] Accessed OPNsense Web GU
- [x] Verified Windows → OPNsense connectivity
- [x] Verified internet connectivity
- [x] Verified DNS resolution

**Problem**
Windows VM initially received an APIPA address (169.254.x.x) instead of a valid IP, and couldn't reach OPNsense at all.

**Root Cause**
Two layered issues:
1. OPNsense em0,em1 interfaces were mapped backwards — LAN was assigned to the adapter facing NAT, and WAN was assigned to the adapter facing the Host-Only network — so Windows had no path to OPNsense LAN.
2. OPNsense was running in **live mode** directly from the installer ISO, so every configuration change (interface assignments, passwords) reverted on reboot.

**Fix**
- Corrected the interface mapping:
  - `em0` → WAN (NAT)
  - `em1` → LAN (Host-Only)
- Installed OPNsense permanently to the virtual disk via the console `installer` login.
- Removed the installation ISO from the VM's virtual optical drive so it boots from disk going forward.

**Key Lessons**
- Verify WAN/LAN interface mapping against actual VirtualBox adapter attachments — don't assume `em0`/`em1` order matches intent.
- Cross-reference MAC addresses between VirtualBox and the OPNsense console to confirm which physical adapter is which.
- Troubleshoot connectivity layer by layer: verify link/interface status → IP configuration → ping the gateway → verify DHCP → test Internet connectivity → verify   DNS, rather than changing DHCP configuration immediately.
- Confirm configuration is actually persistent (installed to disk) before debugging settings that "don't stick."
- Always remove installation media after install completes.

## Next Steps

- Configure firewall rules
- Enable firewall logging
- Analyze network traffic
- Build SOC monitoring dashboard
- Integrate Python for automation/log parsing
- Integrate AI-assisted security analysis
