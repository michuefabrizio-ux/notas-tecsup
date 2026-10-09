---
tipo: concepto
categoria: Electronica y circuitos
cursos: ["[[Electronica y Hardware de Computadoras]]"]
aliases: ["Compuertas lógicas", TTL]
tags: []
---

# Compuertas lógicas TTL

## Tabla

| Compuerta | Expresión | CI TTL |
|---|---|---|
| NOT | `Y = A'` | 7404 |
| AND | `Y = A·B` | 7408 |
| OR | `Y = A + B` | 7432 |
| NAND | `Y = (A·B)'` | 7400 |
| NOR | `Y = (A + B)'` | 7402 |
| XOR | `Y = A ⊕ B` | 7486 |

- TTL trabaja con **5 V**: 0 lógico ≈ 0–0,8 V, 1 lógico ≈ 2–5 V.
- NAND y NOR son **universales** (con ellas se arma cualquier función).
- Flujo de diseño: problema → tabla de verdad → ecuación (simplificar) → circuito.

## Dónde lo usé

- [[EHC Lab 04 - Logica combinacional]]

## Relacionado

- [[Multiplexor y demultiplexor]] · [[WinBreadboard]] · [[Tinkercad]]
