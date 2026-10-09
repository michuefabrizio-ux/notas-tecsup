---
tipo: concepto
categoria: Electronica y circuitos
cursos: ["[[Electronica y Hardware de Computadoras]]"]
aliases: ["Ánodo común", "Cátodo común", LCD]
tags: []
---

# Display de 7 segmentos

## Comparación

| Tipo | Común conectado a | Segmento enciende con |
|---|---|---|
| **Cátodo común** | GND | 1 (HIGH) |
| **Ánodo común** | VCC | 0 (LOW) |

- Segmentos a–g + punto; para mostrar dígitos se usa un decodificador BCD a 7 segmentos o se manejan desde Arduino.
- Para más texto se usa una **LCD 16×2 (1602)**, normalmente con módulo **I2C**.

## Dónde lo usé

- [[EHC Lab 08 - Arduino displays y LCD]]

## Relacionado

- [[Codificador de prioridad]] · [[Arduino Uno]]
