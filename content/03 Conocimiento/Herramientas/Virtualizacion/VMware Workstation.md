---
tipo: herramienta
categoria: Virtualizacion
cursos: ["[[Ethical Hacking]]", "[[Servicios de Red]]"]
aliases: [VMware]
tags: []
---

# VMware Workstation

## Qué es

- Hipervisor de tipo 2 (corre sobre Windows o Linux) para crear máquinas virtuales.

## Modos de red

| Modo | Uso |
|---|---|
| Bridged | La VM sale a la red física como un equipo más |
| NAT | La VM navega a través de la IP del host |
| Host-only | Red aislada entre host y VMs |
| LAN Segment | Red aislada solo entre VMs |

- Se configura en *Edit → Virtual Network Editor*.

## Para qué la usé

- Labs de Ethical Hacking (redes NAT y host-only): [[EH Lab02 - Escaneo de redes]]
- Labs de Servicios de Red (servidor + cliente Windows): [[SRD GLAB-S01 - Servicio DNS]]

## Relacionado

- [[Virtualizacion e hipervisores]] · [[Oracle VirtualBox]]
