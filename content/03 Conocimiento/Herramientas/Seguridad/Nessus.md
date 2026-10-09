---
tipo: herramienta
categoria: Seguridad
cursos: ["[[Ethical Hacking]]"]
aliases: ["Nessus Essentials"]
tags: []
---

# Nessus

## Qué es

- Escáner de vulnerabilidades de Tenable. **Nessus Essentials** es la versión gratuita educativa.

## Instalación (guía del curso)

1. Registrarse con el correo de Tecsup y recibir el **código de activación**.
2. Copiar el `.deb` a Kali e instalarlo (`sudo dpkg -i Nessus-*.deb`).
3. Iniciar el servicio (`sudo systemctl start nessusd`) y entrar a `https://kali:8834`.
4. Aceptar el certificado autofirmado, elegir *Nessus Essentials*, ingresar el código y crear el usuario.

## Para qué la usé

- *Basic Network Scan* a Metasploitable2, Kioptrix y Symfonos en [[EH Lab03 - Enumeracion]].

## Relacionado

- [[Gestion de vulnerabilidades]] · [[CVE y CVSS]] · [[OpenVAS]]
