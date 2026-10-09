---
tipo: concepto
categoria: Fundamentos de redes
cursos: ["[[Implementacion de Redes]]"]
aliases: [Subnetting, VLSM, "Subredes IPv4"]
tags: []
---

# Direccionamiento IPv4 y subredes

## Qué es

- Dirección IPv4 = 32 bits (4 octetos). La **máscara** separa la porción de **red** y de **host**.

## Fórmulas

- Hosts por subred = 2ʰ − 2 (h = bits de host).
- Subredes = 2ⁿ (n = bits prestados).
- Salto (tamaño de bloque) = 256 − valor del octeto de la máscara.

| Prefijo | Máscara | Hosts |
|---|---|---|
| /24 | 255.255.255.0 | 254 |
| /25 | 255.255.255.128 | 126 |
| /26 | 255.255.255.192 | 62 |
| /27 | 255.255.255.224 | 30 |
| /28 | 255.255.255.240 | 14 |
| /29 | 255.255.255.248 | 6 |
| /30 | 255.255.255.252 | 2 |

## VLSM

1. Ordenar las redes de mayor a menor número de hosts.
2. Asignar a cada una el prefijo justo, empezando por la más grande.
3. Seguir con la siguiente dirección libre.

- Privadas (RFC 1918): 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16. APIPA: 169.254.0.0/16.

## Dónde lo usé

- [[IMR Lab 11-12 - Diseno VLSM]] · [[IMR Lab 16 - Evaluacion final PTSA]]

## Relacionado

- [[Mascara wildcard]] · [[IPv6]]
