---
tipo: clase
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 6
fecha: 2026-09-23
estado: entregado
calificacion:
aliases: []
tags: [curso/servicios-red]
---

# SRD S06 — Servicio Proxy (Squid)

← MOC del curso: [[Servicios de Red]] · Fuente: `Material/PPT-S06-ACUEVA-2026-02.pptx`, `Material/MTP-S06-ACUEVA-2026-02.docx`, `Material/06 Servicio Proxy.pdf`

## Tema de la sesión

- Proxy caché **Squid** (6.10 en RHEL 10): ACL, reglas de acceso, autenticación y caché.

## Lo esencial

- Un proxy es intermediario entre clientes e Internet: **caché**, **filtrado** y **auditoría**.
- Tipos: forward explícito, forward transparente (requiere NAT) y **proxy inverso** (protege servidores internos).
- Puerto por defecto **3128**; configuración en `/etc/squid/squid.conf`; logs en `/var/log/squid/access.log`.
- Control de acceso en dos pasos: **definir la ACL** (`acl nombre tipo valores`) y **aplicar la acción** (`http_access allow|deny`).
- Tipos de ACL: `src`, `dst`, `dstdomain`, `url_regex`, `time`.
- Se evalúa en **orden** y gana la primera coincidencia; `http_access deny all` va al final.
- Caso del docente: "AndinaTech S.A." — TI con acceso total; Operaciones sin redes sociales ni streaming de 08:00 a 18:00.

## Conceptos, comandos y normas vistos

- [[Proxy y ACL de Squid]] · [[Squid]] · [[SELinux]]
