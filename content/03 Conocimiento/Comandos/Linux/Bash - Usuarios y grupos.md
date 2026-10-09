---
tipo: comando
categoria: Linux
cursos: ["[[Sistemas Operativos de Codigo Abierto]]"]
aliases: [useradd, groupadd]
tags: []
---

# Bash — Usuarios y grupos

```bash
sudo adduser ana
sudo useradd -m -s /bin/bash -G ventas luis
sudo passwd luis
sudo groupadd ventas
sudo usermod -aG ventas ana
sudo gpasswd -d ana ventas
sudo userdel -r luis
id ana; groups ana
cat /etc/passwd; cat /etc/group
sudo usermod -s /sbin/nologin proveedor1   # sin shell interactivo
```

Lab: [[SOA Lab 04 - Usuarios y grupos]] · Relacionado: [[Bash - Permisos]]
