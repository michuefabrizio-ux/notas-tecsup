---
tipo: concepto
categoria: Inalambricas y voz
cursos: ["[[Protocolos de Enrutamiento]]"]
aliases: [WLC, CAPWAP, "AP autónomo"]
tags: []
---

# WLAN y WLC

## Comparación

| Aspecto | AP autónomo | AP ligero + WLC |
|---|---|---|
| Configuración | En cada AP | Centralizada en el controlador |
| Protocolo | — | **CAPWAP** (túnel AP ↔ WLC) |
| Escala | Pocos AP | Empresas, campus |

- Arranque de un AP ligero: IP por DHCP → descubre el WLC → túnel CAPWAP → descarga el perfil (SSID, seguridad).
- Seguridad: WPA2/WPA3-Personal (PSK) o Enterprise (802.1X + RADIUS).

## Dónde lo usé

- [[PRE Lab 12 - AP autonomo y WLC]]

## Relacionado

- [[IEEE 802.11 Wi-Fi]] · [[Wi-Fi bandas y canales]]
