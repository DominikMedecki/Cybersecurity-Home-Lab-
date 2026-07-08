# 01 - Setting Up VirtualBox, Networks, and Kali Linux

## Overview
The goal is to create an isolated, low-cost lab environment where we can safely practice offensive and defensive security concepts.

## Objectives
- Install VirtualBox + Extension Pack.
- Configure custom internal networks (with DHCP).
- Download and set up Kali Linux as the attacker machine.
- Understand basic network isolation for safe labbing.

## Lab Network Design (High-Level)
- **NAT Adapter** → Kali gets internet access.
- **Host-Only / Internal Networks**:
  - `Vone-Labs` (Vulnerable network) – Isolated, DHCP-enabled.
  - `Hidden-Vone-Labs` – More isolated (future pivoting practice).
- Kali will have access to both the internet and the vulnerable network.
- Vulnerable machines (e.g. Metasploitable) will be added later.

## What I Did (Step-by-Step)

1. **Installed VirtualBox**
   - Downloaded from [virtualbox.org](https://www.virtualbox.org/).
   - Installed the main package (Windows host).
   - Installed the **VirtualBox Extension Pack** (for additional features).

2. **Handled Prerequisites**
   - Installed Microsoft Visual C++ Redistributable (required on fresh Windows 11 installs).

3. **Configured Custom Networks** (via Command Prompt)
   - Navigated to VirtualBox directory.
   - Used `VBoxManage` commands to create DHCP-enabled host-only networks:
     - `Vone-Labs` (e.g., 172.30.1.0/24)
     - `Hidden-Vone-Labs` (e.g., 10.205.1.0/24)

4. **Downloaded & Imported Kali Linux**
   - Downloaded the latest Kali Linux VirtualBox image from [kali.org](https://www.kali.org/).
   - Imported the `.ova` or configured a new VM.
   - Configured network adapters (NAT + internal network).

5. **Basic VM Setup**
   - Allocated RAM, CPU, and storage.
   - Started Kali and performed initial configuration.

## Screenshots
  Add  here 
- VirtualBox Manager after installation
- Network Manager / Created Host-Only Adapters
- `VBoxManage` commands and output
- Kali Linux VM settings (network adapters)
- Kali desktop after first boot

## Challenges & Troubleshooting
- C++ Redistributable error on fresh Windows installs.
- Network adapter order / connectivity issues.
- Extension Pack licensing note (personal/educational use only).
- Remembering exact `VBoxManage` syntax for network creation.

## Key Learnings
- How to set up a safe, segmented virtual lab environment.
- Difference between NAT, Host-Only, and Internal networking in VirtualBox.
- Importance of network isolation in cybersecurity labs (preventing accidental exposure).
- Basic VirtualBox administration and command-line management (`VBoxManage`).
- Foundations for building attacker and target machines.

## Skills Demonstrated
- Virtualization with VirtualBox
- Virtual network configuration & DHCP
- Secure lab design principles
- Kali Linux deployment
- Command-line troubleshooting

## Next Steps / Ideas to Extend
- Take snapshots of clean states.
- Document your exact network IP scheme.
- Add a Windows target machine next.
- Explore VirtualBox Guest Additions for better integration.

## Useful Links
- VirtualBox: https://www.virtualbox.org/
- Kali Linux: https://www.kali.org/

---

**Documented by**: Dominik Medecki  
**Date**: 08/07/2026
**Status**: Completed
