---
tipo: concepto
categoria: Fundamentos de redes
cursos: ["[[Implementacion de Redes]]"]
aliases: ["Ethernet II", "Dirección MAC"]
tags: []
---

# Trama Ethernet

## Campos (Ethernet II)

| Campo | Bytes |
|---|---|
| Preámbulo + SFD | 8 |
| MAC destino | 6 |
| MAC origen | 6 |
| Tipo / longitud (0x0800 IPv4, 0x86DD IPv6, 0x0806 ARP) | 2 |
| Datos | 46–1500 |
| FCS (CRC-32) | 4 |

- Tamaño de trama: 64 a 1518 bytes (sin preámbulo). Menor = *runt*; mayor = *giant*.
- MAC: 48 bits en hexadecimal; primeros 24 = **OUI** del fabricante. Broadcast `FF-FF-FF-FF-FF-FF`.

## Dónde lo usé

- [[IMR Lab 06 - Examinar tramas Ethernet]]

## Relacionado

- [[IEEE 802.3 Ethernet]] · [[Wireshark]] · [[CRC]]
