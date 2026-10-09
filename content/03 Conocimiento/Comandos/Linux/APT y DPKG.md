---
tipo: comando
categoria: Linux
cursos: ["[[Sistemas Operativos de Codigo Abierto]]"]
aliases: [apt, dpkg]
tags: []
---

# APT y DPKG

```bash
sudo apt update && sudo apt upgrade
sudo apt install nmap
apt search speedtest
apt show nmap
sudo apt remove paquete
sudo apt purge paquete && sudo apt autoremove
sudo dpkg -i paquete.deb
dpkg -l | grep nmap
sudo apt -f install          # arreglar dependencias
```

## Compilar desde código fuente

```bash
sudo apt install build-essential
tar xzf redis-*.tar.gz && cd redis-*
make && sudo make install
redis-server --version
```

Lab: [[SOA Lab 05 - Instalacion de programas con APT y DPKG]]
