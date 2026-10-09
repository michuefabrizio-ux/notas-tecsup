---
tipo: comando
categoria: Seguridad
cursos: ["[[Ethical Hacking]]"]
aliases: [nmap]
tags: []
---

# Nmap

## Descubrimiento de hosts

```bash
sudo nmap -sn 10.0.126.0/24
sudo arp-scan -l
sudo netdiscover -r 10.0.126.0/24
```

## Escaneo de puertos

```bash
sudo nmap -sS -p- 10.0.126.129 -oN puertos_129.txt
sudo nmap -sV -p 21,22,80 10.0.126.129 -oX servicios_129.xml
sudo nmap -Pn -sS -p- -A 10.0.126.0/24 -oX red_full.xml
sudo nmap -sU -p 137,138 10.0.126.129
sudo nmap --script smb-enum-shares,smb-os-discovery -p 139,445 10.0.126.129 -d
xsltproc red_full.xml -o red_full.html
```

| Opción | Uso |
|---|---|
| `-sS` / `-sT` / `-sU` | SYN / TCP Connect / UDP |
| `-p 80`, `-p-`, `-F`, `--top-ports N` | Puertos a escanear |
| `-sV` / `-O` / `-A` | Versiones / SO / todo + scripts |
| `-Pn` | Sin host discovery |
| `-n` | Sin resolución DNS |
| `-T0`…`-T5` | Velocidad (por defecto `-T3`) |
| `-oN` / `-oX` / `-oG` / `-oA` | Normal / XML / grepeable / los tres |

Concepto: [[Escaneo de puertos TCP]]
