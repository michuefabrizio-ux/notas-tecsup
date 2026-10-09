---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Protocolos de Enrutamiento]]"]
aliases: [Trunk, "Troncal 802.1Q", DTP]
tags: []
---

# Enlace troncal y VLAN nativa

## Qué es

- Un **troncal** lleva varias VLAN por un solo enlace, marcando cada trama con una etiqueta **802.1Q** de 4 bytes.
- La **VLAN nativa** viaja **sin etiqueta**; debe coincidir en ambos extremos (si no: *native VLAN mismatch*).

## Buenas prácticas

- Troncal manual (`switchport mode trunk`) y `switchport nonegotiate` (sin DTP).
- Nativa distinta de la VLAN 1 y sin usuarios (ej.: 1000).
- Permitir solo las VLAN necesarias (`switchport trunk allowed vlan`).

## Dónde lo usé

- [[PRE Lab 03 - VLAN y trunking]] · [[PRE Lab 06 - EtherChannel]]

## Relacionado

- [[VLAN]] · [[IEEE 802.1Q Etiquetado de VLAN]] · [[IOS - VLAN y troncales]]
