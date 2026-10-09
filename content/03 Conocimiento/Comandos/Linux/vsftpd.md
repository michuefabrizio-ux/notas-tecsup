---
tipo: comando
categoria: Linux
cursos: ["[[Servicios de Red]]"]
aliases: []
tags: []
---

# vsftpd

```bash
dnf install -y vsftpd
systemctl enable --now vsftpd
firewall-cmd --permanent --add-service=ftp
firewall-cmd --permanent --add-port=10000-11000/tcp   # rango pasivo
firewall-cmd --reload
setsebool -P ftpd_use_passive_mode on
setsebool -P ftp_home_dir on
```

## Directivas en /etc/vsftpd/vsftpd.conf

| Directiva | Uso |
|---|---|
| `anonymous_enable=NO` | Desactiva anónimos |
| `local_enable=YES` | Usuarios locales |
| `write_enable=YES` | Permite subir |
| `chroot_local_user=YES` | Enjaula en el home |
| `chroot_list_enable` / `chroot_list_file` | Lista de excepciones |
| `pasv_min_port` / `pasv_max_port` | Rango pasivo |
| `local_umask=022` | Permisos de archivos creados |

## Raíz del chroot sin escritura

```bash
chmod a-w /home/proveedor1
mkdir /home/proveedor1/upload
semanage fcontext -a -t public_content_rw_t "/home/proveedor1/upload(/.*)?"
restorecon -Rv /home/proveedor1
```

Concepto: [[FTP activo y pasivo]]
