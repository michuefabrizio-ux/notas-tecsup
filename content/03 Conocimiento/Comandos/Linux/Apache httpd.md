---
tipo: comando
categoria: Linux
cursos: ["[[Servicios de Red]]"]
aliases: [apache2, httpd]
tags: []
---

# Apache httpd

En RHEL: paquete y servicio `httpd`. En Ubuntu: `apache2`.

```bash
dnf install -y httpd
systemctl enable --now httpd
apachectl configtest          # Ubuntu: apache2ctl configtest
firewall-cmd --permanent --add-service=http --add-service=https && firewall-cmd --reload
```

## Contenido fuera de /var/www/html (SELinux)

```bash
semanage fcontext -a -t httpd_sys_content_t "/srv/web(/.*)?"
restorecon -Rv /srv/web
ausearch -m avc -ts recent       # ver denegaciones
```

## LAMP

```bash
dnf install -y httpd mariadb-server php
systemctl enable --now mariadb php-fpm
mariadb-secure-installation
```

| Ruta (RHEL) | Uso |
|---|---|
| `/etc/httpd/conf/httpd.conf` | Principal |
| `/etc/httpd/conf.d/` | VirtualHosts y extras |
| `/var/log/httpd/` | Logs |

Conceptos: [[Servidor web y VirtualHost]] · [[LAMP]]
