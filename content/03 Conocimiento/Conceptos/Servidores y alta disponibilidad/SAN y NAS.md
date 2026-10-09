---
tipo: concepto
categoria: Servidores y alta disponibilidad
cursos: ["[[Arquitectura de Servidores]]"]
aliases: [SAN, NAS, DAS]
tags: []
---

# SAN y NAS

## Comparación

| Aspecto | DAS | NAS | SAN |
|---|---|---|---|
| Qué entrega | Disco local | **Archivos** por la red | **Bloques** por la red |
| Protocolos | SATA/SAS | SMB/CIFS, NFS | iSCSI, Fibre Channel |
| El cliente ve | Disco propio | Carpeta compartida | Disco propio (LUN) |
| Uso | Un servidor | Compartir archivos | Bases de datos, clústeres, VMs |

- **SMB** es el estándar de Windows (TCP 445); **NFS** el de Linux/Unix (2049).
- Separar los datos del servidor (desacoplar) permite reemplazar o duplicar el cómputo sin perder la información.

## Dónde lo usé

- [[ARQ Lab 04 - Servidores web con almacenamiento TrueNAS]] (NAS con SMB y NFS) · [[ARQ Lab 05-06 - Cluster de conmutacion por error con iSCSI]] (bloques iSCSI)

## Relacionado

- [[Almacenamiento compartido iSCSI]] · [[RAID]] · [[NFSv4]]
