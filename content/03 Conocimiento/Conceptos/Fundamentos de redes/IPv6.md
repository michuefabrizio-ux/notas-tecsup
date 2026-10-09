---
tipo: concepto
categoria: Fundamentos de redes
cursos: ["[[Implementacion de Redes]]", "[[Protocolos de Enrutamiento]]"]
aliases: []
tags: []
---

# IPv6

## Qué es

- Direcciones de **128 bits** en 8 grupos hexadecimales (hextetos).

## Reglas de abreviación

1. Quitar ceros a la izquierda de cada hexteto.
2. Reemplazar **una sola** secuencia de hextetos en cero por `::`.

- Ej.: `2001:0db8:0000:0000:0000:0000:0000:0001` → `2001:db8::1`.

## Tipos

| Tipo | Prefijo |
|---|---|
| Unicast global (GUA) | 2000::/3 |
| Link-local | FE80::/10 |
| Multicast | FF00::/8 |
| Loopback | ::1 |

- No hay broadcast; ARP se reemplaza por **ND** (ICMPv6).

## Dónde lo usé

- [[IMR M12 - Direccionamiento IPv6]] · [[PRE Lab 13 - Rutas estaticas IPv4 e IPv6]]

## Relacionado

- [[SLAAC y DHCPv6]] · [[Direccionamiento IPv4 y subredes]]
