---
tipo: concepto
categoria: Cableado y fibra optica
cursos: ["[[Cableado Estructurado y Fibra Optica]]"]
aliases: [Metrado]
tags: []
---

# Metrado de cableado horizontal

## Qué es

- Cálculo de la cantidad de cable (y bobinas) necesaria para el cableado horizontal.

## Cómo funciona

1. Medir en plano el recorrido de cada enlace (TR → TO) siguiendo la canalización.
2. Sumar las bajadas verticales y la reserva para terminaciones (patch panel y roseta).
3. Verificar que ningún enlace pase de **90 m**.
4. Total ÷ **305 m** (bobina) = número de bobinas (redondear hacia arriba al comprar).

- Ejemplo de mi lab: 849 m de Cat 6A → 849 / 305 = **2,78 bobinas**.

## Dónde lo usé

- [[CAB Lab 05 - Diseno de cableado estructurado con cobre]]

## Relacionado

- [[Ocupacion de canalizaciones]] · [[ANSI-TIA-568 Cableado estructurado]]
