---
tipo: laboratorio
curso: "[[Cableado Estructurado y Fibra Optica]]"
ciclo: 4
periodo: 2026-2
semana: 2
fecha: 2026-08-28
estado: entregado
calificacion:
aliases: []
tags: [curso/cableado]
---

# CAB Lab 02 — Conexionado de jacks y mediciones de cable de cobre

← MOC del curso: [[Cableado Estructurado y Fibra Optica]] · Clase: [[CAB S02 - Media y componentes de cobre]] · Guía: `guia/GLAB-S02-JVELARDE-2026-1.docx` · Entrega: `entrega/GLAB-S02-JVELARDE-2026-1.pdf`

## Objetivo

- Describir el cable UTP Cat 6, implementar un enlace y evaluarlo según TIA-568-C e ISO/IEC 11801.

## Procedimiento

1. Registrar las especificaciones del rack, patch panel, chaqueta del cable y plugs/jacks Cat 6/6A.
2. Ponchar jacks RJ-45 en **T568A** con la herramienta de impacto.
3. Probar con el **CableIQ**.

## Problemas que tuvimos y cómo los resolvimos

| Problema | Causa | Solución |
|---|---|---|
| Fallo de continuidad en la 1.ª prueba | Pares demasiado abiertos y hoja de corte de la herramienta de impacto al revés | Rehacer el extremo respetando el código de colores, chaqueta pegada al jack; 2.ª prueba: PASS |

## Conclusiones (del informe)

- La rigurosidad al ponchar determina el éxito del enlace.
- Los 8 hilos sin cruces ni cortos; canal apto para Gigabit Ethernet.

## Relacionado

- [[T568A y T568B]] · [[Categorias de cable de cobre]]
