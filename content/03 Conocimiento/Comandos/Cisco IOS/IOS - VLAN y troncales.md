---
tipo: comando
categoria: Cisco IOS
cursos: ["[[Protocolos de Enrutamiento]]", "[[Redes Escalables]]"]
aliases: []
tags: []
---

# IOS — VLAN y troncales

```text
S1(config)# vlan 10
S1(config-vlan)# name Ventas
S1(config)# interface f0/6
S1(config-if)# switchport mode access
S1(config-if)# switchport access vlan 10
S1(config)# interface range f0/7-24
S1(config-if-range)# switchport access vlan 999
S1(config-if-range)# shutdown
S1(config)# interface g0/1
S1(config-if)# switchport mode trunk
S1(config-if)# switchport trunk native vlan 1000
S1(config-if)# switchport trunk allowed vlan 10,20,30,1000
S1(config-if)# switchport nonegotiate
```

## Verificación

```text
show vlan brief
show interfaces trunk
show interfaces f0/6 switchport
```

Conceptos: [[VLAN]] · [[Enlace troncal y VLAN nativa]]
