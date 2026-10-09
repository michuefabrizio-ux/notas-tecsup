---
tipo: concepto
categoria: Fundamentos de redes
cursos: ["[[Implementacion de Redes]]"]
aliases: [OSI]
tags: []
---

# Modelo OSI

## Capas

| N.º | Capa | PDU | Ejemplos |
|---|---|---|---|
| 7 | Aplicación | Datos | HTTP, DNS, SMTP |
| 6 | Presentación | Datos | Cifrado, compresión, formatos |
| 5 | Sesión | Datos | Control de diálogo |
| 4 | Transporte | Segmento | TCP, UDP |
| 3 | Red | Paquete | IP, ICMP, OSPF |
| 2 | Enlace de datos | Trama | Ethernet, 802.11, HDLC |
| 1 | Física | Bits | Cable, fibra, radio |

- Truco: "**F**ísica **E**nlace **R**ed **T**ransporte **S**esión **P**resentación **A**plicación".

## Dónde lo usé

- [[IMR M03 - Protocolos y modelos]] · [[SOA Lab 15 - Mitigacion de DoS]] (DoS en capas 4 y 7)

## Relacionado

- [[Modelo TCP-IP]] · [[Encapsulacion y PDU]]
