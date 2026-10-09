---
tipo: concepto
categoria: Electronica y circuitos
cursos: ["[[Electronica y Hardware de Computadoras]]"]
aliases: ["Pull-down", "Pull-up"]
tags: []
---

# Resistencias pull-down y limitadoras

## Comparación

| Uso | Cómo | Para qué |
|---|---|---|
| **Pull-down** | Resistencia (≈10 kΩ) de la entrada a GND | Que la entrada lea 0 cuando el pulsador está suelto (sin "flotar") |
| **Pull-up** | Resistencia de la entrada a 5 V (o `INPUT_PULLUP`) | Lee 1 en reposo y 0 al pulsar |
| **Limitadora** | Resistencia en serie con un LED | Limitar la corriente: `R = (Vfuente − VLED) / I` |

- Ej.: 5 V, LED de 2 V a 15 mA → R = 3 / 0,015 = 200 Ω (se usa 220 Ω).

## Dónde lo usé

- [[EHC Lab 09 - Arduino entradas y salidas digitales]]

## Relacionado

- [[Ley de Ohm y circuitos serie y paralelo]] · [[Arduino Uno]]
