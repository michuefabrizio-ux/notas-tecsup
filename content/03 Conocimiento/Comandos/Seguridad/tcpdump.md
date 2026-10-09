---
tipo: comando
categoria: Seguridad
cursos: ["[[Ethical Hacking]]"]
aliases: []
tags: []
---

# tcpdump

```bash
sudo tcpdump -D                              # interfaces
sudo tcpdump -i eth0 -n host 10.0.126.129
sudo tcpdump -i eth0 -n port 21 -w cap_puerto21.pcap
sudo tcpdump -r cap_puerto21.pcap -n
sudo tcpdump -i eth0 'tcp[tcpflags] & tcp-syn != 0'
```

| Opción | Uso |
|---|---|
| `-i` | Interfaz |
| `-n` | No resolver nombres |
| `-w` / `-r` | Guardar / leer `.pcap` |
| `-c N` | Capturar N paquetes |
| `-A` / `-X` | Mostrar contenido en ASCII / hex+ASCII |
| `-v`, `-vv` | Más detalle |

Filtros: `host`, `src`/`dst`, `net 10.0.0.0/24`, `port`, `tcp`, `udp`, `icmp`.

Concepto: [[Sniffing y ARP spoofing]] · Herramienta gráfica: [[Wireshark]]
