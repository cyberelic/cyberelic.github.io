#### Welcome to cyberelic

This site focuses on my cyber security journey.

I am a dedicated cybersecurity enthusiast with a passion for safeguarding digital landscapes in an ever-evolving threat landscape. I thrive on the challenge of protecting organizations and individuals from cyber threats. Whether it's implementing robust security measures, conducting penetration testing, or staying up-to-date with the latest vulnerabilities, my mission is to fortify digital ecosystems and ensure data integrity.

---

Here is a small list of the cheat sheets i've been consistantly referring back to:

- [PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master)

- [Hacktricks](https://book.hacktricks.xyz/)

- [WADcoms](https://wadcoms.github.io/)

---

`ffuf -u http://<target>:<ip> /w wordlist.txt`

---

here is a simple script that i used while trying to bypass and upload filter.


```bash
for char in '%20' '%0a' '%00' '%0d0a' '/' '.\\' '.' '…' ':'; do
        for ext in '.php' '.phps' '.phar'; do
           echo "shell$char$ext.jpg" >> wordlist.txt
           echo "shell$ext$char.jpg" >> wordlist.txt
           echo "shell.jpg$char$ext" >> wordlist.txt
           echo "shell.jpg$ext$char" >> wordlist.txt
       done
done
```

Use Burp and throw this into intruder to get a shell.

---
#### Hackthebox Academy:

I've been progressing through the Pentester Path and im about %60 finished and its truly a good way to learn the neccessary tools and techniques. below are some of the badges awarded from the HTB academy.

[Arachnoid](https://academy.hackthebox.com/achievement/badge/2fd5f36b-9e12-11ee-bfb6-bea50ffe6cb4) - For completing the Web Attacks module

---

<script src="https://tryhackme.com/badge/101635"></script>
