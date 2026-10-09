---
tipo: evaluacion
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana:
fecha:
estado: entregado
calificacion:
aliases: ["Práctica Calificada 3"]
tags: [curso/servicios-red]
---

# SRD PC3 — Servicios en RHEL (entorno híbrido)

← MOC del curso: [[Servicios de Red]] · Entrega: `entrega/Práctica_Calificada_3_LABORATORIO_desarrollado (1).docx`

## Escenario

- "AndinaTech S.A.", red 192.168.50.0/24: SRV-LINUX-01 (RHEL 10, .10) con DNS, FTP, correo y Apache; SRV-WIN-01 (Windows Server, .20) con IIS.

| Configuración | Valor |
|---|---|
| Hostname | srv-linux.andinatech.lab |
| Interfaz | enp0s3 |
| IP / Gateway | 192.168.50.10/24 · 192.168.50.1 |
| DNS | 192.168.50.10 (primario) · 8.8.8.8 (secundario) |

| Servicio | Puertos |
|---|---|
| DNS (BIND9) | TCP/UDP 53 |
| Web Apache / IIS | TCP 80, 443 |
| MariaDB | TCP 3306 |
| FTP (vsftpd) | TCP 21, 20, 55000-55999 |
| Correo (Postfix/Dovecot) | TCP 25, 143, 993, 587 |

## Conclusiones (de mi entrega)

- Enjaular usuarios FTP y darles `/sbin/nologin` mejora la seguridad, pero hay que revisar cómo PAM valida los shells.
- Validar antes de reiniciar (`named-checkconf`, `postfix check`, `doveconf -n`) evita caídas.
- Windows Server usó el DNS y el FTP del servidor Linux: los protocolos estándar son independientes del sistema operativo.

## Relacionado

- [[DNS zona directa e inversa]] · [[FTP activo y pasivo]] · [[Correo SMTP e IMAP]]
