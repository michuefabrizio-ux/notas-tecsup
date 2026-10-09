---
tipo: comando
categoria: Windows
cursos: ["[[Arquitectura de Servidores]]"]
aliases: []
tags: []
---

# PowerShell — Failover Cluster

```powershell
Install-WindowsFeature Failover-Clustering -IncludeManagementTools
Test-Cluster -Node nodo1, nodo2
New-Cluster -Name Cluster1 -Node nodo1, nodo2 -StaticAddress 10.160.10.60
Get-Cluster
Get-ClusterNode
Get-ClusterGroup
Get-ClusterResource
Set-ClusterQuorum -DiskWitness "Cluster Disk 1"
Move-ClusterGroup -Name "Cluster Group" -Node nodo1
```

## Prueba de failover

```powershell
ping -t 10.160.10.60
```

Concepto: [[Cluster de conmutacion por error]] · Lab: [[ARQ Lab 05-06 - Cluster de conmutacion por error con iSCSI]]
