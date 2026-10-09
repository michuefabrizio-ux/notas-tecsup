---
tipo: concepto
categoria: Matematica aplicada
cursos: ["[[Matematica para las Telecomunicaciones]]"]
aliases: ["Entropía", Huffman, "Shannon-Fano"]
tags: []
---

# Entropía y codificación de fuente

## Fórmulas

- Información de un símbolo: `I = log₂(1/p)` bits.
- **Entropía**: `H = Σ pᵢ·log₂(1/pᵢ)` bits/símbolo (información promedio de la fuente).
- Longitud media: `L = Σ pᵢ·lᵢ`.
- **Eficiencia**: `η = H / L`; **redundancia**: `1 − η`.

## Métodos

- **Shannon-Fano** (de arriba abajo): ordenar por probabilidad, dividir en dos grupos de probabilidad lo más parecida posible, asignar 0/1, repetir.
- **Huffman** (de abajo arriba): unir siempre los dos símbolos menos probables hasta formar el árbol; es **óptimo**.
- Si todas las probabilidades son potencias de 2, ambos dan η = 100 %.

## Dónde lo usé

- [[MPT Lab 11 - Medida de la informacion]] · [[MPT Lab 12 - Huffman y Shannon-Fano]]

## Relacionado

- [[Ancho de banda de VoIP y CODEC]]
