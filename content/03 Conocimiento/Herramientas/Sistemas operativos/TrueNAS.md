---
tipo: herramienta
categoria: Sistemas operativos
cursos: ["[[Arquitectura de Servidores]]"]
aliases: []
tags: []
---

# TrueNAS

## Qué es

- Sistema operativo de almacenamiento basado en **OpenZFS**, administrado por web. Publica datos por SMB, NFS e iSCSI.

## Conceptos de ZFS

- **Pool**: conjunto de discos (vdev Mirror, RAIDZ1, RAIDZ2…).
- **Dataset**: sistema de archivos dentro del pool (para SMB/NFS).
- **Zvol**: volumen de bloques (para iSCSI).

## Para qué la usé

- [[ARQ Lab 04 - Servidores web con almacenamiento TrueNAS]] — `Pool-Mirror` y `Pool-RAID5` con SMB y NFS.
- [[ARQ Lab 05-06 - Cluster de conmutacion por error con iSCSI]] — `pool-tecsup` y zvols iSCSI.

## Relacionado

- [[RAID]] · [[SAN y NAS]]
