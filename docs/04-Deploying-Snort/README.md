# 04 - Deploying Snort (NIDS on Ubuntu Server)

## Overview
In this video we shift focus toward **blue team / defensive security** by deploying **Snort**, a powerful open-source **Network Intrusion Detection System (NIDS)**.

We install a fresh **Ubuntu Server** VM and configure Snort to monitor traffic on the vulnerable lab network.

## Objectives
- Create and install a new Ubuntu Server VM from ISO.
- Configure dual networking (internet + lab network).
- Install and perform basic configuration of Snort.
- Set up a simple detection rule and test it.

## What I Did (Step-by-Step)

1. **Downloaded Ubuntu Server ISO**
   - Used the latest LTS version from ubuntu.com.

2. **Created New VM in VirtualBox**
   - Named it "Snort-VM".
   - Allocated 4 GB RAM, 2 CPUs, ~25 GB disk.
   - Attached Ubuntu Server ISO.

3. **Network Configuration**
   - Adapter 1: NAT / Bridged (for internet access during install).
   - Adapter 2: Internal network (`Vone-Labs` or your vulnerable network) with Promiscuous Mode set to "Allow All" (critical for IDS/monitoring).

4. **Installed Ubuntu Server**
   - Went through the installer (language, keyboard, network interfaces, disk setup, user creation, etc.).
   - Noted network interface names for Snort configuration.

5. **Installed & Configured Snort**
   - Updated system and installed Snort.
   - Configured basic rules.
   - Tested detection (e.g., simple ping or port scan rule).

6. **Verification**
   - Confirmed Snort is running and generating alerts.

## Screenshots
*(Add your screenshots here — especially important for this one)*
- Ubuntu Server installer screens
- Network adapter settings in VirtualBox (Promiscuous Mode)
- Network interfaces identified during install (`ip addr`)
- Snort installation and rule configuration
- Snort alerts/logs when testing from Kali

## Challenges & Troubleshooting
- Identifying the correct network interface for the lab network.
- Promiscuous mode not enabled (Snort won't see traffic).
- Package installation / dependency issues.
- Rule syntax errors in Snort config.

## Key Learnings
- Installing Ubuntu Server from scratch.
- Dual-homed VM setup for monitoring.
- Basics of Network Intrusion Detection Systems (NIDS).
- Importance of promiscuous mode for traffic sniffing.
- Introduction to writing simple Snort rules.

## Skills Demonstrated
- Linux server deployment
- IDS/monitoring tool installation
- Network interface management
- Defensive security tooling
- Lab segmentation for blue team practice

## Next Steps / Ideas to Extend
- Create more custom Snort rules.
- Test various attacks from Kali and observe alerts.
- Explore Snort as IPS (Intrusion Prevention) in a future video.
- Forward logs to a SIEM (like Wazuh later in the series).


---

**Documented by**: [Your Name]  
**Date**: [Today's Date]  
**Status**: Completed
