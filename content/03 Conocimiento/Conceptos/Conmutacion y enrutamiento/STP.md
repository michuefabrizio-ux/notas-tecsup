---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Protocolos de Enrutamiento]]"]
aliases: ["Spanning Tree", "Rapid PVST+", PortFast, "BPDU Guard"]
tags: []
---

# STP (Spanning Tree Protocol)

## Qué es

- Protocolo que evita **bucles de capa 2** bloqueando puertos redundantes, dejando un solo camino lógico.

## Cómo funciona

1. Elige el **puente raíz**: menor **BID** (prioridad, por defecto 32768 + ID de VLAN, y luego la MAC).
2. Cada switch elige su **puerto raíz** (menor costo a la raíz).
3. En cada segmento se elige un **puerto designado**.
4. Los demás quedan **alternos/bloqueados**.

## Comparación

| Versión | Estándar | Convergencia |
|---|---|---|
| STP | 802.1D | 30–50 s |
| PVST+ | Cisco, una instancia por VLAN | ~30 s |
| RSTP | 802.1w | < 1 s |
| Rapid PVST+ | Cisco, RSTP por VLAN | < 1 s (en mi lab: 34 ms) |

- **PortFast**: el puerto de acceso pasa directo a *forwarding*.
- **BPDU Guard**: apaga el puerto si recibe una BPDU (alguien conectó un switch).

```text
S2(config)# spanning-tree mode rapid-pvst
S2(config)# spanning-tree vlan 10,20 root primary
S1(config)# spanning-tree vlan 10,20 root secondary
S1(config-if)# spanning-tree portfast
S1(config-if)# spanning-tree bpduguard enable
show spanning-tree
```

## Dónde lo usé

- [[PRE Lab 05 - STP Rapid PVST PortFast y BPDU Guard]] · [[PRE Lab 11 - Seguridad en switch]]

## Relacionado

- [[EtherChannel]] · [[SPOF]]
