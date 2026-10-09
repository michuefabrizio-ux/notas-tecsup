---
tipo: concepto
categoria: Servidores y alta disponibilidad
cursos: ["[[Electronica y Hardware de Computadoras]]"]
aliases: [FAT32, NTFS, exFAT]
tags: []
---

# Sistemas de archivos FAT32 y NTFS

## Comparación

| Aspecto | FAT32 | NTFS |
|---|---|---|
| Archivo máximo | 4 GB | Muy grande (TB) |
| Permisos | No (sin pestaña Seguridad) | Sí, por usuario y grupo |
| Cifrado / cuotas / journaling | No | Sí |
| Uso | USB, compatibilidad | Discos de Windows |

- En Linux: ext4, XFS, BTRFS (ver [[Bash - Discos y particiones]]).

## Dónde lo usé

- [[EHC Lab 16 - Instalacion de Windows y particiones]]
