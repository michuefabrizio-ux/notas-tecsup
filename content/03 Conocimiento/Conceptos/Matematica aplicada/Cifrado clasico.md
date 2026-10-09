---
tipo: concepto
categoria: Matematica aplicada
cursos: ["[[Matematica para las Telecomunicaciones]]"]
aliases: ["Cifrado César", "Cifrado de Hill", "Criptografía"]
tags: []
---

# Cifrado clásico

## Qué es

- Técnicas históricas de criptografía que transforman el texto para que solo quien tiene la clave lo lea. Base de la **aritmética modular** de los cifrados modernos.

## Comparación

| Cifrado | Cómo funciona |
|---|---|
| Sustitución simple | Alfabeto reordenado con una palabra clave (ej.: `MURCIELAGO`) |
| César | Desplazar k posiciones: `C = (P + k) mod 27` (alfabeto español con Ñ) |
| Vigenère | César con una clave que cambia en cada letra |
| Hill | Bloques de letras × matriz clave: `C = K·P mod 27`; descifrar con K⁻¹ (K debe tener determinante ≠ 0 y ser invertible mod 27) |

## Dónde lo usé

- [[MPT Lab 14 - Cifrado informatico]] · [[MPT Lab 15 - Algoritmos de cifrado]]

## Relacionado

- [[TLS y secreto perfecto hacia adelante]] · [[Triada CIA]]
