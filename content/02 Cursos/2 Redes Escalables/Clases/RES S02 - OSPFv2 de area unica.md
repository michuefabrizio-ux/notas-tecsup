---
tipo: clase
curso: "[[Redes Escalables]]"
ciclo: 4
periodo: 2026-2
semana: 2
fecha:
estado: entregado
calificacion:
aliases: ["RES S02 - OSPFv2 de área única"]
tags: [curso/redes-escalables]
---

# RES S02 — OSPFv2 de área única

← MOC del curso: [[Redes Escalables]] · Fuente: `Material/PPT-S02-JURBINA-2025-2.pdf` (CCNA ENSA, módulo 2)

## Tema de la sesión

- Configuración de OSPFv2 en redes punto a punto y multiacceso.

## Lo esencial

- **Router ID** explícito (`router-id`), si no se toma la loopback o la IP más alta.
- `network <red> <wildcard> area 0` o `ip ospf <proceso> area 0` en la interfaz.
- **Interfaces pasivas**: no envían Hellos hacia las LAN.
- Loopback anunciada como /32; con `ip ospf network point-to-point` se anuncia con su máscara real.
- Redes **multiacceso**: se eligen **DR** y **BDR** (mayor prioridad, luego mayor router ID); los demás son **DROTHER**.
- Multicast: 224.0.0.5 (todos los routers OSPF) y 224.0.0.6 (DR/BDR).
- Estados normales: FULL con DR/BDR, 2-WAY entre DROTHERs.
- Verificación: `show ip protocols`, `show ip ospf interface`, `show ip ospf neighbor`, `show ip route`.

## Conceptos, comandos y normas vistos

- [[OSPF]] · [[Mascara wildcard]] · [[IOS - OSPF]]
