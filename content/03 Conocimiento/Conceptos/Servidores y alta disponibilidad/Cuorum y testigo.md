---
tipo: concepto
categoria: Servidores y alta disponibilidad
cursos: ["[[Arquitectura de Servidores]]"]
aliases: ["Quórum", "Testigo de quórum"]
tags: []
---

# Cuórum y testigo

## Qué es

- **Cuórum**: mayoría de "votos" necesaria para que el clúster siga funcionando.
- **Testigo**: voto extra (disco, recurso compartido de archivos o nube) que rompe el empate en clústeres con número par de nodos.

## Cómo funciona

- Con 2 nodos + testigo hay 3 votos: si cae un nodo, quedan 2 de 3 y el clúster sigue.
- Sin testigo, un clúster de 2 nodos puede quedarse sin mayoría o caer en **split-brain**.

## Dónde lo usé

- [[ARQ Lab 05-06 - Cluster de conmutacion por error con iSCSI]]: quedó sin testigo porque el disco no se inicializó antes de crear el clúster.

## Relacionado

- [[Split-brain]] · [[Cluster de conmutacion por error]] · [[OE3 - Cluster de alta disponibilidad]]
