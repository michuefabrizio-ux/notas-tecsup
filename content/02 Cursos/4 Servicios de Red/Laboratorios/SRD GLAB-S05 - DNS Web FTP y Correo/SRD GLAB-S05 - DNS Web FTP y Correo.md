---
tipo: laboratorio
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 5
fecha: 2026-09-21
estado: entregado
calificacion:
aliases: ["Integración de Servicios de Internet en Entornos Híbridos"]
tags: [curso/servicios-red]
---

# SRD GLAB-S05 — DNS, Web, FTP y Correo (integración híbrida)

← MOC del curso: [[Servicios de Red]] · Clase: [[SRD S05 - Integracion de servicios en Windows y Linux]] · Entrega: `entrega/GLAB-S05-ACUEVA-2026-02_Michue.docx`

## Objetivo

- Integrar DNS, Web, FTP y Correo (con cliente web) para la empresa "ARC", consumidos desde un cliente Windows.

## Direccionamiento y equipos

| Dispositivo | Nombre | IP | Máscara | DNS |
|---|---|---|---|---|
| Servidor DNS | smichue · ns1.arc01.xyz | 10.160.10.130 | 255.255.255.0 | 127.0.0.1 |

> Resto de la tabla en el informe #pendiente/verificar

## Procedimiento

1. DNS para `arc01.xyz` (registros A, MX, alias `ftp`, `mail`).
2. Sitio web por nombre y servidor FTP (`ftp.arc01.xyz`).
3. Correo Postfix + Dovecot con webmail **Rainloop** (IMAP 143, SMTP 25).
4. Prueba: correo de `sebastian.michue@arc01.xyz` al alias `ventas@arc01.xyz`, entregado en mi Maildir por `/etc/aliases`.
5. Pruebas desde Windows con `nslookup`, `ftp` y el navegador.

> Comandos usados: [[BIND9]] · [[Apache httpd]] · [[vsftpd]] · [[Postfix y Dovecot]]

## Problemas que tuve y cómo los resolví

| Problema | Causa | Solución |
|---|---|---|
| Alta de dominio en Rainloop con `rc01.xyz` | Error de digitación (queda en la Captura 42) | Usar el dominio válido `arc01.xyz` (Captura 40) |

## Conclusiones (del informe)

- El DNS es la base: Virtual Hosts, FTP y MX solo funcionaron tras validar la resolución.
- Consolidar todo en un servidor simplifica, pero crea un punto único de falla (ej.: PAM afecta a vsftpd y al sistema).
- Todo funcionó sin cifrado; siguiente paso: HTTPS, FTPS, IMAPS y 587 con SASL.

## Relacionado

- [[DNS zona directa e inversa]] · [[Correo SMTP e IMAP]] · [[FTP activo y pasivo]] · [[SPOF]]
