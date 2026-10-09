---
tipo: concepto
categoria: Servicios de red
cursos: ["[[Servicios de Red]]"]
aliases: [Proxy, "Proxy inverso"]
tags: []
---

# Proxy y ACL de Squid

## Qué es

- Un **proxy** es un intermediario entre los clientes e Internet que ofrece **caché**, **filtrado** y **auditoría**.

## Tipos

| Tipo | Flujo | Uso |
|---|---|---|
| Forward explícito | Cliente → Proxy → Internet | El cliente tiene configurado el proxy |
| Forward transparente | Cliente → Gateway → Proxy → Internet | Se intercepta con NAT, sin configurar el cliente |
| Inverso | Internet → Proxy → Servidores internos | Protege y balancea servidores web |

## Cómo funcionan las ACL

1. **Definir**: `acl <nombre> <tipo> <valores>`.
2. **Aplicar**: `http_access allow|deny <nombre>`.

| Tipo | Filtra por | Ejemplo |
|---|---|---|
| `src` | IP/red de origen | `acl PC src 192.168.10.1` |
| `dst` | IP de destino | — |
| `dstdomain` | Dominio | `acl dominio dstdomain sony.com` |
| `url_regex` | Texto en la URL | `acl palabras url_regex .mp3 .zip` |
| `time` | Horario | `acl tiempo time 08:00-22:30` |

- Las reglas se leen **en orden** y gana la **primera coincidencia**. `http_access deny all` siempre al final.
- Códigos en `access.log`: `TCP_DENIED/403` (bloqueado), `TCP_DENIED/407` (falta autenticación).

## Dónde lo usé

- [[SRD GLAB-S06 - Proxy Squid]]

## Relacionado

- [[Squid]] · [[ACL estandar y extendida]]
