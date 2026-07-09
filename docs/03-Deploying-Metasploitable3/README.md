# 03 - Deploying Metasploitable 3

## Overview
In this video, we deploy **Metasploitable 3**, a more modern and complex vulnerable virtual machine compared to Metasploitable 2. It is built using Vagrant and includes a wider variety of services and vulnerabilities, making it excellent for practicing realistic exploitation, privilege escalation, and post-exploitation.

## Objectives
- Download and set up Metasploitable 3 in VirtualBox.
- Configure it on the isolated vulnerable network.
- Verify it is running and accessible from the Kali attacker machine.

## What I Did (Step-by-Step)

1. **Downloaded Metasploitable 3**
   - Followed the video instructions to obtain the necessary files (usually involves Vagrant box or pre-built VM images).

2. **Imported / Configured the VM**
   - Imported the virtual machine into VirtualBox.
   - Allocated appropriate resources (RAM, CPU cores, disk space).

3. **Network Configuration**
   - Attached the network adapter to the internal vulnerable network (`Vone-Labs` or equivalent from Video #1).
   - Ensured no direct internet access for security.

4. **Started and Verified the Machine**
   - Booted Metasploitable 3.
   - Logged in with default credentials (if applicable).
   - Performed initial enumeration from Kali (ping, Nmap scan, service discovery).

5. **Took Initial Snapshot**
   - Created a clean snapshot in VirtualBox before any attacks.

## Screenshots
*(Insert your screenshots here)*
- Download / setup process
- Import into VirtualBox
- Network adapter settings
- Metasploitable 3 running (login screen or desktop/services)
- Nmap scan results from Kali showing open ports/services
- Snapshot creation

## Challenges & Troubleshooting
- Larger file size and longer import time compared to Metasploitable 2.
- Vagrant-related setup steps (if used).
- Network connectivity issues between Kali and the target.
- Resource allocation (Metasploitable 3 can be heavier on RAM/CPU).

## Key Learnings
- Difference between Metasploitable 2 and 3 (more realistic services and vulnerabilities).
- Working with more complex vulnerable VMs.
- Importance of snapshots for lab safety and repeatability.
- Basic service enumeration on modern vulnerable targets.

## Skills Demonstrated
- Advanced VM deployment in VirtualBox
- Handling resource-intensive lab targets
- Network segmentation consistency across multiple machines
- Initial reconnaissance preparation
- Lab management best practices (snapshots, isolation)

## Next Steps / Ideas to Extend
- Perform full Nmap service/version scan.
- Start exploring specific vulnerabilities (e.g., using Metasploit).
- Compare attack surface with Metasploitable 2.
- Document IP addresses and services for future reference.

## Useful Links

---

**Documented by**: [Your Name]  
**Date**: [Today's Date]  
**Status**: Completed
