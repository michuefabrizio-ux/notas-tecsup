---
tipo: comando
categoria: Cisco IOS
cursos: ["[[Redes Escalables]]"]
aliases: []
tags: []
---

# IOS — ACL

## Estándar numerada

```text
R2(config)# access-list 1 deny 192.168.11.0 0.0.0.255
R2(config)# access-list 1 permit any
R2(config)# interface g0/0
R2(config-if)# ip access-group 1 out
```

## Estándar nombrada

```text
R1(config)# ip access-list standard File_Server_Restrictions
R1(config-std-nacl)# permit host 192.168.20.4
R1(config-std-nacl)# deny any
```

## Extendida

```text
R1(config)# access-list 100 permit tcp 172.22.34.64 0.0.0.31 host 172.22.34.62 eq ftp
R1(config)# access-list 100 permit icmp 172.22.34.64 0.0.0.31 host 172.22.34.62
R1(config)# interface g0/0
R1(config-if)# ip access-group 100 in

R1(config)# ip access-list extended HTTP_ONLY
R1(config-ext-nacl)# permit tcp 172.22.34.96 0.0.0.15 host 172.22.34.62 eq www
R1(config-ext-nacl)# permit icmp 172.22.34.96 0.0.0.15 host 172.22.34.62
```

## Restringir VTY

```text
R1(config)# line vty 0 4
R1(config-line)# access-class vty_block in
```

## Verificación

```text
show access-lists
show ip interface g0/0
```

Concepto: [[ACL estandar y extendida]]
