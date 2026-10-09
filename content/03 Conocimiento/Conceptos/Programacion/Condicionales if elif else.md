---
tipo: concepto
categoria: Programacion
cursos: ["[[Programacion Basica para Redes]]", "[[Informatica Aplicada]]"]
aliases: [Condicionales, "Estructuras condicionales"]
tags: []
---

# Condicionales if / elif / else

## Qué es

- Ejecutan un bloque u otro según una condición. `elif` = "si no, si…" (otra condición cuando la anterior fue falsa).

```python
velocidad = 95
if velocidad <= 70:
    multa = 0
elif velocidad <= 90:
    multa = 100
elif velocidad <= 100:
    multa = 140
else:
    multa = 200
```

| PSeInt | Python |
|---|---|
| `Si … Entonces … SiNo … FinSi` | `if … else` |
| `Segun … Hacer` | `if/elif` encadenados |

## Dónde lo usé

- [[INF Lab 14 - Tipos de datos y condicionales]]

## Relacionado

- [[Ciclos for y while]] · [[Diagramas de flujo EPS]]
