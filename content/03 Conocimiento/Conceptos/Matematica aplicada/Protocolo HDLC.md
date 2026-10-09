---
tipo: concepto
categoria: Matematica aplicada
cursos: ["[[Matematica para las Telecomunicaciones]]"]
aliases: [HDLC]
tags: []
---

# Protocolo HDLC

## Qué es

- *High-Level Data Link Control*: protocolo de capa 2 orientado a bits (base de PPP y del HDLC de Cisco en enlaces seriales).

## Trama

| Campo | Contenido |
|---|---|
| Bandera | `01111110` (inicio y fin) |
| Dirección | Estación secundaria |
| Control | Tipo de trama y números de secuencia |
| Información | Datos |
| FCS | CRC-CCITT (16 bits) |
| Bandera | `01111110` |

- Tipos de trama: **I** (información), **S** (supervisión), **U** (no numeradas).
- *Bit stuffing*: tras cinco 1 seguidos se inserta un 0 para no confundir con la bandera.

## Dónde lo usé

- [[MPT Lab 10 - Protocolo HDLC]]

## Relacionado

- [[CRC]]
