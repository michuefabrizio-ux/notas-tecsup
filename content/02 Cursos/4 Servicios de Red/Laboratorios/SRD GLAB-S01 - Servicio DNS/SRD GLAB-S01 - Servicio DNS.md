---
tipo: laboratorio
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 1
fecha: 2026-08-24
estado: entregado
calificacion:
aliases: []
tags: [curso/servicios-red]
---

# SRD GLAB-S01 — Servicio DNS

← MOC del curso: [[Servicios de Red]] · Clase: [[SRD S01 - Servicio DNS]] · Entrega: `entrega/GLAB-S01-ACUEVA-2026-02.docx.pdf`

## Objetivo

- Implementar el servicio DNS en una red con equipos Linux.
- Administrar zonas, registros y transferencias DNS.

## Direccionamiento y equipos

- Ubuntu Server 22.04 con BIND9 + cliente Windows (VMware/VirtualBox).
- IP y nombres exactos: ver capturas del informe #pendiente/verificar

## Procedimiento

1. Configurar la red del servidor y verificarla con `ip address` e `ip route`.
2. Instalar BIND9 y abrir el puerto 53 TCP/UDP en **UFW**.
3. Crear zonas directas primarias `tecsup01.xyz`, `acme01.xyz` y `contoso01.xyz` con registros SOA, NS, A, MX y CNAME.
4. Crear la zona inversa (`in-addr.arpa`) con registros PTR.
5. Probar con `dig` (estado `NOERROR`) y `dig -x` para la resolución inversa; comprobar que no resuelve dominios no registrados.

> Comandos usados: [[BIND9]] · [[Bash - Red y diagnostico]]

## Conclusiones (del informe)

- BIND9 quedó funcionando con el servicio `named` y el puerto 53 abierto en UFW.
- Las zonas directas organizan la jerarquía con SOA, NS, A, MX y CNAME; la inversa usa PTR bajo `in-addr.arpa`.
- `dig` y `ping` confirmaron respuestas correctas.

## Relacionado

- [[DNS zona directa e inversa]]
