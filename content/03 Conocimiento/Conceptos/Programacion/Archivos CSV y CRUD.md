---
tipo: concepto
categoria: Programacion
cursos: ["[[Programacion Basica para Redes]]"]
aliases: [CSV, CRUD]
tags: []
---

# Archivos CSV y CRUD

## Qué es

- **CSV**: texto con valores separados por comas, una fila por registro.
- **CRUD**: *Create, Read, Update, Delete* (crear, leer, actualizar, eliminar).

```python
import csv

with open("datos.csv", newline="", encoding="utf-8") as f:   # leer
    filas = list(csv.DictReader(f))

filas.append({"codigo": "P006", "nombre": "Teclado"})        # crear
for fila in filas:                                           # actualizar
    if fila["codigo"] == "P001":
        fila["nombre"] = "Laptop Lenovo"
filas = [f for f in filas if f["codigo"] != "P002"]          # eliminar

with open("datos.csv", "w", newline="", encoding="utf-8") as f:
    w = csv.DictWriter(f, fieldnames=["codigo", "nombre"])
    w.writeheader()
    w.writerows(filas)
```

## Dónde lo usé

- [[PBR LC04 - Archivos CSV y CRUD]]

## Relacionado

- [[Funciones y modulos]] · [[Python basico]]
