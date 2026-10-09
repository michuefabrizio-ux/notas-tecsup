---
tipo: evaluacion
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana:
fecha:
estado: entregado
calificacion:
aliases: ["Práctica Calificada 2"]
tags: [curso/servicios-red]
---

# SRD PC2 — DNS, Web y FTP en RHEL 10

← MOC del curso: [[Servicios de Red]] · Entrega: `entrega/Práctica Calificada 2 (LABORATORIO) (1).docx`

## Escenario

- "Corporación TecnoAndes S.A.", dominio `tecnoandes.lab`; todo en un servidor RHEL 10 con SELinux *enforcing* y firewalld.

| Equipo | FQDN | IP | Gateway |
|---|---|---|---|
| Servidor RHEL 10 | ns1.tecnoandes.lab | 192.168.100.10/24 | 192.168.100.1 |
| Web (mismo) | www.tecnoandes.lab | 192.168.100.20/24 | 192.168.100.1 |
| FTP (mismo) | ftp.tecnoandes.lab | 192.168.100.30/24 | 192.168.100.1 |
| Cliente | — | 192.168.100.50/24 | 192.168.100.1 |

## Requerimientos

- DNS autoritativo + recursión solo para la subred corporativa.
- Portal web con contenido **fuera de `/var/www/html`**.
- FTP solo para usuarios locales, enjaulados con chroot (proveedores suben facturas).

## Problemas que tuve y cómo los resolví

| Problema | Solución |
|---|---|
| vsftpd rechaza un home con escritura en el chroot | `chmod a-w /home/proveedor1` y subcarpeta `/upload` con contexto `public_content_rw_t` |

## Conclusiones (de mi entrega)

- Consolidar servicios ahorra recursos, pero exige segmentar bien.
- firewalld con mínimo privilegio: solo 53, 80, 21 y el rango pasivo 10000-10100/tcp.
- SELinux *enforcing* (MAC) aísla los procesos aunque el servicio tenga una vulnerabilidad.

## Relacionado

- [[FTP activo y pasivo]] · [[vsftpd]] · [[Servidor web y VirtualHost]] · [[Minimo privilegio]]
