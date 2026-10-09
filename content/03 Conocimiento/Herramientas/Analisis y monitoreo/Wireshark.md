---
tipo: herramienta
categoria: Analisis y monitoreo
cursos: ["[[Implementacion de Redes]]", "[[Ethical Hacking]]"]
aliases: []
tags: []
---

# Wireshark

## Qué es

- Analizador de protocolos gráfico: captura paquetes y muestra cada capa decodificada.

## Filtros útiles

| Filtro | Muestra |
|---|---|
| `ip.addr == 10.0.126.129` | Tráfico de/hacia una IP |
| `tcp.port == 21` | FTP control |
| `eth.addr == aa:bb:cc:dd:ee:ff` | Una MAC |
| `arp` / `icmp` / `dns` / `http` | Por protocolo |
| `tcp.flags.syn == 1` | Inicios de conexión |

## Para qué la usé

- Instalación (lab NetAcad 3.7.9) y análisis de tramas en [[IMR Lab 06 - Examinar tramas Ethernet]].
- Abrir capturas `.pcap` de [[EH Lab02 - Escaneo de redes]].

## Relacionado

- [[tcpdump]] · [[Trama Ethernet]]
