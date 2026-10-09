---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Protocolos de Enrutamiento]]"]
aliases: [LACP, PAgP, "Port-channel"]
tags: []
---

# EtherChannel

## Qué es

- Agrupa de 2 a 8 enlaces físicos en un **port-channel** lógico: suma ancho de banda y da redundancia; STP lo ve como un solo enlace.

## Comparación

| Protocolo | Tipo | Modos que forman canal |
|---|---|---|
| PAgP | Cisco | desirable–desirable, desirable–auto |
| LACP | IEEE 802.3ad | active–active, active–passive |
| Estático | — | on–on |

- LACP en un lado y PAgP en el otro **no** forman canal.
- Los puertos deben coincidir en velocidad, dúplex, modo (access/trunk), VLAN permitidas y nativa.

```text
S1(config)# interface range f0/1-2
S1(config-if-range)# channel-group 1 mode active
S1(config)# interface port-channel 1
S1(config-if)# switchport mode trunk
show etherchannel summary
```

## Dónde lo usé

- [[PRE Lab 06 - EtherChannel]]

## Relacionado

- [[STP]] · [[Enlace troncal y VLAN nativa]]
