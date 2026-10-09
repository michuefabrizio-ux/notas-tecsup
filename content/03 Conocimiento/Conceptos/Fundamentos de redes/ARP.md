---
tipo: concepto
categoria: Fundamentos de redes
cursos: ["[[Implementacion de Redes]]", "[[Ethical Hacking]]"]
aliases: ["Tabla ARP"]
tags: []
---

# ARP

## Qué es

- Protocolo que obtiene la **MAC** correspondiente a una **IPv4** dentro de la misma red.

## Cómo funciona

1. El host busca la IP en su **tabla ARP**.
2. Si no está, envía un **ARP request** en broadcast ("¿quién tiene 192.168.1.1?").
3. El dueño responde con un **ARP reply** unicast.
4. Se guarda en la tabla ARP por un tiempo.

- Para destinos remotos se resuelve la MAC del **gateway**.
- ARP no tiene autenticación → **ARP spoofing**.

```text
arp -a            (Windows)
ip neigh          (Linux)
show arp          (Cisco)
```

## Relacionado

- [[Sniffing y ARP spoofing]] · [[Trama Ethernet]]
