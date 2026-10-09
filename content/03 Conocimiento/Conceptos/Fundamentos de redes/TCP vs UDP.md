---
tipo: concepto
categoria: Fundamentos de redes
cursos: ["[[Implementacion de Redes]]"]
aliases: [TCP, UDP, Puertos]
tags: []
---

# TCP vs UDP

## Comparación

| Aspecto | TCP | UDP |
|---|---|---|
| Conexión | Orientado a conexión (*three-way handshake*) | Sin conexión |
| Confiabilidad | Acuses, retransmisión, orden | No garantiza entrega |
| Control de flujo | Ventana deslizante | No |
| Encabezado | 20 bytes | 8 bytes |
| Uso | Web, correo, FTP, SSH | DNS, DHCP, VoIP, video, TFTP |

## Puertos comunes

| Puerto | Servicio |
|---|---|
| 20/21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS (UDP y TCP) |
| 67/68 | DHCP |
| 80 / 443 | HTTP / HTTPS |
| 110 / 143 | POP3 / IMAP |

## Relacionado

- [[Modelo TCP-IP]] · [[Escaneo de puertos TCP]]
