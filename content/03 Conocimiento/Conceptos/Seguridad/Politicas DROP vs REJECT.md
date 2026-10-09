---
tipo: concepto
categoria: Seguridad
cursos: ["[[Servicios de Red]]"]
aliases: ["DROP vs REJECT"]
tags: []
---

# Políticas DROP vs REJECT

## Qué es

- Dos formas de bloquear un paquete en un firewall.

## Comparación

| Aspecto | DROP | REJECT |
|---|---|---|
| Respuesta al origen | Ninguna | Mensaje ICMP / TCP RST |
| Lo que ve el cliente | Se queda esperando (timeout) | Error inmediato |
| Uso | Cara a Internet, no revela nada | Red interna, diagnóstico más fácil |
| Equivalente firewalld | Zona `drop` | Zona `block` |

## Dónde lo usé

- [[SRD GLAB-S07 - Firewall iptables]]

## Relacionado

- [[Cadenas de iptables]] · [[Zonas de firewalld]]
