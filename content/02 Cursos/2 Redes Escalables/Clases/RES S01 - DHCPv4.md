---
tipo: clase
curso: "[[Redes Escalables]]"
ciclo: 4
periodo: 2026-2
semana: 1
fecha:
estado: entregado
calificacion:
aliases: []
tags: [curso/redes-escalables]
---

# RES S01 — DHCPv4

← MOC del curso: [[Redes Escalables]] · Fuente: `Material/PPT-S01-JURBINA-2026-1.pptx` (CCNA SRWE v7, módulo 7)

## Tema de la sesión

- Funcionamiento de DHCPv4 y configuración de un router Cisco como servidor y cliente DHCP.

## Lo esencial

- DHCPv4 entrega IP y parámetros de red en **arrendamiento** (*lease*), normalmente de 24 horas a una semana.
- Obtener lease: **DORA** — Discover → Offer → Request → Ack.
- Renovar: Request → Ack directo al servidor original.
- Configuración en IOS: excluir direcciones → crear pool → `network`, `default-router`, `dns-server`, `domain-name`, `lease`.
- Si el servidor está en otra red: `ip helper-address` (DHCP relay).

## Conceptos, comandos y normas vistos

- [[DHCP y DHCP relay]] · [[IOS - Configuracion basica de switch]] · [[Cisco Packet Tracer]]
