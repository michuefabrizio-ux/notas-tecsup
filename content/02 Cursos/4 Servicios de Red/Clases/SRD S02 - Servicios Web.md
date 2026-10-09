---
tipo: clase
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 2
fecha:
estado: entregado
calificacion:
aliases: []
tags: [curso/servicios-red]
---

# SRD S02 — Servicios Web

← MOC del curso: [[Servicios de Red]] · Fuente: `Material/MTP-S02-ACUEVA-2026-02.docx`, `Material/02 Servicios Web.pdf` (el `PPT-S02` no se pudo abrir: archivo dañado)

## Tema de la sesión

- Servidor web **Apache httpd** (y NGINX) en RHEL 10, **Virtual Hosts** y pila **LAMP** con un CMS.

## Lo esencial

- Ciclo de una petición HTTP: conexión TCP (80/443) → petición (método, URI, cabeceras) → procesamiento → respuesta con código (200, 404…) → cierre o *keep-alive*.
- Apache: proceso padre como root + procesos/hilos hijos según el **MPM**; es modular. NGINX usa arquitectura asíncrona por eventos.
- **Virtual Hosts por nombre**: varios dominios en una misma IP; Apache elige el sitio por la cabecera `Host`.
- Rutas clave: `/etc/httpd/conf/httpd.conf`, `/etc/httpd/conf.d/`, `/var/www/html/`, `/var/log/httpd/`.
- Contextos SELinux: `httpd_sys_content_t` (solo lectura), `httpd_sys_rw_content_t` (escritura por scripts), `http_port_t` (puertos permitidos).
- **LAMP**: Linux + Apache + MariaDB + PHP; base para WordPress, Joomla o Drupal.

## Conceptos, comandos y normas vistos

- [[Servidor web y VirtualHost]] · [[LAMP]] · [[Apache httpd]] · [[SELinux modos y contextos]]
