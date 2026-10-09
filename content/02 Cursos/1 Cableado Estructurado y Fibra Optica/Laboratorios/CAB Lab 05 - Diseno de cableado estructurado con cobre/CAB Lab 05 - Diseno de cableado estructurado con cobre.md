---
tipo: laboratorio
curso: "[[Cableado Estructurado y Fibra Optica]]"
ciclo: 4
periodo: 2026-2
semana: 5
fecha: 2026-09-18
estado: entregado
calificacion:
aliases: ["CAB Lab 05 - Diseño de cableado estructurado con cobre"]
tags: [curso/cableado, pi/oe1]
---

# CAB Lab 05 — Diseño de cableado estructurado con cobre

← MOC del curso: [[Cableado Estructurado y Fibra Optica]] · Clase: [[CAB S05 - Puesta a tierra administracion y diseno de cobre]] · Guía: `guia/GLAB-S05-JVELARDE-2026-1.docx` · Entrega: `entrega/GLAB-S05-JVELARDE-2026-1.pdf` (y `DOC-20261003-WA0025.pdf`, versión de otro grupo)

## Objetivo

- Especificar puesta a tierra y documentación, y diseñar los enlaces de un cableado estructurado de cobre.

## Diseño (de nuestro informe)

- Normas: EIA/TIA-568, 569 y 606.
- **ER** en el 2.º piso para acortar el backbone; **8 TR** (2 por piso) para que ningún enlace pase de **90 m**; **54 usuarios**.
- Edificio de concreto sin ductos: canaletas de PVC adosadas (principal, secundaria, terciaria); **15 cm** de separación del cableado eléctrico; sin pasar por baños, tragaluces ni marcos de puertas.
- **Metrado**: ~849 m de UTP Cat 6A = **2,78 bobinas de 305 m**, con reserva por enlace.

## Conclusiones (del informe)

- Respetar distancias y especificaciones hace la red estable y preparada para el futuro.
- Topología en estrella: ER/MC → TR/FD → áreas de trabajo, con backbone de fibra.

## Relacionado

- [[Metrado de cableado horizontal]] · [[Ocupacion de canalizaciones]] · [[Dimensionamiento de ER y TR]] · [[OE1 - Cableado Cat 6A y OM5]]
