---
tipo: concepto
categoria: Servicios de red
cursos: ["[[Servicios de Red]]"]
aliases: ["Pila LAMP"]
tags: []
---

# LAMP

## Qué es

- Pila de software para sitios dinámicos: **L**inux + **A**pache + **M**ariaDB/MySQL + **P**HP.

## Cómo funciona

- Apache recibe la petición, PHP genera la página y consulta la base de datos MariaDB.
- Sobre LAMP se instalan CMS como **WordPress**, **Joomla** o **Drupal**.
- Buenas prácticas: `mariadb-secure-installation`, un usuario de base de datos propio por aplicación con permisos mínimos.
- En RHEL con SELinux: `httpd_sys_content_t` para lectura y `httpd_sys_rw_content_t` donde el CMS debe escribir.

## Dónde lo usé

- [[SRD GLAB-S02 - Servicios Web]] (Joomla! 4 con `joomla_user50`) · [[SRD GLAB-S04 - Servicio de Correo]] (usuarios virtuales en MariaDB)

## Relacionado

- [[Servidor web y VirtualHost]] · [[Apache httpd]]
