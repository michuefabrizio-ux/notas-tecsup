---
tipo: concepto
categoria: Servidores y alta disponibilidad
cursos: ["[[Arquitectura de Servidores]]", "[[Servicios de Red]]"]
aliases: ["Punto único de falla", "Single Point of Failure"]
tags: []
---

# SPOF (punto único de falla)

## Qué es

- Componente cuya falla detiene todo el servicio porque no tiene respaldo.

## Cómo se evita

- Redundancia en cada capa: discos (RAID), servidores (clúster), red (enlaces y equipos dobles, FHRP), energía (fuentes redundantes, PDU, UPS).

## Dónde lo vi

- Consolidar DNS, web, FTP y correo en un solo servidor crea un SPOF: [[SRD GLAB-S05 - DNS Web FTP y Correo]]
- Lo resuelve el clúster: [[ARQ Lab 05-06 - Cluster de conmutacion por error con iSCSI]]

## Relacionado

- [[RAID]] · [[Cluster de conmutacion por error]] · [[HSRP]]
