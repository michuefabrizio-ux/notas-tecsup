---
tipo: laboratorio
curso: "[[Servicios de Red]]"
ciclo: 4
periodo: 2026-2
semana: 7
fecha: 2026-10-07
estado: entregado
calificacion:
aliases: []
tags: [curso/servicios-red]
---

# SRD GLAB-S07 — Firewall iptables

← MOC del curso: [[Servicios de Red]] · Clase: [[SRD S07 - Servicio Firewall]] · Entrega: `entrega/GLAB-S07-ACUEVA-2026-02 (3).docx`

## Objetivo

- Implementar iptables en Linux y definir reglas de acceso a los recursos del servidor.

## Procedimiento

1. Hostname con el formato de la guía (inicial + apellido + `fw`).
2. Política por defecto **DROP** en INPUT.
3. Reglas por IP de origen (`-s`), protocolo (`-p`) y puerto (`--dport`) con permisos distintos para Cli1 y Cli2 (ping, SSH, web, FTP).
4. Comparar DROP y REJECT desde los clientes.
5. Guardar las reglas con `iptables-save` / `iptables-persistent`.

> Comandos usados: [[iptables]]

## Conclusiones (del informe)

- La cadena más importante para proteger el servidor es **INPUT**.
- Con política DROP se permite solo lo necesario.
- El orden importa: gana la primera regla que coincide.
- DROP no responde; REJECT avisa al cliente.
- Las reglas no son permanentes si no se guardan.

## Relacionado

- [[Cadenas de iptables]] · [[Politicas DROP vs REJECT]] · [[Zonas de firewalld]] · [[OE4 - Bastionado del portal web]]
