---
tipo: laboratorio
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 2
fecha: 2026-08-31
estado: entregado
calificacion:
aliases: []
tags: [curso/servicios-red]
---

# SRD GLAB-S02 — Servicios Web

← MOC del curso: [[Servicios de Red]] · Clase: [[SRD S02 - Servicios Web]] · Entrega: `entrega/GLAB-S02-ACUEVA-2026-02.docx.pdf`

## Objetivo

- Implementar el servicio web en Linux, configurar Apache y definir sitios web.

## Direccionamiento y equipos

| Dispositivo | IP | Sitios |
|---|---|---|
| Ubuntu Server (apache2) | 172.16.50.11 | `tecsup50.xyz`, `acme50.xyz`, `joomla50.xyz` |

## Procedimiento

1. Instalar `apache2` y abrir 80/TCP y 443/TCP en UFW.
2. Crear Virtual Hosts por nombre para `tecsup50.xyz` y `acme50.xyz`.
3. Instalar la pila LAMP (MariaDB + PHP) y crear la cuenta `joomla_user50`.
4. Desplegar Joomla! 4 en `joomla50.xyz` y probar la consola `/administrator`.
5. Ajustar permisos `www-data:www-data` y `755`.

> Comandos usados: [[Apache httpd]]

## Conclusiones (del informe)

- Los Virtual Hosts permiten alojar dominios independientes en un solo servidor gracias a la cabecera `Host`.
- LAMP dio el procesamiento dinámico para el CMS con permisos acotados en MariaDB.
- Los permisos `www-data` y `755` fueron clave para que PHP funcione sin abrir de más el sistema.

## Relacionado

- [[Servidor web y VirtualHost]] · [[LAMP]]
