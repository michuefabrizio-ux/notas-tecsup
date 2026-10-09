---
tipo: clase
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 3
fecha:
estado: entregado
calificacion:
aliases: []
tags: [curso/servicios-red]
---

# SRD S03 — Servicio FTP

← MOC del curso: [[Servicios de Red]] · Fuente: `Material/PPT-S03-ACUEVA-2026-02.pptx`, `Material/MTP-S03-ACUEVA-2026-02.docx`, `Material/03 Servicio FTP.pdf`

## Tema de la sesión

- Servidor **vsftpd** en RHEL 10: modos activo y pasivo, usuarios enjaulados y anónimos, SELinux y firewalld.

## Lo esencial

- Componentes: servidor FTP, sitio FTP (directorio publicado), cliente FTP y protocolos.
- FTP usa dos canales: **control (21)** y **datos** (20 en activo, puerto efímero en pasivo).
- **Activo**: el servidor se conecta al cliente (problema con firewalls). **Pasivo**: el cliente abre ambas conexiones (mejor detrás de firewall).
- Variantes seguras: **FTPS** (FTP + TLS, implícito o explícito) y **SFTP** (protocolo nuevo sobre SSH, no es "FTP sobre SSH").
- En RHEL 10 `vsftpd` está **deprecado**, aunque sigue disponible.
- `chroot_local_user=YES` enjaula a los usuarios en su home; con `chroot_list_enable` se arma la lista de excepciones.
- Hay que abrir el rango pasivo (`pasv_min_port`/`pasv_max_port`) en firewalld y activar booleanos SELinux (`ftpd_use_passive_mode`, `ftp_home_dir`).

## Conceptos, comandos y normas vistos

- [[FTP activo y pasivo]] · [[vsftpd]] · [[SELinux]] · [[firewalld]]

## Dudas y pendientes

- [ ] No hay entrega del GLAB-S03 en la exportación #pendiente/verificar
