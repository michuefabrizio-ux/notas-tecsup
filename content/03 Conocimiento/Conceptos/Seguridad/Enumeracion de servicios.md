---
tipo: concepto
categoria: Seguridad
cursos: ["[[Ethical Hacking]]"]
aliases: ["Enumeración", NetBIOS, SNMP]
tags: []
---

# Enumeración de servicios

## Qué es

- Fase en la que el atacante se conecta activamente al sistema para extraer **usuarios, hosts, recursos compartidos y servicios**.

## Cómo funciona

| Técnica | Puertos | Herramientas |
|---|---|---|
| NetBIOS / SMB | UDP 137/138, TCP 139/445 | `nbtstat -a`, `nbtscan`, `nmblookup`, `enum4linux-ng`, NSE `smb-enum-shares` |
| RPC (Unix/Linux) | 111 | `rpcinfo -p`, `nmap -sR` |
| SNMP | UDP 161 | `snmpwalk`, `snmpget`, `snmpset`, `snmp-check` |
| Contraseñas por defecto | — | cirt.net/passwords |

- SNMP usa *community strings*: **public** (solo lectura) y **private** (lectura/escritura); dejarlas por defecto expone tablas ARP, rutas y configuración.

```bash
snmpwalk -v1 -c public 192.168.10.200
enum4linux-ng -A 10.0.126.129
```

## Dónde lo usé

- [[EH Lab03 - Enumeracion]]

## Relacionado

- [[Escaneo de puertos TCP]] · [[Gestion de vulnerabilidades]]
