---
tipo: concepto
categoria: Fundamentos de redes
cursos: ["[[Implementacion de Redes]]"]
aliases: ["Encapsulación", PDU]
tags: []
---

# Encapsulación y PDU

## Cómo funciona

- Al bajar por las capas, cada una agrega su encabezado (**encapsulación**); al subir en el destino, se quitan (**desencapsulación**).

| Capa | PDU | Dirección que agrega |
|---|---|---|
| Aplicación | Datos | — |
| Transporte | Segmento (TCP) / datagrama (UDP) | Puertos |
| Red | Paquete | IP origen/destino |
| Enlace | Trama | MAC origen/destino + FCS |
| Física | Bits | — |

- La IP de origen/destino no cambia en el camino; las MAC cambian en cada salto.

## Relacionado

- [[Modelo OSI]] · [[Trama Ethernet]]
