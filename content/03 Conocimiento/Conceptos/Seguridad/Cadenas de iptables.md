---
tipo: concepto
categoria: Seguridad
cursos: ["[[Servicios de Red]]"]
aliases: [netfilter]
tags: []
---

# Cadenas de iptables

## Qué es

- **iptables** organiza las reglas de filtrado de netfilter en **tablas** y **cadenas**.

## Cómo funciona

| Cadena | Tráfico |
|---|---|
| INPUT | Paquetes dirigidos al propio equipo |
| OUTPUT | Paquetes que genera el equipo |
| FORWARD | Paquetes que atraviesan el equipo (router/firewall) |

- Cada cadena tiene una **política por defecto** (ACCEPT o DROP). Lo seguro: DROP y permitir solo lo necesario.
- Las reglas se evalúan **en orden**; aplica la **primera** que coincide.
- Filtros comunes: `-s` (origen), `-p` (protocolo), `--dport` (puerto destino), `-i` (interfaz).
- Las reglas no son permanentes: guardar con `iptables-save` o `iptables-persistent`.
- En RHEL 10 iptables está deprecado; se usa nftables vía firewalld.

## Dónde lo usé

- [[SRD GLAB-S07 - Firewall iptables]]

## Relacionado

- [[iptables]] · [[Politicas DROP vs REJECT]] · [[Zonas de firewalld]]
