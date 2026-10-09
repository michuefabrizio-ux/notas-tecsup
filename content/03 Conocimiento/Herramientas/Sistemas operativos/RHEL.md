---
tipo: herramienta
categoria: Sistemas operativos
cursos: ["[[Servicios de Red]]"]
aliases: ["Red Hat Enterprise Linux", "RHEL 10"]
tags: []
---

# RHEL (Red Hat Enterprise Linux)

## Qué es

- Distribución Linux empresarial. En Servicios de Red se usa **RHEL 10**: gestor de paquetes `dnf`, red con `nmcli`, firewall **firewalld/nftables** y **SELinux** *enforcing*.

## Cambios de RHEL 10 vistos en clase

- iptables deprecado y módulo `ip_tables` eliminado.
- `vsftpd` deprecado; Sendmail eliminado (se usa Postfix).
- `PermitRootLogin prohibit-password` por defecto en SSH.
- DNS sobre TLS como *Technology Preview*.

## Para qué la usé

- Prácticas calificadas: [[SRD PC1 - DNS autoritativo en RHEL]] · [[SRD PC2 - DNS Web y FTP en RHEL]] · [[SRD PC3 - Servicios en RHEL]]
- Base del portal del PI: [[OE4 - Bastionado del portal web]]
