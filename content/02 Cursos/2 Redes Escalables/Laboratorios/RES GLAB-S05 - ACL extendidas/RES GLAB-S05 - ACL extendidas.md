---
tipo: laboratorio
curso: "[[Redes Escalables]]"
ciclo: 4
periodo: 2026-2
semana: 5
fecha: 2026-09-15
estado: entregado
calificacion:
aliases: ["RES GLAB-S05 - ACL extendidas IPv4"]
tags: [curso/redes-escalables, pi/oe2]
---

# RES GLAB-S05 — ACL extendidas IPv4

← MOC del curso: [[Redes Escalables]] · Entrega: `entrega/GLAB-S05-JURBINA-2026-02.docx`, `entrega/PacketTracer-Semana 5-20260916T033729Z-1-001.zip`

> En la carátula quedó el título "Redundancia LAN con equipos Routers — Laboratorio N.º 3"; el contenido es de ACL extendidas.

## Objetivo

- Configurar ACL extendidas numeradas y nombradas (PT 5.4.12) y resolver el reto 5.5.1 *IPv4 ACL Implementation Challenge*.

## Direccionamiento y equipos

| Dispositivo | Interfaz | IP | Máscara | Gateway |
|---|---|---|---|---|
| R1 | G0/0 | 172.22.34.65 | 255.255.255.224 | N/A |
| R1 | G0/1 | 172.22.34.97 | 255.255.255.240 | N/A |
| R1 | G0/2 | 172.22.34.1 | 255.255.255.192 | N/A |
| Server | NIC | 172.22.34.62 | 255.255.255.192 | 172.22.34.1 |
| PC1 | NIC | 172.22.34.66 | 255.255.255.224 | 172.22.34.65 |
| PC2 | NIC | 172.22.34.98 | 255.255.255.240 | 172.22.34.97 |

## Procedimiento

1. ACL 100: PC1 solo FTP + ICMP al servidor (wildcard de /27 = 0.0.0.31).
2. ACL nombrada: PC2 solo web + ICMP al servidor.
3. Reto 5.5.1: listas 101, 111, `vty_block` en HQ y `branch_to_hq` en Branch.

> Comandos usados: [[IOS - ACL]]

## Respuestas del reto (del informe)

- Ping PC-1 → Branch Server: **denegado** por la 111 (`deny ip 192.168.1.0 0.0.0.63 host 192.168.2.45`).
- Web del External Server → Enterprise Web Server: **permitido** por `permit ip any any` de la 101.
- FTP Internet User → Branch Server: exitoso; para impedirlo, agregar `deny tcp any host 192.168.2.45 eq ftp` en la 101 antes del `permit ip any any`.

## Relacionado

- [[ACL estandar y extendida]] · [[Mascara wildcard]] · [[OE2 - VLAN ACL y DMZ]]
