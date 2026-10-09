---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Protocolos de Enrutamiento]]"]
aliases: [DUAL]
tags: []
---

# EIGRP

## Qué es

- Protocolo de enrutamiento **vector distancia avanzado** de Cisco (AD 90 interna); usa el algoritmo **DUAL** y guarda rutas de respaldo (*feasible successors*) para converger muy rápido.

## Puntos clave

- Los vecinos deben tener el **mismo número de AS**.
- `no auto-summary` para trabajar sin clase (VLSM).
- `passive-interface` en las LAN.

```text
R1(config)# router eigrp 100
R1(config-router)# network 192.168.1.0 0.0.0.255
R1(config-router)# no auto-summary
R1(config-router)# passive-interface g0/0
show ip eigrp neighbors
show ip route eigrp
```

## Dónde lo usé

- [[PRE Lab 15 - EIGRP avanzado]] · Topología del [[RES GLAB-S04 - ACL estandar]] (EIGRP preconfigurado)

## Relacionado

- [[OSPF]] · [[Rutas estaticas]]
