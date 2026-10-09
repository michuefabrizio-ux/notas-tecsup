---
tipo: laboratorio
curso: "[[Arquitectura de Servidores]]"
ciclo: 4
periodo: 2026-2
semana: 4
fecha: 2026-08-09
estado: entregado
calificacion:
aliases: ["Despliegue de servidores web heterogéneos con almacenamiento centralizado en TrueNAS (RAID 1 y RAID 5)"]
tags: [curso/arq-servidores, pi/oe3]
---

# ARQ Lab 04 — Servidores web heterogéneos con almacenamiento TrueNAS (RAID 1 y RAID 5)

← MOC del curso: [[Arquitectura de Servidores]] · Entrega: `entrega/Guia_Laboratorio_04_TrueNAS-1.docx` (y `Guia_Laboratorio_04_TrueNAS.docx`) · Fecha de entrega: 2026-08-15

## Objetivo

- Centralizar el almacenamiento en **TrueNAS** (OpenZFS) y publicarlo a un servidor web Windows por **SMB** y a uno Linux por **NFS**; probar la resiliencia ante falla de discos.

## Direccionamiento y equipos

| Dispositivo | Rol | IP |
|---|---|---|
| Gateway | Enrutamiento perimetral | 10.160.10.2 |
| TrueNAS | NAS (OpenZFS) | 10.160.10.50 |
| SRV-WEB-WIN | Windows Server 2022 + IIS (SMB, TCP 445) | 10.160.10.51 |
| SRV-WEB-LNX | Ubuntu Server + Apache (NFS, 2049) | 10.160.10.52 |

| Disco | Capacidad | Uso |
|---|---|---|
| Disco 0 | 20 GB | Sistema TrueNAS |
| Discos 1 y 2 | 100 GB c/u | RAID 1 (Mirror) → Windows |
| Discos 3, 4 y 5 | 100 GB c/u | RAID 5 (RAIDZ1) → Linux |

## Procedimiento

1. **Fase 1**: crear `Pool-Mirror` (RAID 1) y `Pool-RAID5` (RAIDZ1), datasets y shares SMB/NFS.
2. **Fase 2**: IIS en Windows apuntando al share SMB y Apache en Linux apuntando al export NFS.
3. **Fase 3**: desconectar discos en VMware en caliente y comprobar que los sitios siguen arriba.
4. **Fase 4**: reflexión crítica (SMB vs NFS, desacoplar datos, redundancia vs uptime).

## Conclusiones

- Revisar en el informe si están desarrolladas las notas de reflexión (Fase 4 = 50 % de la nota) #pendiente/verificar

## Relacionado

- [[RAID]] · [[SAN y NAS]] · [[NFSv4]] · [[TrueNAS]] · [[OE3 - Cluster de alta disponibilidad]]
