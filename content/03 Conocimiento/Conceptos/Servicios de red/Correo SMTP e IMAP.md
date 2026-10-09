---
tipo: concepto
categoria: Servicios de red
cursos: ["[[Servicios de Red]]"]
aliases: [SMTP, IMAP, POP3, MTA, MDA]
tags: []
---

# Correo: SMTP e IMAP

## Qué es

- El correo se apoya en un **MUA** (cliente: Thunderbird, Outlook, webmail), un **MTA** (transporte: Postfix) y un **MDA** (entrega al buzón: Dovecot).

## Cómo funciona

1. El MUA envía al MTA por **SMTP**.
2. Si el destino es local, el MTA lo entrega al MDA; si no, consulta el **registro MX** del dominio destino y lo reenvía.
3. El MDA guarda el correo en el buzón (Maildir o mbox).
4. El destinatario lo lee por **IMAP** (queda en el servidor) o **POP3** (se descarga).

## Puertos

| Protocolo | Puerto | Seguro |
|---|---|---|
| SMTP (MTA↔MTA) | 25 | STARTTLS |
| Submission (cliente) | 587 | STARTTLS + SASL |
| IMAP | 143 | 993 (IMAPS) |
| POP3 | 110 | 995 (POP3S) |

## Comparación

| Aspecto | IMAP | POP3 |
|---|---|---|
| Correos | Quedan en el servidor | Se descargan |
| Varios dispositivos | Sí, sincronizado | No recomendado |

## Dónde lo usé

- [[SRD GLAB-S04 - Servicio de Correo]] · [[SRD GLAB-S05 - DNS Web FTP y Correo]] · [[SRD PC3 - Servicios en RHEL]]

## Relacionado

- [[Postfix y Dovecot]] · [[DNS zona directa e inversa]]
