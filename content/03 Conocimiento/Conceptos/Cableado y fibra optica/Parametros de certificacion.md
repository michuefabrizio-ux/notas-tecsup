---
tipo: concepto
categoria: Cableado y fibra optica
cursos: ["[[Cableado Estructurado y Fibra Optica]]"]
aliases: ["Parámetros de certificación", NEXT, PSNEXT, "ACR-F", "Pérdida de retorno"]
tags: []
---

# Parámetros de certificación (cobre)

## Qué es

- Mediciones que hace un certificador para decir si un enlace **PASA** o **FALLA** según TIA-568 / ISO 11801.

## Parámetros

| Parámetro | Qué mide | Mejor si… |
|---|---|---|
| Wiremap | Continuidad pin a pin, cruces, pares divididos | Correcto |
| Longitud / retardo | Distancia y tiempo de propagación | Dentro del límite |
| Delay skew | Diferencia de retardo entre pares | Bajo |
| Pérdida de inserción (IL) | Pérdida de potencia; crece con distancia y frecuencia | Baja |
| Pérdida de retorno (RL) | Reflexiones por desajuste de impedancia (100 Ω) | Alta (en dB) |
| NEXT | Diafonía en el extremo cercano | Alta (en dB) |
| PSNEXT | NEXT sumando el efecto de los otros 3 pares | Alta |
| ACR-N / ACR-F | Relación señal/diafonía en extremo cercano / lejano | Alta |
| TCL | Balance del par | Alta |
| PSANEXT / PSAACRF | Diafonía ajena (*alien*) entre cables | Alta |

- **Margen**: diferencia con el límite; positivo = PASA.
- RL: `RL = 20 log(|Z0 − Zm| / (Z0 + Zm))`. Ej.: Z0 = 100 Ω, Zm = 95 Ω → −31,83 dB.
- RL límite: Cat 5e 16 dB a 100 MHz; Cat 6A 8 dB a 500 MHz.
- Causas comunes de falla: destrenzado excesivo, jack mal ponchado, cable dañado.

## Dónde lo usé

- [[CAB Lab 01 - Calificacion de cableado por velocidad]] · [[CAB Lab 03 - Certificacion de cableado de par trenzado]] · [[CAB Lab 04 - Certificacion Cat 6A]]

## Relacionado

- [[Enlace permanente y canal]] · [[Fluke DSX]]
