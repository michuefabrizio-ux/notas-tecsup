---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Protocolos de Enrutamiento]]", "[[Redes Escalables]]"]
aliases: ["Router-on-a-stick", "Inter-VLAN"]
tags: []
---

# Enrutamiento inter-VLAN

## Comparación

| Método | Cómo | Limitación |
|---|---|---|
| Heredado | Una interfaz física del router por VLAN | No escala |
| Router-on-a-stick | Subinterfaces en un troncal | Un solo enlace = cuello de botella |
| Switch capa 3 | SVI por VLAN + `ip routing` | Requiere switch L3 |

```text
R1(config)# interface g0/0/1.10
R1(config-subif)# encapsulation dot1Q 10
R1(config-subif)# ip address 192.168.10.1 255.255.255.0
R1(config)# interface g0/0/1.99
R1(config-subif)# encapsulation dot1Q 99 native
```

## Dónde lo usé

- [[PRE Lab 04 - Enrutamiento inter-VLAN]] · [[PRE Lab 07 - Configurar DHCPv4]] · Eje [[OE2 - VLAN ACL y DMZ]]

## Relacionado

- [[VLAN]] · [[Enlace troncal y VLAN nativa]]
