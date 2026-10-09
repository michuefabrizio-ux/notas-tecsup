---
tipo: concepto
categoria: Servicios de red
cursos: ["[[Servicios de Red]]"]
aliases: [FTP, FTPS, SFTP]
tags: []
---

# FTP activo y pasivo

## Qué es

- **FTP** transfiere archivos entre cliente y servidor usando dos canales: **control (TCP 21)** y **datos**.

## Cómo funciona

- **Activo**: el cliente envía `PORT`; el servidor abre la conexión de datos **desde su puerto 20** hacia el cliente. Lo bloquean los firewalls del cliente.
- **Pasivo**: el cliente envía `PASV`; el servidor responde con un puerto efímero (ej.: `227 Entering Passive Mode (192,168,1,10,39,40)` → puerto 39×256+40) y el **cliente abre** la conexión.
- En el servidor hay que fijar y abrir el rango pasivo (`pasv_min_port`, `pasv_max_port`).
- **Usuarios enjaulados (chroot)**: no pueden salir de su home. vsftpd exige que la raíz del chroot no sea escribible.
- **Anónimo**: acceso sin cuenta, normalmente solo lectura.

## Comparación

| Aspecto | Activo | Pasivo |
|---|---|---|
| Quién abre el canal de datos | Servidor (puerto 20) | Cliente |
| Firewall | Problemático | Más sencillo |

| Protocolo | Seguridad |
|---|---|
| FTP | Texto plano |
| FTPS | FTP + TLS (implícito o explícito) |
| SFTP | Protocolo distinto sobre SSH |

## Dónde lo usé

- [[SRD PC2 - DNS Web y FTP en RHEL]] · [[SRD GLAB-S05 - DNS Web FTP y Correo]] · [[SRD PC3 - Servicios en RHEL]]

## Relacionado

- [[vsftpd]] · [[SSH con llave publica]]
