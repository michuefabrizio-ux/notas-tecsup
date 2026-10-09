---
tipo: clase
curso: "[[Cableado Estructurado y Fibra Optica]]"
ciclo: 4
periodo: 2026-2
semana: 8
fecha:
estado: entregado
calificacion:
aliases: ["CAB S08 - Presupuesto de pérdidas ópticas"]
tags: [curso/cableado]
---

# CAB S08 — Presupuesto de pérdidas ópticas

← MOC del curso: [[Cableado Estructurado y Fibra Optica]] · Fuente: `Material/PPT-S08-JVELARDE-2026-02.pdf`

## Tema de la sesión

- Atenuación de un enlace, presupuesto y margen de potencia, instrumentos OLTS y OTDR.

## Lo esencial

- Número de empalmes: `N = L / Lb + 1` (15 km con bobinas de 5 km → 4 empalmes).
- Atenuación del span: `Aspan = L·α + N·ae + Nc·ac + (no linealidades, dispersión, dispositivos en línea)`.
- Presupuesto: `PB = PTx,min − S0 ≥ 0`; margen: `PM = PB − Aspan` (1–3 dB en LAN; > 3 hasta 10 dB en WAN).
- Potencia recibida: `PIN = PTx,max − Aspan`, que debe quedar dentro del rango dinámico del receptor.
- Fibras UIT-T: G.652 (la más comercial), G.653, G.654, G.655, G.656, **G.657** (acceso FTTx), G.651.1 (multimodo 50 µm).
- GPON: hasta 20 km, splitters 1:4 a 1:64.
- Instrumentos: **OLTS** (fuente + medidor de potencia), certificador de fibra y **OTDR**.

## Conceptos, comandos y normas vistos

- [[Presupuesto de perdidas opticas]] · [[Fibra monomodo]] · [[Fuente y medidor de potencia optica]] · [[OTDR]]
