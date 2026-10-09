---
tipo: comando
categoria: Linux
cursos: ["[[Sistemas Operativos de Codigo Abierto]]", "[[Servicios de Red]]"]
aliases: []
tags: []
---

# Bash — Red y diagnóstico

```bash
ip addr show
ip route
ping -c 4 8.8.8.8
traceroute www.tecsup.edu.pe
ss -tulpn                  # puertos en escucha y proceso
netstat -tuln
nmcli con show
nmcli con mod ens160 ipv4.addresses 172.16.50.10/24 ipv4.gateway 172.16.50.1 ipv4.method manual
hostnamectl set-hostname ns1.corp.redes.lab
dig www.dominio.lab
curl -I http://www.dominio.lab
```

Relacionado: [[Netplan]] · [[BIND9]]
