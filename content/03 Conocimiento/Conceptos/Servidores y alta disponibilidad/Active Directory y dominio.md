---
tipo: concepto
categoria: Servidores y alta disponibilidad
cursos: ["[[Administracion de Sistemas Operativos]]", "[[Arquitectura de Servidores]]"]
aliases: [AD, "AD DS", "Controlador de dominio"]
tags: []
---

# Active Directory y dominio

## Qué es

- **AD DS**: servicio de directorio de Windows Server que centraliza usuarios, equipos y políticas en un **dominio** (ej.: `hptecsup.local`).
- El **controlador de dominio (DC)** guarda la base de datos del directorio y autentica.

## Cómo funciona

- Estructura: bosque → dominio → **unidades organizativas (OU)** → objetos (usuarios, grupos, equipos).
- Depende del **DNS** para que los equipos encuentren al DC.
- Las **GPO** se vinculan a sitios, dominios u OU.

## Dónde lo usé

- Dominio del clúster en [[ARQ Lab 05-06 - Cluster de conmutacion por error con iSCSI]] · GPO en [[ASO Lab 07 - Directivas de grupo]]

## Relacionado

- [[GPO]] · [[PowerShell - Active Directory]] · [[DNS zona directa e inversa]]
