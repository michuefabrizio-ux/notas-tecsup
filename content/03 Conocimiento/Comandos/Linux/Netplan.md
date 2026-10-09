---
tipo: comando
categoria: Linux
cursos: ["[[Sistemas Operativos de Codigo Abierto]]"]
aliases: []
tags: []
---

# Netplan

Configuración de red en Ubuntu Server (`/etc/netplan/*.yaml`). La indentación YAML debe ser exacta (espacios, no tabulaciones).

```yaml
network:
  version: 2
  ethernets:
    ens33:
      dhcp4: false
      addresses: [10.160.10.10/24]
      routes:
        - to: default
          via: 10.160.10.2
      nameservers:
        addresses: [8.8.8.8]
```

```bash
sudo netplan try
sudo netplan apply
ip addr show ens33
```

Lab: [[SOA Lab 06 - Red y servicio DHCP]]
