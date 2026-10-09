---
tipo: laboratorio
curso: "[[Arquitectura de Servidores]]"
ciclo: 4
periodo: 2026-2
semana: 6
fecha: 2026-09-30
estado: entregado
calificacion:
aliases: ["Implementación de un clúster de conmutación por error en Windows Server con almacenamiento iSCSI en TrueNAS"]
tags: [curso/arq-servidores, pi/oe3]
---

# ARQ Lab 05-06 — Clúster de conmutación por error en Windows Server con iSCSI en TrueNAS

← MOC del curso: [[Arquitectura de Servidores]] · Entrega: `entrega/Informe_Laboratorio_Cluster_Failover_Michue (3).docx`

## Objetivo

- Crear un clúster de conmutación por error (WSFC) de dos nodos con almacenamiento compartido iSCSI servido por TrueNAS.

## Direccionamiento y equipos

| Elemento | Dato |
|---|---|
| TrueNAS | 10.160.10.50 · pool `pool-tecsup` (MIRROR, 2 discos) |
| Zvols | `clusterconf` 1 GB (iSCSI), `fsconf` 1 GB, `fsdata` 50 GB |
| Nodos | nodo1 y nodo2 · dominio `hptecsup.local` |
| Clúster | `Cluster1` · IP 10.160.10.60/24 |

## Procedimiento

1. Verificar el pool y crear los zvols en TrueNAS.
2. Iniciador iSCSI en cada nodo (*Auto Configure*); ambos nodos ven el mismo disco de 1 GB.
3. Poner el disco en línea en NODO01.
4. **Validar la configuración** en Failover Cluster Manager (nodos *Validated*, pruebas *Success*).
5. **Crear el clúster** `Cluster1` con IP 10.160.10.60.
6. Verificar con `Get-ClusterGroup`.
7. Prueba de failover: `ping -t 10.160.10.60` desde el AD y caída del nodo02.

> Comandos usados: [[PowerShell - Failover Cluster]]

## Resultado

- 253 paquetes enviados, 252 recibidos: **1 perdido** durante el cambio de nodo.

## Problemas que tuve y cómo los resolví

| Problema | Causa | Solución |
|---|---|---|
| Clúster sin testigo de quórum y almacenamiento *Offline* | El disco compartido no se inicializó antes de crear el clúster | Inicializar y formatear el disco antes de crear el clúster para usarlo como testigo |

## Conclusiones (del informe)

- Dos nodos funcionan como uno solo; al caer uno, el otro tomó el control perdiendo solo 1 paquete de 253.
- iSCSI permite que ambos nodos vean el mismo disco como propio.
- Validar antes de crear el clúster da seguridad.

## Relacionado

- [[Cluster de conmutacion por error]] · [[Almacenamiento compartido iSCSI]] · [[Cuorum y testigo]] · [[OE3 - Cluster de alta disponibilidad]]
