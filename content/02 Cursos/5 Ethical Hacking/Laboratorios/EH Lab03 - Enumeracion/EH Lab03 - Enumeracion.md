---
tipo: laboratorio
curso: "[[Ethical Hacking]]"
ciclo: 4
periodo: 2026-2
semana:
fecha:
estado: entregado
calificacion:
aliases: ["EH Lab03 - Enumeración"]
tags: [curso/ethical-hacking]
---

# EH Lab03 — Enumeración

← MOC del curso: [[Ethical Hacking]] · Clase: [[EH U03 - Enumeracion]] · Entrega: `entrega/Lab03 - Enumeracion (1).docx`, `entrega/Laboratorio_Seguridad_Redes_smichue.zip`

## Objetivo

- Enumerar infraestructura y servicios de red y analizar vulnerabilidades con Nessus.

## Direccionamiento y equipos

| Target | IP |
|---|---|
| Metasploitable2 | 10.0.126.129 |
| Symfonos | 10.0.126.130 |
| Kioptrix | 10.0.126.131 |

## Procedimiento

1. Descubrimiento de red con `arp-scan` y `netdiscover` (10.0.126.0/24).
2. Escaneo SYN TCP de cada target y escaneo UDP (NetBIOS 137/138).
3. Scripts NSE: `smb-enum-shares`, `smb-os-discovery`, `nbstat.nse`; depuración con `-d`.
4. `enum4linux-ng -A <ip>` en los tres targets.
5. Instalar **Nessus Essentials** offline en Kali y correr *Basic Network Scan*.

> Comandos usados: [[Nmap]] · Herramienta: [[Nessus]]

## Conclusiones (del informe)

- ARP (`arp-scan`, `netdiscover`) fue el método más preciso en la subred local porque trabaja en capa 2.
- Los tres targets exponen SMB/NetBIOS (UDP 137/138, TCP 139/445) y revelan nombres y grupos de trabajo.
- NSE da un mapeo puntual; `enum4linux` automatiza la extracción de recursos, dominio y usuarios.
- Lo recolectado en reconocimiento se correlaciona con los hallazgos de Nessus.

## Relacionado

- [[Enumeracion de servicios]] · [[Gestion de vulnerabilidades]]
