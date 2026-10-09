---
tipo: clase
curso: "[[Ethical Hacking]]"
ciclo: 4
periodo: 2026-2
semana:
fecha:
estado: entregado
calificacion:
aliases: []
tags: [curso/ethical-hacking]
---

# EH U06 — Sniffing

← MOC del curso: [[Ethical Hacking]] · Fuente: `Material/U06 - Sniffing.pptx`

## Tema de la sesión

- Captura de tráfico, técnicas de sniffing activo y contramedidas.

## Lo esencial

- **Sniffing**: capturar los paquetes que circulan por la red; sirve para atacar o para monitoreo forense.
- Formas de acceso al tráfico: **Network TAP**, **SPAN / port mirror**, IDS.
- Con **hub** todo el tráfico llega a todos (fácil); con **switch** solo llega lo que va a tu MAC.
- La NIC debe estar en **modo promiscuo**.
- **Pasivo** (hub, no inyecta) vs. **activo** (switch: ARP spoofing, MAC flooding sobre la tabla CAM, DNS spoofing).
- Protocolos en texto plano expuestos: FTP, Telnet, correo, syslog, DNS, credenciales web.

## Conceptos, comandos y normas vistos

- [[Sniffing y ARP spoofing]] · [[Wireshark]] · [[tcpdump]] · [[ARP]]
