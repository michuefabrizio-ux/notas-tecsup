---
tipo: clase
curso: "[[Cableado Estructurado y Fibra Optica]]"
ciclo: 4
periodo: 2026-2
semana: 3
fecha:
estado: entregado
calificacion:
aliases: ["CAB S03 - Parámetros de certificación"]
tags: [curso/cableado]
---

# CAB S03 — Parámetros de certificación

← MOC del curso: [[Cableado Estructurado y Fibra Optica]] · Fuente: `Material/PPT-S03-JVELARDE-2026-02.pdf`, `Material/Lectura 01.pdf` (manual de solución de problemas de cobre)

## Tema de la sesión

- Parámetros que mide un certificador en enlaces Cat 5e, 6 y 6A según TIA-568 e ISO/IEC 11801.

## Lo esencial

- Se certifica para garantizar que lo instalado cumple lo que el cliente pagó; las redes certificadas tienen menos errores.
- Modelos de prueba: **enlace permanente**, **canal** (≤ 100 m) y **MPTL** (jack en un extremo y plug en el otro; cámaras, AP, iluminación).
- Parámetros: pérdida de inserción, pérdida de retorno, NEXT, PSNEXT, FEXT, ACR-N, ACR-F, PS-ACR-F, TCL, retardo de propagación, *delay skew* y alien (PSANEXT, PSAACRF).
- **Margen** = límite − medido (en IL) o medido − límite (en RL); margen positivo = PASA.
- RL: `RL = 20 log(|Zdeseada − Zmedida| / (Zdeseada + Zmedida))`. Ej.: Z = 95 Ω → −31,83 dB. Límites: 5e 16 dB a 100 MHz, 6A 8 dB a 500 MHz.

## Conceptos, comandos y normas vistos

- [[Parametros de certificacion]] · [[Enlace permanente y canal]] · [[Fluke DSX]]
