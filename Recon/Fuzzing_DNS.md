<h1 align="center">DNS Fuzzing Cheat Sheet </h1>

<p align="center">
  Comprehensive reference guide for DNS enumeration, subdomain brute-forcing, prioritization strategies, and execution commands.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Kali_Linux-111827?style=for-the-badge&logo=kalilinux&logoColor=00BFFF">
  <img src="https://img.shields.io/badge/Web_Security-111827?style=for-the-badge&logo=owasp&logoColor=00A4EF">
  <img src="https://img.shields.io/badge/Reconnaissance-Techniques-111827?style=for-the-badge&logoColor=FF003C">
  <img src="https://img.shields.io/badge/DNS-Brute_Forcing-111827?style=for-the-badge&logoColor=00FFFF">
  <img src="https://img.shields.io/badge/Type-CheatSheet-111827?style=for-the-badge&logoColor=00FFFF">
</p>


## Gobuster - DNS

```
gobuster dns -d objetivo.com -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt -t 50
```

```
gobuster dns -d objetivo.com -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-110000.txt -t 100
```

```
gobuster dns -d objetivo.com -w /usr/share/seclists/Discovery/DNS/combined_subdomains.txt -t 100
```

```
gobuster dns -d objetivo.com -w /usr/share/seclists/Discovery/DNS/bitquark-subdomains-top100000.txt -t 100
```

```
gobuster dns -d objetivo.com -w /usr/share/seclists/Discovery/DNS/shubs-subdomains.txt -t 100
```

```
gobuster dns -d objetivo.com -w /usr/share/seclists/Discovery/DNS/dns-Jhaddix.txt -t 100
```
