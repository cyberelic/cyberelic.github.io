## Welcome to cyberelic

this site focuses on my cyber security journey. its a place for me to write down walkthroughs of the [CTF's](https://en.wikipedia.org/wiki/Capture_the_flag_(cybersecurity)) I complete.


## Tryhackme - BruteIt

This is a box labled "easy" from [tryhackme.com/room/bruteit](https://www.tryhackme.com/room/bruteit)

### Task 1

how many ports are open?

```
$ sudo nmap -v -sS -A -T4 -p- 10.10.162.54

Starting Nmap 7.92 ( https://nmap.org ) at 2022-08-06 14:51 CDT
NSE: Loaded 155 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 14:51
Completed NSE at 14:51, 0.00s elapsed
Initiating NSE at 14:51
Completed NSE at 14:51, 0.00s elapsed
Initiating NSE at 14:51
Completed NSE at 14:51, 0.00s elapsed
Initiating Ping Scan at 14:51
Scanning 10.10.162.54 [4 ports]
Completed Ping Scan at 14:51, 0.21s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 14:51
Completed Parallel DNS resolution of 1 host. at 14:51, 0.00s elapsed
Initiating SYN Stealth Scan at 14:51
Scanning 10.10.162.54 [65535 ports]
Discovered open port 22/tcp on 10.10.162.54
Discovered open port 80/tcp on 10.10.162.54
Increasing send delay for 10.10.162.54 from 0 to 5 due to 1312 out of 3279 dropped probes since last increase.
Increasing send delay for 10.10.162.54 from 5 to 10 due to 11 out of 11 dropped probes since last increase.
SYN Stealth Scan Timing: About 6.33% done; ETC: 14:59 (0:07:39 remaining)
SYN Stealth Scan Timing: About 10.21% done; ETC: 15:01 (0:08:56 remaining)
SYN Stealth Scan Timing: About 27.38% done; ETC: 15:03 (0:08:24 remaining)
SYN Stealth Scan Timing: About 32.86% done; ETC: 15:03 (0:07:48 remaining)
SYN Stealth Scan Timing: About 39.05% done; ETC: 15:03 (0:07:12 remaining)
SYN Stealth Scan Timing: About 44.68% done; ETC: 15:03 (0:06:35 remaining)
SYN Stealth Scan Timing: About 49.97% done; ETC: 15:03 (0:05:58 remaining)
SYN Stealth Scan Timing: About 55.51% done; ETC: 15:03 (0:05:21 remaining)
SYN Stealth Scan Timing: About 60.78% done; ETC: 15:03 (0:04:43 remaining)
SYN Stealth Scan Timing: About 66.14% done; ETC: 15:03 (0:04:05 remaining)
SYN Stealth Scan Timing: About 71.28% done; ETC: 15:03 (0:03:28 remaining)
SYN Stealth Scan Timing: About 76.56% done; ETC: 15:03 (0:02:51 remaining)
SYN Stealth Scan Timing: About 81.75% done; ETC: 15:03 (0:02:14 remaining)
SYN Stealth Scan Timing: About 87.04% done; ETC: 15:03 (0:01:36 remaining)
SYN Stealth Scan Timing: About 92.23% done; ETC: 15:04 (0:00:58 remaining)
Completed SYN Stealth Scan at 15:04, 754.59s elapsed (65535 total ports)
Initiating Service scan at 15:04
Scanning 2 services on 10.10.162.54
Completed Service scan at 15:04, 6.34s elapsed (2 services on 1 host)
Initiating OS detection (try #1) against 10.10.162.54
Retrying OS detection (try #2) against 10.10.162.54
Retrying OS detection (try #3) against 10.10.162.54
Retrying OS detection (try #4) against 10.10.162.54
Retrying OS detection (try #5) against 10.10.162.54
Initiating Traceroute at 15:04
Completed Traceroute at 15:04, 3.02s elapsed
Initiating Parallel DNS resolution of 2 hosts. at 15:04
Completed Parallel DNS resolution of 2 hosts. at 15:04, 0.00s elapsed
NSE: Script scanning 10.10.162.54.
Initiating NSE at 15:04
Completed NSE at 15:04, 3.86s elapsed
Initiating NSE at 15:04
Completed NSE at 15:04, 0.48s elapsed
Initiating NSE at 15:04
Completed NSE at 15:04, 0.01s elapsed
Nmap scan report for 10.10.162.54
Host is up (0.11s latency).
Not shown: 65533 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 4b:0e:bf:14:fa:54:b3:5c:44:15:ed:b2:5d:a0:ac:8f (RSA)
|   256 d0:3a:81:55:13:5e:87:0c:e8:52:1e:cf:44:e0:3a:54 (ECDSA)
|_  256 da:ce:79:e0:45:eb:17:25:ef:62:ac:98:f0:cf:bb:04 (ED25519)
80/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
|_http-title: Apache2 Ubuntu Default Page: It works
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
|_http-server-header: Apache/2.4.29 (Ubuntu)
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.92%E=4%D=8/6%OT=22%CT=1%CU=41485%PV=Y%DS=4%DC=T%G=Y%TM=62EEC956
OS:%P=aarch64-unknown-linux-gnu)SEQ(SP=104%GCD=1%ISR=109%TI=Z%CI=Z%II=I%TS=
OS:A)OPS(O1=M506ST11NW6%O2=M506ST11NW6%O3=M506NNT11NW6%O4=M506ST11NW6%O5=M5
OS:06ST11NW6%O6=M506ST11)WIN(W1=F4B3%W2=F4B3%W3=F4B3%W4=F4B3%W5=F4B3%W6=F4B
OS:3)ECN(R=Y%DF=Y%T=40%W=F507%O=M506NNSNW6%CC=Y%Q=)T1(R=Y%DF=Y%T=40%S=O%A=S
OS:+%F=AS%RD=0%Q=)T2(R=N)T3(R=N)T4(R=Y%DF=Y%T=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=
OS:)T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=Y%DF=Y%T=40%W=0%S=A%
OS:A=Z%F=R%O=%RD=0%Q=)T7(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)U1(R=Y%
OS:DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=G%RUD=G)IE(R=Y%DFI=N%T=
OS:40%CD=S)

Uptime guess: 30.050 days (since Thu Jul  7 13:52:49 2022)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=260 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 5900/tcp)
HOP RTT       ADDRESS
1   46.95 ms  10.6.0.1
2   ... 3
4   115.89 ms 10.10.162.54

NSE: Script Post-scanning.
Initiating NSE at 15:04
Completed NSE at 15:04, 0.00s elapsed
Initiating NSE at 15:04
Completed NSE at 15:04, 0.00s elapsed
Initiating NSE at 15:04
Completed NSE at 15:04, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 781.43 seconds
           Raw packets sent: 68385 (3.013MB) | Rcvd: 66934 (2.681MB)
```
          
Ports **22** and **80** are open

Answer: 2


What verson of SSH is running?

Answer: OpenSSH 7.6p1


```

```

whats interesting here is the robots.txt that was found with intriguing entrys.
