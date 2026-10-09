---
tipo: concepto
categoria: Seguridad
cursos: ["[[Servicios de Red]]"]
aliases: ["SELinux contextos"]
tags: []
---

# SELinux: modos y contextos

## Qué es

- **SELinux** es un control de acceso obligatorio (**MAC**) del kernel: aunque los permisos POSIX lo permitan, un proceso solo accede a lo que su política autoriza.

## Cómo funciona

- **Modos**: `enforcing` (bloquea y registra), `permissive` (solo registra), `disabled`.
- Cada proceso corre en un **dominio** (ej.: `httpd_t`, `squid_t`) y cada archivo tiene un **tipo** o contexto.
- Los **booleanos** activan permisos puntuales (ej.: `ftpd_use_passive_mode`).
- Las denegaciones aparecen como **AVC** en `/var/log/audit/audit.log`.

| Servicio | Contexto / booleano |
|---|---|
| Apache | `httpd_sys_content_t`, `httpd_sys_rw_content_t`, `http_port_t` |
| FTP | `public_content_t`, `public_content_rw_t`, `ftp_home_dir` |
| BIND | `restorecon -Rv /var/named/` |
| Squid | `squid_connect_any`, `squid_use_tproxy` |
| Postfix / Dovecot | `postfix_local_write_mail_spool`, `dovecot_can_use_home_dirs` |
| NFS | `nfs_export_all_ro`, `nfs_export_all_rw` |

## Dónde lo usé

- [[SRD PC1 - DNS autoritativo en RHEL]] · [[SRD PC2 - DNS Web y FTP en RHEL]]

## Relacionado

- [[SELinux]] · [[Bastionado]] · [[OE4 - Bastionado del portal web]]
