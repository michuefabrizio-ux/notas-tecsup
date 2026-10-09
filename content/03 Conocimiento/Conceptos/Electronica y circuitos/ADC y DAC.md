---
tipo: concepto
categoria: Electronica y circuitos
cursos: ["[[Electronica y Hardware de Computadoras]]"]
aliases: [ADC, DAC, PWM]
tags: []
---

# ADC y DAC

## Qué es

- **ADC**: convierte una señal analógica en digital (ej.: ADC0808, 8 bits). **DAC**: lo contrario (ej.: DAC0800).

## Cómo funciona

- Resolución: n bits → 2ⁿ niveles; paso = Vref / 2ⁿ.
- Arduino Uno: ADC de **10 bits** (0–1023 para 0–5 V) con `analogRead()`; no tiene DAC real, usa **PWM** (0–255) con `analogWrite()`.

## Dónde lo usé

- [[EHC Lab 12 - Entradas y salidas analogicas]]

## Relacionado

- [[Arduino Uno]] · [[Serie de Fourier]]
