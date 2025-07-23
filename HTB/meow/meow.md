# HTB Starting Point: Meow

**Difficulty**: Very Easy

**Category**: Starting Point

**Date Completed**: July 10,2025

**Platform**: Hack The Box 

**Skills Covered**: Nmap scanning, Telnet access, Linux navigation, flag capture


## Objective

Gain remote access to a Linux machine via Telnet and capture the user flag.  
This box is intentionally simple — the goal is to walk through the basics of enumeration and shell access.


## Tools Used

- Kali Linux (VirtualBox VM)
- Nmap
- Telnet
- Terminal + Common Linux commands (`ls`, `cat`, `cd`, `whoami`, etc.)


## Walkthrough

### 1. **Initial Nmap Scan**
```bash
nmap -sV -p- 10.129.1.XXX
```

Results: 

```bash
PORT     STATE SERVICE VERSION
23/tcp   open  telnet  Linux telnetd
```
Only port 23 (Telnet) is open. Very Old-school, and exactly what I expected for a beginnger box. 

### 2. **Connect via Telnet**

```bash
telnet 10.129.1.xxx
```
No login prompt. Telnet dropped me right into a shell. A nightmare in real life security, but a gift in training. 

### 3. Explore the System
```bash
whoami
```

Response
```bash
root
```
*Logged in as root by default.* Again, this would be terrifying in the wild, but for learning? Helpful.

### 4. Hunt for the Flag

I searched the file system: 
```bash
ls /root
```
Output:
```bash
flag.txt
```
Then captured the flag: 
```bash
cat /root/flag.txt
```

## Lessons Learned 

- Even outdated protocols like Telnet still show up in real environments. Knowing how they work matters.
- Never underestimate simple machines! They train your eyes to look for low hanging fruit
- Always check for open ports first. Enumeration is everything.

## Final Thoughts 

This was my first real step into hands-on ethical hacking. Nothing fancy. Just an honest walkthrough of me figuring it out one command at a time
