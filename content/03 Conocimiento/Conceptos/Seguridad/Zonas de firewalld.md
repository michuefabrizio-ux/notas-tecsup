---
tipo: concepto
categoria: Seguridad
cursos: ["[[Servicios de Red]]"]
aliases: ["Zonas firewalld"]
tags: []
---

# Zonas de firewalld

## Qué es

- En **firewalld** cada interfaz se asigna a una **zona**; la zona define qué tráfico entrante se permite según el nivel de confianza.

## Cómo funciona

| Zona | Confianza | Comportamiento |
|---|---|---|
| drop | Mínima | Descarta sin responder (ideal para *deny-all*) |
| block | Mínima | Rechaza con ICMP |
| public | Baja | Por defecto; solo servicios elegidos |
| external | Media | Interfaces externas con NAT |
| dmz | Media | Servidores públicos |
| work / home | Alta | Redes de confianza |
| internal | Alta | Red interna |
| trusted | Total | Acepta todo |

- **Runtime** se pierde al recargar; **permanent** persiste. Usar `--permanent` + `--reload` o `--runtime-to-permanent`.
- Arquitectura en RHEL 10: `firewall-cmd` → `firewalld` → **nftables** → netfilter.
- NAT: `--add-masquerade` (SNAT) y `--add-forward-port` (DNAT).

## Dónde lo usé

- [[SRD S07 - Servicio Firewall]] · [[SRD PC1 - DNS autoritativo en RHEL]] · [[SRD PC2 - DNS Web y FTP en RHEL]]

## Relacionado

- [[firewalld]] · [[Cadenas de iptables]] · [[DMZ]] · [[OE4 - Bastionado del portal web]]
