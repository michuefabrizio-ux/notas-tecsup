---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Protocolos de Enrutamiento]]", "[[Redes Escalables]]"]
aliases: [VLANs]
tags: []
---

# VLAN

## Qué es

- Red LAN **lógica** dentro de un switch: cada VLAN es un **dominio de difusión** separado, sin importar la ubicación física.

## Tipos

| Tipo | Uso |
|---|---|
| Datos | Tráfico de usuarios |
| Predeterminada (VLAN 1) | Todos los puertos al inicio |
| Nativa | Tráfico sin etiqueta en el troncal |
| Administración | SVI para gestionar el switch |
| Voz | Telefonía IP con QoS |

- Rango normal 1–1005 (en `vlan.dat`); extendido 1006–4094.
- Buena práctica: puertos sin uso en una VLAN aislada (ej.: *ParkingLot*) y apagados.

## Dónde lo usé

- [[PRE Lab 03 - VLAN y trunking]] · Eje [[OE2 - VLAN ACL y DMZ]]

## Relacionado

- [[Enlace troncal y VLAN nativa]] · [[Enrutamiento inter-VLAN]] · [[IOS - VLAN y troncales]] · [[Dominio de difusion]]
