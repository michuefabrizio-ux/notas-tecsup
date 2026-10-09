---
tipo: concepto
categoria: Matematica aplicada
cursos: ["[[Matematica para las Telecomunicaciones]]"]
aliases: [CODEC, RTP]
tags: []
---

# Ancho de banda de VoIP y CODEC

## Qué es

- El **CODEC** digitaliza y comprime la voz; el ancho de banda real de una llamada suma el *payload* del CODEC y las cabeceras de cada paquete.

## Cómo se calcula

- Paquetes por segundo = 1 / tamaño de muestra (ej.: 20 ms → 50 pps).
- Tamaño de paquete = payload + RTP (12 B) + UDP (8 B) + IP (20 B) + cabecera de capa 2.
- Ancho de banda = tamaño de paquete (bits) × pps.
- Audio digital: muestreo (Nyquist, fs ≥ 2·fmáx) y cuantificación; PCM telefónico = 8000 muestras/s × 8 bits = 64 kbps (G.711).

## Dónde lo usé

- [[MPT Lab 13 - Ancho de banda en redes]]

## Relacionado

- [[VoIP SIP y PBX]] · [[QoS]] · [[TCP vs UDP]]
