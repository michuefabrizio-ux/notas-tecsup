---
tipo: concepto
categoria: Matematica aplicada
cursos: ["[[Matematica para las Telecomunicaciones]]"]
aliases: [Fourier, Espectro]
tags: []
---

# Serie de Fourier

## Qué es

- Representación de una señal **periódica** como suma de una componente continua y senos/cosenos de frecuencias múltiplas de la fundamental f₀ = 1/T.

## Cómo funciona

- `x(t) = a₀ + Σ [aₙ·cos(2πnf₀t) + bₙ·sen(2πnf₀t)]`
- Cada término es un **armónico**; el conjunto de amplitudes por frecuencia es el **espectro discreto**.
- Onda cuadrada simétrica: solo armónicos **impares**, con amplitud proporcional a 1/n (4A/(nπ)). Cuantos más armónicos se suman, más se parece a la cuadrada.
- Señales no periódicas → **transformada de Fourier** y espectro continuo.

## Dónde lo usé

- [[MPT S01 - Senales espectros y serie de Fourier]] · [[MPT Serie de Fourier onda cuadrada en Excel]]

## Relacionado

- [[Convolucion]] · [[Excel]]
