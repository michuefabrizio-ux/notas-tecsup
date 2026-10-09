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

# EH U02 — Escaneo de redes

← MOC del curso: [[Ethical Hacking]] · Fuente: `Material/U02 - Escaneo de Redes.pptx`, `Material/tcpdump-cheatsheet.pdf`

## Tema de la sesión

- Descubrimiento de hosts, escaneo de puertos, estrategia de escaneo, `xsltproc` y análisis de tráfico con `tcpdump`.

## Lo esencial

- El **escaneo** interactúa con la red objetivo para encontrar hosts vivos, puertos, servicios, SO y vulnerabilidades; completa el footprinting y define la **superficie de ataque**.
- **Host discovery**: `ping`, `hping3`, `arping`, `arp-scan`, `netdiscover`, `nmap -sn`.
- Reconocimiento de ruta: `tracert` (Windows) / `traceroute` (Linux).
- **Escaneo de puertos** con base en las flags TCP y el *three-way handshake*:
  - **TCP Connect** (`-sT`): conexión completa, confiable, deja registro.
  - **SYN / half-open** (`-sS`): más rápido y sigiloso.
- Opciones nmap: `-p`, `-p-`, `-sV`, `-O`, `-A`, `-Pn`, `-T0..5`, `-F`, `--top-ports`, salidas `-oN/-oX/-oG/-oA`.
- `xsltproc` convierte el XML de nmap a HTML.

## Conceptos, comandos y normas vistos

- [[Escaneo de puertos TCP]] · [[Nmap]] · [[tcpdump]] · [[Kali Linux]]
