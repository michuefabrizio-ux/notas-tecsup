---
tipo: concepto
categoria: Electronica y circuitos
cursos: ["[[Electronica y Hardware de Computadoras]]"]
aliases: ["Lógica secuencial", "Flip-flop", 7490]
tags: []
---

# Contadores y registros

## Qué es

- Circuitos **secuenciales**: su salida depende de las entradas y del estado anterior (memoria con **flip-flops**), al ritmo de un **reloj**.

## Contadores

- Binarios (módulo 2ⁿ) o decimales/BCD (módulo 10). **7490**: contador de décadas (÷2 y ÷5).
- Asíncronos (en cascada) o síncronos (todos con el mismo reloj).

## Registros de desplazamiento

| Tipo | Entrada → salida |
|---|---|
| SISO | Serie → serie |
| SIPO | Serie → paralelo |
| PISO | Paralelo → serie |
| PIPO | Paralelo → paralelo |

## Dónde lo usé

- [[EHC Lab 06 - Contadores]]

## Relacionado

- [[Display de 7 segmentos]] · [[CRC]] (los CRC se calculan con registros de desplazamiento)
