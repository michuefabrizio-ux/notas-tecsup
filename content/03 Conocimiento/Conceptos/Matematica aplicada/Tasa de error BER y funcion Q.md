---
tipo: concepto
categoria: Matematica aplicada
cursos: ["[[Matematica para las Telecomunicaciones]]"]
aliases: [BER, "Función Q", "Probabilidad de error"]
tags: []
---

# Tasa de error (BER) y función Q(x)

## Qué es

- **BER**: proporción de bits recibidos con error. En presencia de ruido blanco gaussiano se calcula con la función **Q(x)**.

## Cómo funciona

- Ruido gaussiano: media 0, varianza σ². `Q(x) = P(X > x)` para una normal estándar (área de la cola).
- La Pe depende de la distancia entre niveles frente al ruido: más SNR → menor Q → menos errores.
- El **filtro acoplado** maximiza la SNR en el instante de muestreo y da menor Pe que un filtro pasa bajos.
- Ejemplo de mi lab (AMI-NRZ): filtro acoplado 2,09 × 10⁻¹² vs LPF 5,82 × 10⁻⁷.

## Dónde lo usé

- [[MPT Lab 05 - Variables aleatorias]] · [[MPT Lab 06 - Tasa de error y funcion Q]]

## Relacionado

- [[Modulacion digital]] · [[Codigos de deteccion y correccion de errores]]
