---
tipo: concepto
categoria: Servicios de red
cursos: ["[[Servicios de Red]]", "[[Implementacion de Redes]]"]
aliases: [DNS, "Zona directa", "Zona inversa"]
tags: []
---

# DNS: zona directa e inversa

## Qué es

- El **DNS** (*Domain Name System*) es un sistema jerárquico y distribuido que traduce nombres a IP.
- **Zona directa** (*forward*): nombre → IP. **Zona inversa** (*reverse*): IP → nombre, bajo `in-addr.arpa`.

## Cómo funciona

- Jerarquía: raíz `.` → TLD (`.pe`, `.com`) → dominio (`tecsup.edu.pe`) → subdominios.
- **FQDN**: nombre completo terminado en punto (`ns1.tecsup.edu.pe.`). Olvidar el punto en un archivo de zona agrega el dominio otra vez.
- El cliente busca en: caché → hostname → archivo `hosts` → servidor DNS.
- **Recursiva**: el servidor resuelve todo. **Iterativa**: devuelve referencias y el cliente sigue.
- Un servidor **autoritativo** con `recursion no` solo responde por sus zonas.
- Zona inversa: se invierten los octetos de red. Ej.: 172.16.50.0/24 → `50.16.172.in-addr.arpa`.

## Registros

| Registro | Uso | Ejemplo |
|---|---|---|
| SOA | Inicio de autoridad (serie `YYYYMMDDNN`) | — |
| NS | Servidor de nombres | `@ NS ns1` |
| A / AAAA | Nombre → IPv4 / IPv6 | `www A 192.168.1.10` |
| CNAME | Alias | `ftp CNAME www` |
| MX | Servidor de correo con prioridad | `@ MX 10 mail` |
| PTR | IP → nombre | `10 PTR www.dominio.` |
| TXT | Texto (SPF, DKIM) | `@ TXT "v=spf1 mx -all"` |

## Dónde lo usé

- [[SRD GLAB-S01 - Servicio DNS]] · [[SRD PC1 - DNS autoritativo en RHEL]] · [[SRD GLAB-S05 - DNS Web FTP y Correo]] · [[SRD PC3 - Servicios en RHEL]]

## Relacionado

- [[BIND9]] · [[Correo SMTP e IMAP]] · [[CMD - Red]]
