---
tipo: laboratorio
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 6
fecha: 2026-09-27
estado: entregado
calificacion:
aliases: []
tags: [curso/servicios-red]
---

# SRD GLAB-S06 — Proxy Squid

← MOC del curso: [[Servicios de Red]] · Clase: [[SRD S06 - Servicio Proxy]] · Entrega: `entrega/GLAB-S06-ACUEVA-2026-02 (3).docx`

## Objetivo

- Implementar Squid en Linux y definir reglas de acceso a Internet para los clientes.

## Procedimiento

1. Hostname con el formato de la guía (inicial + apellido + `proxy`).
2. Instalar Squid en Ubuntu Server y definir la red local.
3. ACL por dominios y por extensiones (`.exe`, `.zip`, `.mp3`) con `url_regex`.
4. ACL de tiempo para limitar el horario.
5. Probar desde el cliente y revisar `access.log`.

> Comandos usados: [[Squid]]

## Conclusiones (del informe)

- Squid centraliza el acceso a Internet de toda la LAN.
- Filtrar dominios y extensiones reduce riesgos y ahorra ancho de banda.
- Las ACL de tiempo automatizan el control horario; la caché acelera la navegación.

## Relacionado

- [[Proxy y ACL de Squid]]
