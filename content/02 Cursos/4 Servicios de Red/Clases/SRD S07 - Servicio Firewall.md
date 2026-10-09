---
tipo: clase
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 7
fecha: 2026-09-27
estado: entregado
calificacion:
aliases: []
tags: [curso/servicios-red]
---

# SRD S07 — Servicio Firewall (firewalld + nftables)

← MOC del curso: [[Servicios de Red]] · Fuente: `Material/MTP-S07-ACUEVA-2026-02.docx`, `Material/07 Servicio Firewall.pdf` (el `PPT-S07` no se pudo abrir: archivo dañado)

## Tema de la sesión

- Cortafuegos en RHEL 10 con **firewalld** sobre **nftables**; en el laboratorio se trabajó con **iptables** en Ubuntu.

## Lo esencial

- Cadena: `firewall-cmd` → `firewalld` → **nftables** → netfilter (kernel). RHEL 10 eliminó el módulo `ip_tables`; iptables está deprecado.
- nftables: actualizaciones atómicas, un solo comando `nft`, conjuntos y mapas.
- **Zonas** por nivel de confianza: drop, block, public (por defecto), external, dmz, work, home, internal, trusted.
- **drop** descarta sin responder; **block** rechaza con ICMP.
- **Runtime vs. permanent**: lo runtime se pierde al recargar; usar `--permanent` + `--reload` o `--runtime-to-permanent`.
- NAT: masquerading (SNAT), port forwarding (DNAT) y redirect.

## Conceptos, comandos y normas vistos

- [[Zonas de firewalld]] · [[Cadenas de iptables]] · [[Politicas DROP vs REJECT]] · [[firewalld]] · [[iptables]] · [[Defensa en profundidad]]
