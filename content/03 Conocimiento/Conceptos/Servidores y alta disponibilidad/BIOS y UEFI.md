---
tipo: concepto
categoria: Servidores y alta disponibilidad
cursos: ["[[Soporte de Hardware y Software]]", "[[Electronica y Hardware de Computadoras]]"]
aliases: [BIOS, UEFI, POST, CMOS]
tags: []
---

# BIOS y UEFI

## Qué es

- *Firmware* que arranca el equipo: hace el **POST** (autoprueba), inicializa el hardware y carga el sistema operativo. La configuración se guarda en la **CMOS** (con pila).

## Comparación

| Aspecto | BIOS (legado) | UEFI |
|---|---|---|
| Tabla de particiones | MBR (discos ≤ 2 TB, 4 primarias) | GPT (discos enormes, 128 particiones) |
| Interfaz | Texto | Gráfica, con ratón |
| Arranque | Más lento | Más rápido |
| Seguridad | — | *Secure Boot* |
| Compatibilidad | Muy amplia | Equipos modernos |

## Dónde lo usé

- [[SHS Lab 03 - BIOS UEFI y cotizacion de PC]] · [[EHC S15-16 - Hardware del computador virtualizacion y SO moviles]]

## Relacionado

- [[Sistemas de archivos FAT32 y NTFS]]
