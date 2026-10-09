---
tipo: laboratorio
curso: "[[Redes Escalables]]"
ciclo: 4
periodo: 2026-2
semana: 4
fecha: 2026-09-08
estado: entregado
calificacion:
aliases: ["RES GLAB-S04 - ACL estándar IPv4"]
tags: [curso/redes-escalables, pi/oe2]
---

# RES GLAB-S04 — ACL estándar IPv4

← MOC del curso: [[Redes Escalables]] · Entrega: `entrega/GLAB-S04-JURBINA-2026-02 (1).docx`, `entrega/Packet Tracer ACL (2).zip`

> En la carátula del informe quedó el título de plantilla "Certificación de cableado estructurado — Laboratorio N.º 3"; el contenido es de ACL estándar.

## Objetivo

- Planificar, configurar, aplicar y verificar ACL estándar numeradas y nombradas (PT 5.1.8, 5.1.9 y 5.2.7).

## Direccionamiento y equipos

| Dispositivo | Interfaz | IP | Máscara | Gateway |
|---|---|---|---|---|
| R1 | G0/0 | 192.168.10.1 | 255.255.255.0 | N/A |
| R1 | G0/1 | 192.168.11.1 | 255.255.255.0 | N/A |
| R2 | G0/0 | 192.168.20.1 | 255.255.255.0 | N/A |
| R3 | G0/0 | 192.168.30.1 | 255.255.255.0 | N/A |
| PC1 | NIC | 192.168.10.10 | 255.255.255.0 | 192.168.10.1 |
| PC2 | NIC | 192.168.11.10 | 255.255.255.0 | 192.168.11.1 |
| PC3 | NIC | 192.168.30.10 | 255.255.255.0 | 192.168.30.1 |
| WebServer | NIC | 192.168.20.254 | 255.255.255.0 | 192.168.20.1 |

## Procedimiento

1. Verificar conectividad completa (EIGRP ya configurado).
2. R2: la red 192.168.11.0/24 no accede al WebServer → ACL 1 en la salida hacia el WebServer + `permit any`.
3. R3: la red 192.168.10.0/24 no se comunica con 192.168.30.0/24 → ACL en la salida hacia PC3 + `permit any`.
4. Verificar con `show access-lists` y pings.

> Comandos usados: [[IOS - ACL]]

## Conclusiones (del informe)

- La ACL estándar filtra solo por IP de origen.
- Hace falta `permit any` al final; si no, el *deny* implícito bloquea todo.
- La ACL estándar va lo más cerca posible del **destino**.
- `show access-lists` muestra los *matches* para comprobar el efecto.

## Relacionado

- [[ACL estandar y extendida]] · [[Mascara wildcard]]
