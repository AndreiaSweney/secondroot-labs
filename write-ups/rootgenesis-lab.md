# RootGenesis Lab Setup

**Author:** Andreia Sweeney

**Repo:** [secondroot-labs](https://github.com/AndreiaSweney/secondroot-labs.git)

**Purpose:** Documenting the architecture, setup, and early-stage issues of my home cybersecurity lab.



## Objective

To build a virtual home lab for practical cybersecurity training, including offensice (red team) and defensive (blue team) techniques. This lab supports my learning goals around SOC analyst
workflows, threat detection, and ethical hacking. Starting from foundational tools and progressing toward more complex simulations.

## Host Machine Specs

| Component    | Details                   |
|--------------|---------------------------|
| Device       | Lenovo ThinkPad T14 Gen 2 |
| CPU          | Intel Core i7-1165G7      |
| RAM          | 16 GB                     |
| Storage      | 512 GB SSD                |
| Host OS      | Windows 10 Pro            |
| Hypervisor   | VirtualBox (v7.x)         |

## Tools Used

| Tool              | Purpose                                      |
|-------------------|----------------------------------------------|
| Kali Linux VM     | Offensive security, penetration testing      |
| Security Onion VM | Network traffic analysis, blue team training |
| Windows 10 VM     | Target machine for simulated attacks         |
| Wireshark         | Packet capture and network analysis          |
| Hack The Box      | Hands-on labs for red team concepts          |
| TryHackMe         | Guided labs and cybersecurity fundamentals   |
| WSL2 (Backup)     | Lightweight Linux alternative when needed    |
| GitHub            | Documentation and version control            |

## Network & VM Configuration 

**Kali Linux**:
- Internet access: NAT adapter
- Internal communication: Host-only adapter

 **Security Onion**:
 - Still in resource tuning phase (stability testing)

**Windows 10**: 
- ISO downloaded, configuration pending

**WSL2**: 
- Used as a fallback test environment of VM fails

## Issues Encountered 

### VT-x Not Enabled (VirtualBox) 
**Error**: Kali VM failed to boot with "VT-x not available"

**Fix**: Enabled virtualization in BIOS

➔ ThinkPad: F1 on boot ➔ Security tab ➔ Enable Intel VT-x

---

### Network Conflicts
**Issue**: Bridged adapter caused inconsistent wi-fi access

**Fix**: 
- **NAT Adapter** for Internet
- **Host-only Adapter** for internal VM communication

---
### Storage Constraints

**Issues**: Downloading multiple ISOs consumed most of SSD
**Fix**: 
- Cleared unnecessary files
- Resized VM disks for better allocation
- Future Plan: External drive for snapshots and backups

---

## Current Status 

| Component      | Status      | Notes                           |
|----------------|-------------|---------------------------------|
| Kali Linux     | Running     | HTB modules tested              |
| Security Onion | Configuring | Resource tuning ongoing         |
| Windows 10     | Pending     | ISO ready, not deployed         | 
| Networking     | Stable      | Dual adapter config in place    |
| WSL2           | Backup Only | Used when VM instability occurs |


## Next Steps

- Finalize and deploy Security Onion VM
- Configure Windows 10 target VM
- Run internal attacks from Kali → Windows
- Test alerting/detection with Security Onion
- Build automation with Python for log triage
- Add diagram of VM network architecture

## Repo Structure Reference

```plaintext
secondroot-labs/
|-- htb/
|-- notes-secplus/
|-- tryhackme/
|-- write-ups/
|   |__ rootgenesis-lab.md (this file)
|__ README.md

```





