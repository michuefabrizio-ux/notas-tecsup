---
tipo: concepto
categoria: Cableado y fibra optica
cursos: ["[[Cableado Estructurado y Fibra Optica]]"]
aliases: ["Presupuesto de potencia", "Power budget"]
tags: []
---

# Presupuesto de pérdidas ópticas

## Qué es

- Cálculo que verifica si la luz llega al receptor con potencia suficiente después de todas las pérdidas del enlace.

## Fórmulas del docente

- Número de empalmes: `N = L / Lb + 1`
- Atenuación del span: `Aspan = L·α + N·ae + Nc·ac + al + acr + apmd + adl`

| Símbolo | Significado |
|---|---|
| L, α | Longitud (km) y atenuación de la fibra (dB/km) |
| N, ae | Nº de empalmes y pérdida por empalme |
| Nc, ac | Nº de conectores y pérdida por conector |
| al, acr, apmd | No linealidades, dispersión cromática, PMD |
| adl | Dispositivos en línea (splitter, atenuador) |

- Presupuesto: `PB = PTx,min − S0 ≥ 0` (S0 = sensibilidad del receptor).
- Margen: `PM = PB − Aspan` → **1–3 dB** en LAN; **> 3 hasta 10 dB** en WAN.
- Potencia recibida: `PIN = PTx,max − Aspan`, con `S0 ≤ PIN ≤ PR,max`.

## Ejemplo

- 15 km con bobinas de 5 km → N = 15/5 + 1 = **4 empalmes**.

## Dónde lo usé

- [[CAB S08 - Presupuesto de perdidas opticas]] · [[CAB Lab 08 - Certificacion de fibra optica]]

## Relacionado

- [[Fibra monomodo]] · [[Perdidas en empalmes]] · [[Fuente y medidor de potencia optica]]
