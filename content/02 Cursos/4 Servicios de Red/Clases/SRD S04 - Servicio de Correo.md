---
tipo: clase
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 4
fecha: 2026-09-09
estado: entregado
calificacion:
aliases: []
tags: [curso/servicios-red]
---

# SRD S04 — Servicio de Correo

← MOC del curso: [[Servicios de Red]] · Fuente: `Material/PPT-S04-ACUEVA-2026-02.pptx`, `Material/MTP-S04-ACUEVA-2026-02.docx`, `Material/04 Servicio de Correo.pdf`

## Tema de la sesión

- Servidor de correo con **Postfix** (MTA) y **Dovecot** (MDA, IMAP/POP3) en RHEL 10.

## Lo esencial

- Componentes: servidor de correo, cliente (MUA: Thunderbird, Outlook, webmail) y protocolos.
- Flujo: MUA → (SMTP) → **MTA Postfix** → si es local, **MDA Dovecot** lo guarda en el buzón → el usuario lo lee por **IMAP** o **POP3**.
- **SMTP** envía (cliente→servidor y servidor→servidor); para otro dominio se consulta el registro **MX** del DNS destino (con prioridad).
- **IMAP** mantiene los correos en el servidor (ideal para varios dispositivos); **POP3** los descarga.
- Puerto **587 (submission)** con autenticación **SASL** para clientes; el 25 queda para MTA↔MTA.
- En RHEL 10 Sendmail fue eliminado; Postfix es el MTA soportado.

## Conceptos, comandos y normas vistos

- [[Correo SMTP e IMAP]] · [[Postfix y Dovecot]] · [[DNS zona directa e inversa]]
