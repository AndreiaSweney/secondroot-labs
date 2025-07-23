# Fawn – Hack The Box Write-Up

**Difficulty:** Easy  
**Category:** Starting Point  
**IP Address:** *[REDACTED]*  
**Date Completed:** July 22, 2025  
**Platform:** Hack The Box

## Summary

Fawn is a beginner-friendly box designed to teach the basics of enumerating and interacting with an FTP service. This was my second box, and I completed it without running into errors. I stayed focused, followed my process, and captured the flag.

---

## Tools & Commands Used

- `nmap`
- `ftp`
- `ls`, `cd`, `cat`



## Step-by-Step Walkthrough

### 1. Nmap Scan

First, I scanned the target to see what ports were open and what services were running:

```bash
nmap -sV -Pn <TARGET_IP>
```


### 2. FTP Login 

I connected using: 

```bash
ftp <TARGET_IP>
```
When promted, I used: 

- Username: `anonymous`
- Password: (just hit enter)

Login successful. 


### 3. Enumerating Files

Once inside the FTP environment, I ran: 

```bash
ls
```

I found a single file: `flag.txt`


### 4. Capturing the Flag 

I downloaded the flag: 

```bash
get flag.txt
```
Then exited FTP and viewed the file with:

```bash
cat flag.txt
```
**FLAG:** HTB{********REDACTED********}

### What I Learned 

- How to identify an open FTP service using `nmap`
- How to use anonymous login to gain access
- The importance of checking for easily accessible files in public facing services

### Notes to Self 
- Always check if anonymous login is enabled on FTP services
- Track commands during the process so the write-ups flow naturally
