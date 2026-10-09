---
tipo: comando
categoria: Cisco IOS
cursos: ["[[Redes Escalables]]"]
aliases: []
tags: []
---

# IOS — OSPF

```text
R1(config)# router ospf 10
R1(config-router)# router-id 1.1.1.1
R1(config-router)# network 10.1.1.4 0.0.0.3 area 0
R1(config-router)# passive-interface g0/0/1
R1(config-router)# exit
R1(config)# interface g0/0/0
R1(config-if)# ip ospf 10 area 0
R1(config-if)# ip ospf priority 255
R1(config)# interface loopback 0
R1(config-if)# ip ospf network point-to-point
R1# clear ip ospf process
```

## Verificación

```text
show ip protocols
show ip ospf neighbor
show ip ospf interface g0/0/0
show ip ospf interface brief
show ip route ospf
```

Concepto: [[OSPF]]
