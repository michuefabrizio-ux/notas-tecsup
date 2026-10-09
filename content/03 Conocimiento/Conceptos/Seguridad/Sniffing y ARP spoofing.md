---
tipo: concepto
categoria: Seguridad
cursos: ["[[Ethical Hacking]]", "[[Protocolos de Enrutamiento]]"]
aliases: [Sniffing, "ARP spoofing", "MAC flooding"]
tags: []
---

# Sniffing y ARP spoofing

## Qué es

- **Sniffing**: capturar y analizar los paquetes que circulan por la red.

## Cómo funciona

- La NIC debe estar en **modo promiscuo** para aceptar tramas que no son para ella.
- Acceso al tráfico: **TAP** de red, puerto **SPAN / mirror**, o atacando el switch.

| Tipo | Red | Técnica |
|---|---|---|
| Pasivo | Hub | Solo escucha; no inyecta paquetes |
| Activo | Switch | **MAC flooding** (llena la tabla CAM y el switch actúa como hub), **ARP spoofing** (respuestas ARP falsas para ponerse en medio), **DNS spoofing** |

- Pasos del atacante: conectarse al switch → descubrir la topología → elegir víctimas → ARP spoofing → desviar y capturar el tráfico.
- Contramedidas: port security, DHCP snooping + DAI, cifrado (SSH, HTTPS) en lugar de Telnet/FTP.

## Dónde lo usé

- [[EH U06 - Sniffing]]

## Relacionado

- [[ARP]] · [[Wireshark]] · [[tcpdump]]
