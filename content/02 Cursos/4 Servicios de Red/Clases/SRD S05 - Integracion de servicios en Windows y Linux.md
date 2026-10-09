---
tipo: clase
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 5
fecha:
estado: entregado
calificacion:
aliases: ["SRD S05 - Integración de servicios en Windows y Linux"]
tags: [curso/servicios-red]
---

# SRD S05 — Integración de servicios de Internet en Windows y Linux

← MOC del curso: [[Servicios de Red]] · Fuente: `Material/MTP-S05-ACUEVA-2026-02.docx`, `Material/05 Integración de Servicios de Internet en Windows y Linux.pdf` (el `PPT-S05` no se pudo abrir: archivo dañado)

## Tema de la sesión

- Infraestructura **híbrida**: RHEL 10 (DNS BIND9, FTP) + Windows Server (IIS, Exchange).

## Lo esencial

- Cada servicio va en la plataforma donde rinde mejor: DNS/FTP en RHEL, intranet IIS y correo Exchange en Windows Server.
- El **DNS es la base**: el registro A debe apuntar al IIS y el registro MX al servidor de correo; si fallan, falla todo lo demás.
- Seguridad perimetral cruzada: **firewalld** (zonas) en RHEL y **Windows Defender Firewall** (perfiles Domain/Private/Public) en Windows.
- PowerShell útil: `Install-WindowsFeature Web-Server`, `New-Website`, `New-NetFirewallRule`, `Test-NetConnection`, `Get-Service W3SVC`.

## Conceptos, comandos y normas vistos

- [[DNS zona directa e inversa]] · [[Servidor web y VirtualHost]] · [[FTP activo y pasivo]] · [[Correo SMTP e IMAP]] · [[Windows Server 2019-2022]]
