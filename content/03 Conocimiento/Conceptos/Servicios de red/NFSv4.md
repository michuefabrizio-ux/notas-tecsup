---
tipo: concepto
categoria: Servicios de red
cursos: ["[[Servicios de Red]]"]
aliases: [NFS]
tags: []
---

# NFSv4

## Qué es

- **NFS** permite montar directorios remotos como si fueran locales. NFSv4 es la versión actual en RHEL 10.

## Cómo funciona

- El servidor exporta carpetas en `/etc/exports` y las publica con `exportfs -ra`.
- El cliente monta con `mount` o en `/etc/fstab` (usar `_netdev` y `nofail` para no colgar el arranque).
- `root_squash` (por defecto) convierte al root remoto en usuario sin privilegios.

## Comparación

| Aspecto | NFSv3 | NFSv4 |
|---|---|---|
| Puertos | Varios + rpcbind (111) | Solo TCP 2049 |
| Montaje | Protocolo MOUNT aparte | Integrado |
| Seguridad | AUTH_SYS (UID/GID) | Kerberos (krb5, krb5i, krb5p) |

## Dónde lo usé

- [[SRD S08 - Acceso remoto SSH y NFS]]

## Relacionado

- [[SAN y NAS]] · [[SELinux]]
