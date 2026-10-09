---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Redes Escalables]]"]
aliases: ["Máscara wildcard", Wildcard]
tags: []
---

# Máscara wildcard

## Qué es

- Máscara usada en ACL y OSPF donde **0 = el bit debe coincidir** y **1 = no importa**.

## Cómo se calcula

- `255.255.255.255 − máscara de subred`.

| Prefijo | Máscara | Wildcard |
|---|---|---|
| /24 | 255.255.255.0 | 0.0.0.255 |
| /26 | 255.255.255.192 | 0.0.0.63 |
| /27 | 255.255.255.224 | 0.0.0.31 |
| /28 | 255.255.255.240 | 0.0.0.15 |
| /30 | 255.255.255.252 | 0.0.0.3 |

- Atajos: `host 10.1.1.1` = `10.1.1.1 0.0.0.0`; `any` = `0.0.0.0 255.255.255.255`.

## Dónde lo usé

- [[RES GLAB-S05 - ACL extendidas]] · [[RES S02 - OSPFv2 de area unica]]

## Relacionado

- [[ACL estandar y extendida]] · [[OSPF]] · [[Direccionamiento IPv4 y subredes]]
