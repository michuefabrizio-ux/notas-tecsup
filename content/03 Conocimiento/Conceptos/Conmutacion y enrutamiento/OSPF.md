---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Redes Escalables]]"]
aliases: [OSPFv2, DR, BDR]
tags: []
---

# OSPF

## Qué es

- Protocolo de enrutamiento de **estado de enlace** (distancia administrativa 110); usa el **costo** como métrica.

## Cómo funciona

- Los routers forman **adyacencias** con Hellos, intercambian LSAs y calculan rutas con SPF (Dijkstra).
- **Router ID**: `router-id` manual → mayor IP de loopback → mayor IP activa.
- **Área 0** (backbone) en OSPF de área única.
- En redes multiacceso se eligen **DR** y **BDR** (mayor prioridad, luego mayor router ID); el resto es **DROTHER**.
- Direcciones: 224.0.0.5 (todos los routers OSPF), 224.0.0.6 (DR y BDR).
- Estados finales: FULL (con DR/BDR) y 2-WAY (entre DROTHERs).

## Dónde lo usé

- [[RES S02 - OSPFv2 de area unica]] · [[RES Examen - OSPF y ACL]]

## Relacionado

- [[IOS - OSPF]] · [[Mascara wildcard]]
