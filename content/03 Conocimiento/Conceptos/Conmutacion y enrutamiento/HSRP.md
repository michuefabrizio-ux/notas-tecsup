---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Protocolos de Enrutamiento]]"]
aliases: [FHRP, VRRP, GLBP]
tags: []
---

# HSRP

> Visto en clase y en laboratorio: [[PRE Lab 09 - HSRP]].

## Qué es

- *Hot Standby Router Protocol* (Cisco): dos o más routers comparten una **IP y MAC virtuales** que los hosts usan como gateway. Es un **FHRP**.

## Cómo funciona

- Un router **activo** reenvía; otro queda en **standby**.
- Gana la mayor **prioridad** (por defecto 100); con **preempt** el de mayor prioridad recupera el rol al volver.

```text
R1(config-if)# standby version 2
R1(config-if)# standby 1 ip 192.168.1.254
R1(config-if)# standby 1 priority 110
R1(config-if)# standby 1 preempt
show standby brief
```

## Comparación

| FHRP | Tipo | Balanceo |
|---|---|---|
| HSRP | Cisco | No |
| VRRP | Estándar IETF | No |
| GLBP | Cisco | Sí |

## Dónde lo usé

- [[PRE Lab 09 - HSRP]]

## Relacionado

- [[SPOF]] · [[Disponibilidad y SLA]]
