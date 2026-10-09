---
tipo: concepto
categoria: Fundamentos de redes
cursos: ["[[Implementacion de Redes]]", "[[Protocolos de Enrutamiento]]"]
aliases: ["Dominio de difusión", "Dominio de colisión"]
tags: []
---

# Dominio de difusión

## Qué es

- Conjunto de dispositivos que reciben un **broadcast** de cualquiera de ellos.

## Comparación

| Dispositivo | Dominio de colisión | Dominio de difusión |
|---|---|---|
| Hub | Uno para todos | Uno |
| Switch | Uno por puerto | Uno por VLAN |
| Router | Uno por interfaz | Uno por interfaz (no reenvía broadcast) |

- Las **VLAN** y los **routers** dividen dominios de difusión.

## Relacionado

- [[VLAN]] · [[ARP]]
