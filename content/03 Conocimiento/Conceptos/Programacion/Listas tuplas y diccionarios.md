---
tipo: concepto
categoria: Programacion
cursos: ["[[Programacion Basica para Redes]]"]
aliases: [Listas, Tuplas, Diccionarios]
tags: []
---

# Listas, tuplas y diccionarios

## Comparación

| Estructura | Sintaxis | ¿Se puede modificar? | Uso |
|---|---|---|---|
| Lista | `[1, 2, 3]` | Sí | Colecciones que cambian |
| Tupla | `("P001", "P002")` | No | Datos fijos (códigos) |
| Diccionario | `{"nombre": "Mouse", "stock": 50}` | Sí | Datos con clave |

```python
codigos = ("P001", "P002")
ventas = [10, 25, 8]
ventas.append(30)
inventario = {"P001": {"nombre": "Laptop HP", "stock": 15}}
for codigo, datos in inventario.items():
    print(codigo, datos["nombre"])
```

## Dónde lo usé

- [[PBR Ventas semanales con tuplas]] · [[PBR Trabajo - Sistema de gestion de inventario]]

## Relacionado

- [[Variables y tipos de datos]] · [[Ciclos for y while]]
