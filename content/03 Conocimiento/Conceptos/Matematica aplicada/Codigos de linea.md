---
tipo: concepto
categoria: Matematica aplicada
cursos: ["[[Matematica para las Telecomunicaciones]]"]
aliases: ["Códigos de línea", NRZ, Manchester, AMI, "HDB-3"]
tags: []
---

# Códigos de línea

## Qué es

- Forma de representar los bits como niveles de voltaje para transmitirlos en **banda base** por un cable.

## Comparación

| Código | Idea | Ventaja | Desventaja |
|---|---|---|---|
| NRZ | El nivel se mantiene todo el bit | Poco ancho de banda | Componente DC, pierde sincronía con muchos bits iguales |
| RZ | Vuelve a 0 a mitad del bit | Mejor sincronía | Doble ancho de banda |
| Manchester (bifase) | Transición en mitad de cada bit | Autosincronizante (Ethernet 10 Mb/s) | Doble ancho de banda |
| AMI (bipolar) | Los 1 alternan +V y −V; el 0 es 0 V | Sin DC, detecta errores | Pierde sincronía con muchos 0 |
| HDB-3 | AMI que sustituye 4 ceros seguidos por un patrón con violación | Mantiene la sincronía | Más complejo |
| Multinivel | Varios bits por símbolo | Menos baudios | Más sensible al ruido |

## Dónde lo usé

- [[MPT Lab 03 - Codigos de linea]] · [[MPT Lab 06 - Tasa de error y funcion Q]] (AMI-NRZ)

## Relacionado

- [[Modulacion digital]] · [[Trama Ethernet]]
