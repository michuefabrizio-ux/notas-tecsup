---
tipo: comando
categoria: Linux
cursos: ["[[Sistemas Operativos de Codigo Abierto]]"]
aliases: [fdisk, mkfs, lsblk, LVM]
tags: []
---

# Bash — Discos y particiones

```bash
lsblk -f
sudo fdisk -l
sudo fdisk /dev/sdb          # o cfdisk
sudo mkfs.ext4 /dev/sdb1
sudo mkdir /datos && sudo mount /dev/sdb1 /datos
df -h; df -i                 # espacio e inodos
sudo blkid                   # UUID para /etc/fstab
dd if=/dev/zero of=prueba bs=1M count=1024 oflag=direct
```

## LVM

```bash
sudo pvcreate /dev/sdc
sudo vgcreate vg_datos /dev/sdc
sudo lvcreate -L 10G -n lv_web vg_datos
sudo lvextend -r -L +5G /dev/vg_datos/lv_web
```

Labs: [[SOA Lab 01 - Instalacion de GNU Linux]] · [[SOA Lab 09 - Unidades de almacenamiento]]
