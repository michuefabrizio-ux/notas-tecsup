---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Redes Escalables]]"]
aliases: [ACL, "ACL estándar", "ACL extendida"]
tags: []
---

# ACL estándar y extendida

## Qué es

- Listas de reglas `permit`/`deny` que un router evalúa **en orden** sobre cada paquete; al final hay un **deny implícito**.

## Comparación

| Aspecto | Estándar | Extendida |
|---|---|---|
| Números | 1–99, 1300–1999 | 100–199, 2000–2699 |
| Filtra por | IP de origen | Origen, destino, protocolo y puertos |
| Ubicación | Cerca del **destino** | Cerca del **origen** |

- Se aplican a una interfaz y un sentido: `ip access-group <ACL> in|out`.
- Una ACL por interfaz, por protocolo y por sentido.
- Pueden ser **numeradas** o **nombradas** (las nombradas permiten editar por número de secuencia).

## Dónde lo usé

- [[RES GLAB-S04 - ACL estandar]] · [[RES GLAB-S05 - ACL extendidas]] · Eje [[OE2 - VLAN ACL y DMZ]]

## Relacionado

- [[IOS - ACL]] · [[Mascara wildcard]] · [[Proxy y ACL de Squid]]
