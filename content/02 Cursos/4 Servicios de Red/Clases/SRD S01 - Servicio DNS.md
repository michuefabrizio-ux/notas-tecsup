---
tipo: clase
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 1
fecha:
estado: entregado
calificacion:
aliases: ["SRD S01 - Servicio DNS"]
tags: [curso/servicios-red]
---

# SRD S01 — Servicio DNS

← MOC del curso: [[Servicios de Red]] · Fuente: `Material/PPT-S01-ACUEVA-2026-02.pptx`, `Material/MTP-S01-ACUEVA-2026-02.docx`, `Material/01 Servicio DNS.pdf`

## Tema de la sesión

- Funcionamiento del DNS e implementación de un servidor **BIND** autoritativo en RHEL 10.

## Lo esencial

- El **DNS** traduce nombres a IP (**búsqueda directa**) e IP a nombres (**búsqueda inversa**).
- Jerarquía en árbol invertido: **raíz (.)** → **TLD** (.com, .pe) → segundo nivel (tecsup.edu.pe) → subdominios.
- **FQDN**: nombre completo con el punto final (ej.: `ns1.tecsup.edu.pe.`).
- Partes: **cliente DNS** (resolver), **servidor DNS** y **zonas de autoridad**.
- Orden de resolución en el cliente: caché DNS → hostname → archivo `hosts` → servidor DNS; el resultado se guarda en caché.
- **Recursiva**: el servidor resuelve todo por el cliente. **Iterativa**: el servidor devuelve la mejor referencia y el cliente sigue preguntando.
- Registros críticos: SOA, NS, A, AAAA, CNAME, MX, PTR, TXT (SPF).
- En RHEL 10: `/etc/named.conf` (principal) y `/var/named/` (zonas). Siempre validar con `named-checkconf` y `named-checkzone` antes de reiniciar.
- Seguridad: permisos `root:named` 640, `restorecon` de SELinux y `firewall-cmd --add-service=dns`. RHEL 10 trae DNS sobre TLS (DoT) como *Technology Preview* y el demonio `dnsconfd`.
- Caso de práctica del docente: "CrediSeguro S.A.", dominio `crediseguro.local`, red 10.10.0.0/16.

## Conceptos, comandos y normas vistos

- [[DNS zona directa e inversa]] · [[BIND9]] · [[SELinux]] · [[firewalld]] · [[RHEL]]

## Dudas y pendientes

- [ ] Fecha de la sesión #pendiente/verificar
