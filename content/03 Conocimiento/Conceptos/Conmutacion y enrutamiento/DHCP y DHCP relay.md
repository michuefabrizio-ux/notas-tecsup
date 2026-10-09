---
tipo: concepto
categoria: Conmutacion y enrutamiento
cursos: ["[[Redes Escalables]]", "[[Protocolos de Enrutamiento]]"]
aliases: [DHCP, DHCPv4, DORA, "ip helper-address"]
tags: []
---

# DHCP y DHCP relay

## Qué es

- **DHCPv4** asigna dinámicamente IP, máscara, gateway, DNS y dominio por un tiempo de **arrendamiento**.

## Cómo funciona

| Paso | Mensaje | Envía |
|---|---|---|
| 1 | DHCPDISCOVER | Cliente (broadcast) |
| 2 | DHCPOFFER | Servidor |
| 3 | DHCPREQUEST | Cliente |
| 4 | DHCPACK | Servidor |

- Renovación: REQUEST + ACK directo al servidor que dio la IP.
- **Relay**: los broadcast no cruzan routers; `ip helper-address <IP-servidor>` en la interfaz de la LAN reenvía las peticiones.

```text
ip dhcp excluded-address 192.168.10.1 192.168.10.10
ip dhcp pool LAN10
 network 192.168.10.0 255.255.255.0
 default-router 192.168.10.1
 dns-server 8.8.8.8
 domain-name ejemplo.com
 lease 7
!
interface g0/1
 ip helper-address 10.1.1.2
!
show ip dhcp binding
show ip dhcp pool
```

## Dónde lo usé

- [[RES S01 - DHCPv4]] · [[PRE Lab 07 - Configurar DHCPv4]]

## Relacionado

- [[Direccionamiento IPv4 y subredes]]
