---
tipo: concepto
categoria: Programacion
cursos: ["[[Programacion Basica para Redes]]"]
aliases: [Funciones, "Módulos"]
tags: []
---

# Funciones y módulos

## Qué es

- **Función**: bloque con nombre que se reutiliza (`def`). **Módulo**: archivo `.py` que otro importa; un **paquete** es una carpeta de módulos con `__init__.py`.

```python
# modulos/reportes.py
def total(lista):
    return sum(lista)

# main.py
from modulos import reportes
print(reportes.total([1, 2, 3]))
```

## Dónde lo usé

- [[PBR Proyecto - Encuestas presidenciales]] (main + paquete de módulos) · [[PBR Trabajo - Sistema de gestion de inventario]]

## Relacionado

- [[Python basico]]
