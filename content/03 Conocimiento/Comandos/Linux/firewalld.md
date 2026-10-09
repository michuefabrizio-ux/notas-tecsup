---
tipo: comando
categoria: Linux
cursos: ["[[Servicios de Red]]"]
aliases: [firewall-cmd]
tags: []
---

# firewalld

```bash
firewall-cmd --state
firewall-cmd --get-active-zones
firewall-cmd --list-all --zone=public
firewall-cmd --permanent --add-service=dns
firewall-cmd --permanent --add-port=10000-10100/tcp
firewall-cmd --permanent --zone=internal --change-interface=ens19
firewall-cmd --reload
firewall-cmd --runtime-to-permanent
```

## Reglas ricas y NAT

```bash
firewall-cmd --permanent --add-rich-rule='rule family="ipv4" source address="192.168.100.0/24" drop'
firewall-cmd --permanent --zone=external --add-masquerade
firewall-cmd --permanent --zone=external --add-forward-port=port=80:proto=tcp:toaddr=192.168.10.20
```

## Backend

```bash
grep FirewallBackend /etc/firewalld/firewalld.conf   # FirewallBackend=nftables
```

Concepto: [[Zonas de firewalld]]
