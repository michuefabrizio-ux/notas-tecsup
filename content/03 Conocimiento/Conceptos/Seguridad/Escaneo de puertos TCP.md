---
tipo: concepto
categoria: Seguridad
cursos: ["[[Ethical Hacking]]"]
aliases: ["Port scanning", "Host discovery"]
tags: []
---

# Escaneo de puertos TCP

## Qué es

- Técnica para saber qué **puertos** están abiertos en un host, qué **servicio** y **versión** corren y, a veces, el **sistema operativo**.

## Cómo funciona

- Se apoya en el *three-way handshake*: SYN → SYN/ACK → ACK.
- Estados que reporta nmap: `open`, `closed`, `filtered`.

| Tipo | Opción nmap | Cómo trabaja | Característica |
|---|---|---|---|
| TCP Connect / full open | `-sT` | Completa el handshake | Confiable, deja registro |
| SYN / half-open / stealth | `-sS` | SYN → SYN/ACK → RST | Rápido, más sigiloso (requiere root) |
| UDP | `-sU` | Envía datagramas UDP | Lento, útil para NetBIOS/SNMP |

- Antes del escaneo de puertos va el **host discovery** (`ping`, `arp-scan`, `netdiscover`, `nmap -sn`). En la red local, ARP es lo más preciso.

## Dónde lo usé

- [[EH Lab02 - Escaneo de redes]] · [[EH Lab03 - Enumeracion]]

## Relacionado

- [[Nmap]] · [[TCP vs UDP]] · [[Fases del hacking etico]]
