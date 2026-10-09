---
tipo: concepto
categoria: Programacion
cursos: ["[[Programacion Basica para Redes]]", "[[Informatica Aplicada]]"]
aliases: ["Estructuras repetitivas", Bucles]
tags: []
---

# Ciclos for y while

## Comparación

| Estructura | Cuándo usar | PSeInt |
|---|---|---|
| `for` | Número de vueltas conocido | `Para i <- 1 Hasta n` |
| `while` | Mientras se cumpla una condición | `Mientras … Hacer` |
| Hacer-mientras | Se ejecuta al menos una vez | `Repetir … Hasta Que` |

```python
total = 0                      # acumulador
for venta in [10, 25, 8]:
    total = total + venta
contador = 0                   # contador
while contador < 3:
    contador += 1
```

## Dónde lo usé

- [[INF Lab 15 - Estructuras repetitivas]] · [[PBR Ventas semanales con tuplas]]

## Relacionado

- [[Condicionales if elif else]]
