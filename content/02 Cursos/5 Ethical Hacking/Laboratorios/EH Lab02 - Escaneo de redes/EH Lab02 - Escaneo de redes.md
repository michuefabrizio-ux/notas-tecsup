---
tipo: laboratorio
curso: "[[Ethical Hacking]]"
ciclo: 4
periodo: 2026-2
semana:
fecha: 2026-08-27
estado: entregado
calificacion:
aliases: []
tags: [curso/ethical-hacking]
---

# EH Lab02 — Escaneo de redes

← MOC del curso: [[Ethical Hacking]] · Clase: [[EH U02 - Escaneo de redes]] · Entrega: `entrega/Lab02 - EscaneodeRedes-SebastianMichue.docx`, `entrega/archivos_escritorio.zip`

## Objetivo

- Desplegar un entorno controlado y usar herramientas de descubrimiento de hosts y escaneo de puertos.

## Direccionamiento y equipos

- Windows 11 + VMware Workstation; VMs: Kali Linux 2026.2, Metasploitable2, Kioptrix Level 1, basic_pentesting_1, DC-1, Matrix, skydogctf.
- Dos redes: NAT y host-only (dirección asignada por el docente) #pendiente/verificar

## Procedimiento

1. Host discovery con una herramienta vista en clase.
2. Todos los puertos abiertos por host, salida normal (`-oN`).
3. Servicios y versiones por target, salida XML (`-oX`).
4. Un solo comando nmap por red: todos los puertos + versiones + SO, en XML.
5. `xsltproc` para pasar los XML a HTML.
6. Diagrama de red con IP y MAC de cada target y del Kali.

> Evidencias en el zip: `nmap_allports_*.txt`, `nmap_services_*.xml`, `red_hostonly_full.html`, `red_NAT_full.html`, `cap_puerto21_TCPconnect.pcap`, `cap_puerto22_SYN.pcap`.

> Comandos usados: [[Nmap]] · [[tcpdump]]

## Conclusiones

- La sección de conclusiones del informe está vacía #pendiente/verificar

## Relacionado

- [[Escaneo de puertos TCP]]
