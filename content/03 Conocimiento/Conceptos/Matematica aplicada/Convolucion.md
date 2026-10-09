---
tipo: concepto
categoria: Matematica aplicada
cursos: ["[[Matematica para las Telecomunicaciones]]"]
aliases: ["Convolución", "Integral de convolución"]
tags: []
---

# Convolución

## Qué es

- Operación que da la salida de un sistema lineal e invariante (SLIT) a partir de la entrada x(t) y su respuesta h(t).

## Cómo funciona

- `r(t) = ∫ h(τ)·x(t − τ) dτ`
- Gráficamente: girar x, desplazarla t, multiplicar por h y sacar el área.
- Convolución en el tiempo = **producto en frecuencia** (R(f) = H(f)·X(f)).
- Rect ∗ rect (anchos distintos) = trapecio; rect ∗ rect (iguales) = triángulo.

## Dónde lo usé

- [[MPT Lab 02 - Integral de la convolucion]]

## Relacionado

- [[Serie de Fourier]] · [[Modulacion digital]]
