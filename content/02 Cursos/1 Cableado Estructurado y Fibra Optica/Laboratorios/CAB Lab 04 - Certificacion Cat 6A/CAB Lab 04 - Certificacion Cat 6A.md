---
tipo: laboratorio
curso: "[[Cableado Estructurado y Fibra Optica]]"
ciclo: 4
periodo: 2026-2
semana: 4
fecha:
estado: entregado
calificacion:
aliases: ["Certificación de cableado UTP Cat. 6A"]
tags: [curso/cableado, pi/oe1]
---

# CAB Lab 04 — Certificación de cableado UTP Cat 6A

← MOC del curso: [[Cableado Estructurado y Fibra Optica]] · Clase: [[CAB S04 - Sistemas de distribucion y espacios]] · Guía: `guia/GLAB-S04-JVELARDE-2026-1.docx` · Entrega: `entrega/GLAB-S04-JVELARDE-2026-1.docx-DYMER.docx.pdf`

## Objetivo

- Especificar el cableado de distribución y espacios, y hacer troubleshooting de enlaces de cobre con HDTDR y HDTDX.

## Escenario

| Tramo | Medio | Velocidad |
|---|---|---|
| Horizontal | F/UTP Cat 6A | 1 Gbps |
| Vertical | Cat 6A | 10 Gbps |
| Horizontal | F/UTP Cat 6 | 1 Gbps |

## Procedimiento

1. Instalar cableado horizontal Cat 6A (cables 001 a 009).
2. Autotest con **Fluke Versiv DSX-5000** (enlace permanente).
3. Revisar wiremap, NEXT, IL, RL, ACR-F y ACR-N.

## Conclusiones (del informe)

- 100 % de los enlaces (001–009) **PASA** con TIA-568-C e ISO 11801; longitudes de 28–29 ft; aptos para 10GBASE-T.
- Wiremap correcto (T568A y T568B) sin cortos, abiertos ni pares divididos; NEXT con margen de hasta +6,0 dB.
- Blindaje y drenaje del F/UTP integrados correctamente.

## Relacionado

- [[Parametros de certificacion]] · [[Blindaje U-UTP y F-UTP]] · [[OE1 - Cableado Cat 6A y OM5]]
