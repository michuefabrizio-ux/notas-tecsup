---
tipo: concepto
categoria: Servicios de red
cursos: ["[[Servicios de Red]]"]
aliases: [VirtualHost, "Virtual Hosts", HTTP]
tags: []
---

# Servidor web y VirtualHost

## Qué es

- Un **servidor web** entrega contenido por HTTP (80) o HTTPS (443). En Linux: **Apache httpd** o **NGINX**; en Windows: **IIS**.
- Un **VirtualHost** permite alojar varios sitios en un solo servidor.

## Cómo funciona

- Petición HTTP: conexión TCP → método + URI + cabeceras → procesamiento → código de estado (200, 404…) → cierre o *keep-alive*.
- **VirtualHost por nombre**: varios dominios en la misma IP; Apache elige el sitio por la cabecera `Host`.
- **VirtualHost por IP**: cada sitio tiene su propia IP.
- Apache: proceso padre (root) + hijos según el MPM. NGINX: asíncrono por eventos, menos recursos por conexión.
- Si se pide un nombre que no tiene VirtualHost, se muestra el sitio por defecto.

## Comparación

| Aspecto | Apache httpd | NGINX |
|---|---|---|
| Modelo | Procesos/hilos (MPM) | Eventos asíncronos |
| Configuración | `.conf` + `.htaccess` | `nginx.conf`, sin `.htaccess` |
| Uso típico | LAMP, CMS | Alto tráfico, proxy inverso |

## Dónde lo usé

- [[SRD GLAB-S02 - Servicios Web]] · [[SRD PC2 - DNS Web y FTP en RHEL]] · [[SRD GLAB-S05 - DNS Web FTP y Correo]]

## Relacionado

- [[Apache httpd]] · [[LAMP]] · [[SELinux modos y contextos]] · [[OE4 - Bastionado del portal web]]
