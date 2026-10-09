---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Protocolos de Enrutamiento]]"]
aliases: ["Port security", "DHCP snooping", DAI]
tags: []
---

# Seguridad de puertos del switch

## Técnicas

| Técnica | Protege contra |
|---|---|
| Apagar puertos sin uso + VLAN aislada | Conexiones no autorizadas |
| **Port security** | MAC flooding y equipos no autorizados |
| **DHCP snooping** | Servidores DHCP falsos / agotamiento DHCP |
| **DAI** (Dynamic ARP Inspection) | ARP spoofing |
| IP Source Guard | Suplantación de IP |
| PortFast + BPDU Guard | Switches no autorizados |
| Desactivar CDP en puertos de usuario | Fuga de información de la red |

```text
S1(config-if)# switchport mode access
S1(config-if)# switchport port-security
S1(config-if)# switchport port-security maximum 2
S1(config-if)# switchport port-security mac-address sticky
S1(config-if)# switchport port-security violation restrict
S1(config)# ip dhcp snooping
S1(config)# ip dhcp snooping vlan 10
S1(config-if)# ip dhcp snooping trust      ! solo hacia el servidor DHCP legítimo
show port-security interface f0/1
```

- Violación: **protect** (descarta), **restrict** (descarta y registra), **shutdown** (err-disabled, por defecto).

## Dónde lo usé

- [[PRE Lab 10 - CDP y ataque a la tabla MAC]] · [[PRE Lab 11 - Seguridad en switch]]

## Relacionado

- [[Sniffing y ARP spoofing]] · [[STP]]
