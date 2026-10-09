---
tipo: concepto
categoria: Servidores y alta disponibilidad
cursos: ["[[Arquitectura de Servidores]]"]
aliases: [iSCSI]
tags: []
---

# Almacenamiento compartido iSCSI

## Qué es

- **iSCSI** transporta comandos SCSI sobre TCP/IP (puerto 3260): el servidor ve un disco remoto como si fuera local (almacenamiento por **bloques**).

## Cómo funciona

- **Target**: quien ofrece el disco (ej.: TrueNAS con un zvol).
- **Initiator**: quien lo consume (ej.: Iniciador iSCSI de Windows en cada nodo).
- **LUN**: la unidad lógica entregada.
- En un clúster, todos los nodos ven el mismo LUN, pero solo el dueño del recurso lo usa a la vez.

## Dónde lo usé

- [[ARQ Lab 05-06 - Cluster de conmutacion por error con iSCSI]]

## Relacionado

- [[SAN y NAS]] · [[Cluster de conmutacion por error]]
