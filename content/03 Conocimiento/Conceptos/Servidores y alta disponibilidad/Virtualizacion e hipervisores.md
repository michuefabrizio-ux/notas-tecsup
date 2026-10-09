---
tipo: concepto
categoria: Servidores y alta disponibilidad
cursos: ["[[Administracion de Sistemas Operativos]]", "[[Arquitectura de Servidores]]"]
aliases: [Hipervisor, "Máquina virtual"]
tags: []
---

# Virtualización e hipervisores

## Qué es

- Ejecutar varias **máquinas virtuales** aisladas sobre un mismo hardware mediante un **hipervisor**.

## Comparación

| Tipo | Corre sobre | Ejemplos |
|---|---|---|
| Tipo 1 (bare-metal) | El hardware | Hyper-V, VMware ESXi, KVM |
| Tipo 2 (alojado) | Un sistema operativo | VMware Workstation, VirtualBox |

- Ventajas: consolidar servidores, *snapshots/checkpoints*, clonar con plantillas (Sysprep en Windows), alta disponibilidad con migración en vivo.

## Dónde lo usé

- [[ASO Lab 09 - Virtualizacion con Hyper-V]] · Todos los labs con [[VMware Workstation]]

## Relacionado

- [[Hyper-V]] · [[KVM]] · [[Migracion en vivo]]
