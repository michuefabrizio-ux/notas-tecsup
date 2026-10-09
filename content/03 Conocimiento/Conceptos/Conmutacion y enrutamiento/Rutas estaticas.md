---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Protocolos de Enrutamiento]]"]
aliases: ["Rutas estáticas", "Ruta flotante", "Ruta predeterminada"]
tags: []
---

# Rutas estáticas

## Tipos

| Tipo | Ejemplo |
|---|---|
| Siguiente salto | `ip route 192.168.2.0 255.255.255.0 10.1.1.2` |
| Interfaz de salida | `ip route 192.168.2.0 255.255.255.0 s0/1/0` |
| Completamente especificada | `ip route 192.168.2.0 255.255.255.0 g0/0/1 10.1.1.2` |
| Predeterminada | `ip route 0.0.0.0 0.0.0.0 10.1.1.2` · `ipv6 route ::/0 2001:db8::2` |
| **Flotante** | `ip route 0.0.0.0 0.0.0.0 10.2.2.2 5` (AD mayor = respaldo) |

- Distancia administrativa: estática 1, EIGRP 90, OSPF 110, RIP 120.
- En IPv6 hay que activar `ipv6 unicast-routing`.

## Dónde lo usé

- [[PRE Lab 13 - Rutas estaticas IPv4 e IPv6]]

## Relacionado

- [[OSPF]] · [[EIGRP]] · [[IPv6]]
