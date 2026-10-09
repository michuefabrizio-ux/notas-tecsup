---
tipo: clase
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 8
fecha: 2026-10-06
estado: entregado
calificacion:
aliases: []
tags: [curso/servicios-red]
---

# SRD S08 — Acceso remoto seguro (OpenSSH) y NFSv4

← MOC del curso: [[Servicios de Red]] · Fuente: `Material/MTP-S08-ACUEVA-2026-02.docx`, `Material/08 Servicios de Acceso Remoto y NFS.pdf` (el `PPT-S08` no se pudo abrir: archivo dañado)

## Tema de la sesión

- Acceso remoto cifrado con **OpenSSH** (llaves) y almacenamiento compartido con **NFSv4**.

## Lo esencial

- **Telnet** (TCP 23) viaja en texto plano; **SSH** (TCP 22) cifra todo: negociación → autenticación → sesión con clave simétrica.
- Autenticación por llaves: pública en `~/.ssh/authorized_keys`, privada solo en el cliente; recomendado **Ed25519** (o ECDSA si se exige FIPS).
- RHEL 10 trae `PermitRootLogin prohibit-password` por defecto.
- **NFSv4** solo necesita el puerto **2049**, no depende de rpcbind y usa un pseudo-filesystem; admite Kerberos.
- Exportaciones en `/etc/exports` (`exportfs -ra`); en el cliente usar `_netdev` y `nofail` en `/etc/fstab`.
- Booleanos SELinux: `nfs_export_all_ro`, `nfs_export_all_rw`, `use_nfs_home_dirs`.

## Conceptos, comandos y normas vistos

- [[SSH con llave publica]] · [[NFSv4]] · [[SELinux]] · [[firewalld]]
