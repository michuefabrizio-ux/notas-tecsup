---
tipo: laboratorio
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 4
fecha: 2026-09-15
estado: entregado
calificacion:
aliases: []
tags: [curso/servicios-red]
---

# SRD GLAB-S04 — Servicio de Correo

← MOC del curso: [[Servicios de Red]] · Clase: [[SRD S04 - Servicio de Correo]] · Entrega: `entrega/GLAB-S04-ACUEVA-2026-02.docx`

## Objetivo

- Instalar y configurar los componentes SMTP y POP3/IMAP del servidor de correo y probar un cliente web.

## Procedimiento

1. Instalar Postfix y Dovecot (Ubuntu Server 22.04).
2. Configurar **usuarios virtuales** guardados en **MariaDB**.
3. Conectar Dovecot a la base de datos (mismo esquema de contraseña en la config y en la tabla).
4. Instalar **Roundcube Webmail** sobre Apache2 y probar envío, recepción y alias.

> Comandos usados: [[Postfix y Dovecot]]

## Problemas que tuve y cómo los resolví

| Problema | Causa | Solución |
|---|---|---|
| Sintaxis rechazada | Dovecot 2.4+ y MariaDB 11+ cambiaron directivas y funciones de cifrado | Adaptar la configuración a la versión instalada |

## Conclusiones (del informe)

- Los usuarios virtuales en MariaDB separan las cuentas de correo de los usuarios del sistema.
- Roundcube permite validar el envío, la recepción y los alias de forma visual.

## Relacionado

- [[Correo SMTP e IMAP]]
