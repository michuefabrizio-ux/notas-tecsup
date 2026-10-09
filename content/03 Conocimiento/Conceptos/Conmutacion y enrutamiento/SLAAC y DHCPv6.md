---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Protocolos de Enrutamiento]]"]
aliases: [SLAAC, DHCPv6]
tags: []
---

# SLAAC y DHCPv6

## Comparación

| Método | Dirección | DNS y otros | Flags RA |
|---|---|---|---|
| SLAAC | El host la arma con el prefijo del RA | En el RA (RDNSS) | A=1, O=0, M=0 |
| DHCPv6 sin estado | SLAAC | Servidor DHCPv6 | A=1, O=1 |
| DHCPv6 con estado | Servidor DHCPv6 | Servidor DHCPv6 | M=1 |

- El identificador de interfaz puede ser **EUI-64** (a partir de la MAC) o aleatorio.
- El gateway siempre es la **link-local** del router que envió el RA.

## Dónde lo usé

- [[PRE M08 - SLAAC y DHCPv6]]

## Relacionado

- [[IPv6]] · [[DHCP y DHCP relay]]
