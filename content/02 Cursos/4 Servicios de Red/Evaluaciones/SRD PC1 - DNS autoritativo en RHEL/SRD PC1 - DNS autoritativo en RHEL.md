---
tipo: evaluacion
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana:
fecha:
estado: entregado
calificacion:
aliases: ["Práctica Calificada 1"]
tags: [curso/servicios-red]
---

# SRD PC1 — DNS autoritativo en RHEL 10

← MOC del curso: [[Servicios de Red]] · Guía: `guia/Práctica Calificada 1 (LABORATORIO).docx` · Entrega: `entrega/Práctica Calificada 1 (LABORATORIO) (3).docx`

## Escenario

- Empresa "TechVanguard", dominio `corp.redes.lab`, red 172.16.50.0/24, 120 minutos.

| Equipo | FQDN | IP |
|---|---|---|
| DNS | ns1.corp.redes.lab | 172.16.50.10 |
| Web | www | 172.16.50.20 |
| Correo | mail | 172.16.50.30 |

## Requerimientos

1. Hostname estático, IP 172.16.50.10/24, gateway 172.16.50.1, DNS propio (127.0.0.1) y firewalld solo con DNS.
2. BIND autoritativo: `recursion no`, DNSSEC, `allow-query` solo localhost y la red interna.
3. Zona directa: SOA (serie `YYYYMMDDNN`), A, CNAME `intranet`, MX 10, TXT SPF `v=spf1 mx -all`; zona inversa con PTR.
4. `named-checkconf` / `named-checkzone`, permisos `root:named` 640, `restorecon`, habilitar `named` y probar con `dig`.

## Conclusiones (de mi entrega)

- Con `recursion no` el servidor solo responde con autoridad y no actúa como resolver abierto.
- La zona inversa invierte los octetos: 172.16.50.0/24 → `50.16.172.in-addr.arpa`.
- Permisos, SELinux y firewalld son capas independientes de seguridad.
- La mayoría de errores fueron de sintaxis (el punto final del FQDN en el SOA), y las herramientas de validación los detectan.

## Relacionado

- [[DNS zona directa e inversa]] · [[BIND9]] · [[SELinux modos y contextos]]
