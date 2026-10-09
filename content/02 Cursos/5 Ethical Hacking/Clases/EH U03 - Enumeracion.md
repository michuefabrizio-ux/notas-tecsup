---
tipo: clase
curso: "[[Ethical Hacking]]"
ciclo: 4
periodo: 2026-2
semana:
fecha:
estado: entregado
calificacion:
aliases: ["EH U03 - Enumeración"]
tags: [curso/ethical-hacking]
---

# EH U03 — Enumeración

← MOC del curso: [[Ethical Hacking]] · Fuente: `Material/U03 - Enumeracion.pptx`

## Tema de la sesión

- Extracción activa de usuarios, hosts, recursos compartidos y servicios.

## Lo esencial

- **Enumeración**: el atacante crea conexiones activas y hace consultas directas; normalmente en la red interna. Objetivo: vulnerabilidades para explotar después.
- **NetBIOS** (UDP 137/138, TCP 139): equipos del dominio/grupo, recursos compartidos, políticas. Herramientas: `nbtstat -a` (Windows), `nbtscan`, `nmblookup`.
- **RPC en Unix/Linux**: `nmap -sR`, `rpcinfo -p`.
- **Contraseñas por defecto**: cirt.net/passwords.
- **SNMP** (UDP): *community string* **public** (lectura) y **private** (lectura/escritura). Herramientas: `snmpwalk`, `snmpget`, `snmpset`, `snmp-check`.

## Conceptos, comandos y normas vistos

- [[Enumeracion de servicios]] · [[Nmap]] · [[Nessus]]
