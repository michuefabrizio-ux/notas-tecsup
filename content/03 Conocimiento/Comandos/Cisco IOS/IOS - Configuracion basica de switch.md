---
tipo: comando
categoria: Cisco IOS
cursos: ["[[Protocolos de Enrutamiento]]", "[[Implementacion de Redes]]"]
aliases: []
tags: []
---

# IOS — Configuración básica de switch y router

```text
Switch> enable
Switch# configure terminal
Switch(config)# hostname S1
S1(config)# no ip domain-lookup
S1(config)# enable secret class
S1(config)# service password-encryption
S1(config)# banner motd #Acceso solo autorizado#
S1(config)# line console 0
S1(config-line)# password cisco
S1(config-line)# login
S1(config)# interface vlan 99
S1(config-if)# ip address 192.168.99.11 255.255.255.0
S1(config-if)# no shutdown
S1(config)# ip default-gateway 192.168.99.1
```

## SSH

```text
S1(config)# ip domain-name ejemplo.com
S1(config)# crypto key generate rsa general-keys modulus 1024
S1(config)# username admin secret Cisco123
S1(config)# line vty 0 15
S1(config-line)# transport input ssh
S1(config-line)# login local
S1(config)# ip ssh version 2
```

## Guardar

```text
S1# copy running-config startup-config
```

Concepto: [[VLAN de administracion y SVI]]
