## Welcome to cyberelic

this site focuses on my cyber security journey. its a place for me to write down walkthroughs of the [CTF's](https://en.wikipedia.org/wiki/Capture_the_flag_(cybersecurity)) I complete.


# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)

# Tryhackme - Anthem

this is an easy box from tryhackme.

```
sudo nmap -v -sS -A -T4 -p- 10.10.186.97 -Pn
```

Which returned the following results:

```
Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
Starting Nmap 7.92 ( https://nmap.org ) at 2022-07-11 14:01 CDT
NSE: Loaded 155 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 14:01
Completed NSE at 14:01, 0.00s elapsed
Initiating NSE at 14:01
Completed NSE at 14:01, 0.00s elapsed
Initiating NSE at 14:01
Completed NSE at 14:01, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 14:01
Completed Parallel DNS resolution of 1 host. at 14:01, 0.00s elapsed
Initiating SYN Stealth Scan at 14:01
Scanning 10.10.186.97 [65535 ports]
Discovered open port 3389/tcp on 10.10.186.97
Discovered open port 80/tcp on 10.10.186.97
SYN Stealth Scan Timing: About 10.15% done; ETC: 14:07 (0:04:34 remaining)
SYN Stealth Scan Timing: About 30.35% done; ETC: 14:05 (0:02:20 remaining)
SYN Stealth Scan Timing: About 43.95% done; ETC: 14:05 (0:01:56 remaining)
SYN Stealth Scan Timing: About 61.08% done; ETC: 14:06 (0:01:38 remaining)
SYN Stealth Scan Timing: About 80.17% done; ETC: 14:05 (0:00:46 remaining)
Completed SYN Stealth Scan at 14:06, 260.15s elapsed (65535 total ports)
Initiating Service scan at 14:06
Scanning 2 services on 10.10.186.97
Completed Service scan at 14:06, 16.80s elapsed (2 services on 1 host)
Initiating OS detection (try #1) against 10.10.186.97
adjust_timeouts2: packet supposedly had rtt of -101207 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -101207 microseconds.  Ignoring time.
Retrying OS detection (try #2) against 10.10.186.97
Initiating Traceroute at 14:06
Completed Traceroute at 14:06, 3.02s elapsed
Initiating Parallel DNS resolution of 2 hosts. at 14:06
Completed Parallel DNS resolution of 2 hosts. at 14:06, 0.00s elapsed
NSE: Script scanning 10.10.186.97.
Initiating NSE at 14:06
Completed NSE at 14:07, 69.50s elapsed
Initiating NSE at 14:07
Completed NSE at 14:08, 8.22s elapsed
Initiating NSE at 14:08
Completed NSE at 14:08, 0.00s elapsed
Nmap scan report for 10.10.186.97
Host is up (0.14s latency).
Not shown: 65533 filtered tcp ports (no-response)
PORT     STATE SERVICE       VERSION
80/tcp   open  http          Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
3389/tcp open  ms-wbt-server Microsoft Terminal Services
| rdp-ntlm-info: 
|   Target_Name: WIN-LU09299160F
|   NetBIOS_Domain_Name: WIN-LU09299160F
|   NetBIOS_Computer_Name: WIN-LU09299160F
|   DNS_Domain_Name: WIN-LU09299160F
|   DNS_Computer_Name: WIN-LU09299160F
|   Product_Version: 10.0.17763
|_  System_Time: 2022-07-11T19:06:46+00:00
|_ssl-date: 2022-07-11T19:07:54+00:00; 0s from scanner time.
| ssl-cert: Subject: commonName=WIN-LU09299160F
| Issuer: commonName=WIN-LU09299160F
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2022-07-10T18:37:00
| Not valid after:  2023-01-09T18:37:00
| MD5:   09c9 93d1 2dbb ccc1 5205 cde3 6b7d e101
|_SHA-1: 4a6d 2210 354b 84ef e955 cc9d e951 5cd7 e397 b8d4
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: specialized
Running (JUST GUESSING): AVtech embedded (85%)
Aggressive OS guesses: AVtech Room Alert 26W environmental monitor (85%)
No exact OS matches for host (test conditions non-ideal).
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=262 (Good luck!)
IP ID Sequence Generation: Busy server or unknown class
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

TRACEROUTE (using port 3389/tcp)
HOP RTT       ADDRESS
1   49.64 ms  10.6.0.1
2   ... 3
4   149.74 ms 10.10.186.97

NSE: Script Post-scanning.
Initiating NSE at 14:08
Completed NSE at 14:08, 0.00s elapsed
Initiating NSE at 14:08
Completed NSE at 14:08, 0.00s elapsed
Initiating NSE at 14:08
Completed NSE at 14:08, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 365.08 seconds
           Raw packets sent: 131352 (5.785MB) | Rcvd: 36451 (6.554MB)
```
           
           
second thing i ran was a nikto scan:
which gave the following results:
