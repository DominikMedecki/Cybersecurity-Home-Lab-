# 02 - Deploying Metasploitable 2

**Playlist Video**: [CyberSecurity Home Lab for Beginners #2](https://www.youtube.com/watch?v=_7MvHeoP_V8)

## Overview
In this video we deploy **Metasploitable 2**, a deliberately vulnerable Linux machine created by Rapid7. It serves as our primary target for practicing reconnaissance, exploitation, and post-exploitation in the lab.

This is a key component of the home lab — it allows us to safely simulate real-world vulnerabilities without risking production systems.

## Objectives
- Download the Metasploitable 2 virtual machine image.
- Import it into VirtualBox.
- Configure networking so it sits on the isolated vulnerable network.
- Verify the machine boots and is reachable from Kali.

## What I Did (Step-by-Step)

1. **Downloaded Metasploitable 2**
   - Obtained the official `.zip` file containing the VM from a trusted source (usually Rapid7 or mirrored on VulnHub).

2. **Extracted the Files**
   - Used 7-Zip (or built-in Windows tools) to extract the archive.

3. **Imported into VirtualBox**
   - Opened VirtualBox → File → Import Appliance.
   - Selected the `.ova` or `.vmx` files and followed the import wizard.
   - Adjusted settings (RAM, CPU, storage) as recommended.

4. **Configured Networking**
   - Set the network adapter to the internal / host-only network created in Video #1 (`Vone-Labs` or similar).
   - Ensured it does **not** have internet access (for isolation).

5. **Started the VM**
   - Booted Metasploitable 2.
   - Logged in with default credentials (`msfadmin` / `msfadmin`).

6. **Verified Connectivity**
   - From Kali Linux: Used `ping`, `nmap`, or `arp` to confirm the Metasploitable 2 machine was reachable on the lab network.

## Screenshots
*(Add your screenshots here — you mentioned you took many, great job!)*

- Download / extraction process
- Import Appliance wizard in VirtualBox
- VM Settings (especially Network Adapter)
- Metasploitable 2 login screen
- `ifconfig` or `ip addr` output on the target
- Kali scanning/discovering the target (e.g. `nmap -sP` or full scan)

## Challenges & Troubleshooting
- File extraction issues with large zips.
- Network adapter not connecting properly (make sure cable is connected in settings).
- IP address conflicts or DHCP not assigning properly.
- Adjusting VM resources for better performance.

## Key Learnings
- How to import pre-built vulnerable VMs into VirtualBox.
- Importance of proper network segmentation (target should not reach the internet).
- Default credentials and basic enumeration of vulnerable systems.
- Safe environment setup for ethical hacking practice.

## Skills Demonstrated
- Working with pre-configured vulnerable machines
- Virtual machine import and configuration
- Network isolation techniques
- Basic Linux target enumeration
- Lab hygiene and safety practices

## Next Steps / Ideas to Extend
- Run initial reconnaissance with Nmap from Kali.
- Take a clean snapshot before starting any attacks.
- Document the IP address scheme for this machine.
- Prepare for Metasploitable 3 in a future video.

## Useful Links
- Metasploitable 2 (usually via VulnHub or Rapid7 archives)
- Previous Video (VirtualBox + Networks): [Video #1](../01-Setup-VirtualBox-Networks-Kali)

---

**Documented by**: [Your Name]  
**Date**: [Today's Date]  
**Status**: Completed
