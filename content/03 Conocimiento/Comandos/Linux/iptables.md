---
tipo: comando
categoria: Linux
cursos: ["[[Servicios de Red]]"]
aliases: []
tags: []
---

# iptables

```bash
iptables -L -n -v --line-numbers
iptables -P INPUT DROP
iptables -A INPUT -i lo -j ACCEPT
iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT
iptables -A INPUT -s 192.168.1.10 -p tcp --dport 22 -j ACCEPT
iptables -A INPUT -s 192.168.1.11 -p icmp -j REJECT
iptables -D INPUT 3          # borrar regla 3
iptables -F                  # vaciar reglas
iptables-save > /etc/iptables/rules.v4
```

| Opción | Significado |
|---|---|
| `-A` / `-I` | Agregar al final / insertar arriba |
| `-P` | Política por defecto |
| `-s` / `-d` | IP origen / destino |
| `-p` / `--dport` | Protocolo / puerto destino |
| `-j` | Acción: ACCEPT, DROP, REJECT |

Conceptos: [[Cadenas de iptables]] · [[Politicas DROP vs REJECT]]
