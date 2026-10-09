---
tipo: concepto
categoria: Servidores y alta disponibilidad
cursos: ["[[Arquitectura de Servidores]]"]
aliases: ["RAID 1", "RAID 5", RAIDZ]
tags: []
---

# RAID

## Qué es

- **RAID** (*Redundant Array of Independent/Inexpensive Disks*): varios discos tratados como una sola unidad para ganar **rendimiento** y/o **tolerancia a fallos**.
- RAID **no reemplaza el backup**: protege contra falla de disco, no contra borrado, virus o corrupción.

## Cómo funciona

- **Striping**: reparte los datos en bloques entre discos (velocidad).
- **Mirroring**: copia idéntica en otro disco.
- **Paridad**: dato calculado que permite reconstruir un disco perdido.

## Comparación

| Nivel | Técnica | Mín. discos | Tolera | Capacidad útil |
|---|---|---|---|---|
| RAID 0 | Striping | 2 | 0 discos | 100 % |
| RAID 1 | Mirroring | 2 | 1 disco | 50 % |
| RAID 5 | Striping + paridad distribuida | 3 | 1 disco | (n−1)/n |
| RAID 6 | Doble paridad | 4 | 2 discos | (n−2)/n |
| RAID 10 | Espejo + striping | 4 | 1 por espejo | 50 % |

- En ZFS/TrueNAS: **Mirror** ≈ RAID 1, **RAIDZ1** ≈ RAID 5, RAIDZ2 ≈ RAID 6.
- **Hardware RAID** (controladora dedicada) vs **software RAID** (lo hace el sistema operativo).

## Dónde lo usé

- [[ARQ Lab 04 - Servidores web con almacenamiento TrueNAS]] (Mirror y RAIDZ1)

## Relacionado

- [[SAN y NAS]] · [[SPOF]] · [[TrueNAS]]
