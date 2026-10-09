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

# EH U04 — Hacking de sistemas (Metasploit)

← MOC del curso: [[Ethical Hacking]] · Fuente: `Material/U04 - Hacking de sistemas.pptx`, `Material/U04-Metasploit-guia.pdf`

## Tema de la sesión

- Explotación de vulnerabilidades con el framework **Metasploit**.

## Lo esencial

- Recapitulación: fases → footprinting → escaneo de redes, de puertos y de **vulnerabilidades**.
- Exploits públicos: exploit-db.com; gestión centralizada con **Metasploit** (`msfconsole`).
- Flujo: identificar servicio vulnerable → buscar exploit → configurar exploit → configurar payload → ejecutar.
- Módulos: **exploits** (siempre usan payload), **auxiliary** (escáneres, fuzzers, sin payload), **payloads**. Ruta: `/usr/share/metasploit-framework/modules/`.
- Shell directa vs. **reverse shell**.
- Guía: Kali + Metasploitable2, `msfdb init`, workspaces, `db_nmap`, `hosts`, `services`, `db_export`/`db_import`.

## Conceptos, comandos y normas vistos

- [[Metasploit]] · [[Fases del hacking etico]] · [[CVE y CVSS]]
