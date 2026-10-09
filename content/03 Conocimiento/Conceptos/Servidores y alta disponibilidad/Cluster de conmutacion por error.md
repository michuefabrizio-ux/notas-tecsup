---
tipo: concepto
categoria: Servidores y alta disponibilidad
cursos: ["[[Arquitectura de Servidores]]"]
aliases: ["Clúster de conmutación por error", WSFC, Failover]
tags: []
---

# Clúster de conmutación por error

## Qué es

- Grupo de servidores (**nodos**) que trabajan como uno solo: si un nodo falla, sus servicios pasan a otro (**failover**).

## Cómo funciona

1. Almacenamiento compartido visible por todos los nodos (iSCSI/SAN).
2. **Validación** de la configuración antes de crear el clúster.
3. Nombre e **IP virtual** del clúster (los clientes se conectan a ella, no a un nodo).
4. **Quórum** para decidir qué nodos siguen activos.
5. Prueba: al caer el nodo dueño, los recursos pasan al otro con una interrupción mínima.

## Comparación

| Plataforma | Componentes |
|---|---|
| Windows (WSFC) | Failover Cluster Manager, Hyper-V, testigo de disco o de archivos |
| Linux | Pacemaker + Corosync, normalmente sobre KVM |

## Dónde lo usé

- [[ARQ Lab 05-06 - Cluster de conmutacion por error con iSCSI]] (1 paquete perdido de 253)

## Relacionado

- [[Cuorum y testigo]] · [[SPOF]] · [[Disponibilidad y SLA]] · [[OE3 - Cluster de alta disponibilidad]]
