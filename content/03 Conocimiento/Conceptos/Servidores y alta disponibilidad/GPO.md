---
tipo: concepto
categoria: Servidores y alta disponibilidad
cursos: ["[[Administracion de Sistemas Operativos]]"]
aliases: ["Directivas de grupo", "Group Policy"]
tags: []
---

# GPO (directivas de grupo)

## Qué es

- Conjunto de configuraciones que AD aplica automáticamente a usuarios y equipos, sin tocar cada máquina.

## Cómo funciona

- Se crean en *Group Policy Management* y se **vinculan** a sitio, dominio u OU.
- Orden de aplicación: local → sitio → dominio → OU (la última gana).
- **Filtrado de seguridad**: aplicar la GPO solo a ciertos grupos.
- **Almacén central**: plantillas ADMX en `SYSVOL\Policies\PolicyDefinitions` para todo el dominio.
- Forzar y verificar: `gpupdate /force`, `gpresult /r`.

## Dónde lo usé

- [[ASO Lab 07 - Directivas de grupo]] · [[ASO Proyecto - Entorno tipo kiosko mediante GPO]]

## Relacionado

- [[Active Directory y dominio]]
