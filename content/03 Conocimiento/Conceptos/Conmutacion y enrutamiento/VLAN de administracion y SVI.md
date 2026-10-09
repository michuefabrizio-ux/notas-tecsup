---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Protocolos de Enrutamiento]]"]
aliases: [SVI, "VLAN de administración"]
tags: []
---

# VLAN de administración y SVI

## Qué es

- La **SVI** (*Switch Virtual Interface*) es una interfaz lógica `interface vlan X` que da IP al switch para gestionarlo (SSH, SNMP).
- En switches de capa 3, las SVI también sirven de gateway para el enrutamiento inter-VLAN.

```text
S1(config)# interface vlan 99
S1(config-if)# ip address 192.168.99.11 255.255.255.0
S1(config-if)# no shutdown
S1(config)# ip default-gateway 192.168.99.1
```

## Dónde lo usé

- [[PRE Lab 01 - Configuracion basica de switch]]

## Relacionado

- [[IOS - Configuracion basica de switch]] · [[VLAN]]
