---
tipo: comando
categoria: Python
cursos: ["[[Programacion Basica para Redes]]"]
aliases: []
tags: []
---

# Python básico

```python
nombre = input("Nombre: ")
edad = int(input("Edad: "))
print(f"Hola {nombre}, tienes {edad} años")

lista = [3, 1, 2]
lista.sort(); len(lista); sum(lista); max(lista)
texto = "p001".upper()

for i in range(1, 6):        # 1 a 5
    print(i)

def promedio(valores):
    return sum(valores) / len(valores)

with open("archivo.txt", "a", encoding="utf-8") as f:
    f.write("línea\n")
```

Conceptos: [[Variables y tipos de datos]] · [[Listas tuplas y diccionarios]] · [[Condicionales if elif else]] · [[Ciclos for y while]] · [[Funciones y modulos]] · [[Archivos CSV y CRUD]]
