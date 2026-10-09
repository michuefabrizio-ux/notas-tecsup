---
tipo: concepto
categoria: Matematica aplicada
cursos: ["[[Matematica para las Telecomunicaciones]]"]
aliases: [Hamming, Paridad, "Síndrome"]
tags: []
---

# Códigos de detección y corrección de errores

## Comparación

| Técnica | Detecta | Corrige |
|---|---|---|
| Paridad par/impar | 1 bit (errores impares) | No |
| Hamming (7,4) | 2 bits | 1 bit |
| Códigos de bloque lineales | Según distancia mínima | Según distancia mínima |
| CRC | Ráfagas | No (solo detecta) |

## Cómo funciona

- **Paridad par**: se agrega un bit para que el total de 1 sea par.
- **Código de bloque (n, k)**: k bits de datos + (n − k) de redundancia. Matriz generadora **G**: `c = d·G`; matriz de verificación **H**.
- **Síndrome**: `s = r·Hᵀ`; si s = 0 no hay error detectado; si no, indica la posición del error.
- **Hamming**: bits de paridad en las posiciones 1, 2, 4, 8…; corrige un error. Se usa en memorias ECC.
- Capacidad: detecta d_min − 1 errores y corrige ⌊(d_min − 1)/2⌋.

## Dónde lo usé

- [[MPT Lab 07 - Deteccion y correccion de errores]]

## Relacionado

- [[CRC]]
