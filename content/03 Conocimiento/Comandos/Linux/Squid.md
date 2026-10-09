---
tipo: comando
categoria: Linux
cursos: ["[[Servicios de Red]]"]
aliases: []
tags: []
---

# Squid

```bash
dnf install -y squid httpd-tools
systemctl enable --now squid
squid -k parse            # validar
squid -z                  # crear caché
squid -k reconfigure      # recargar
firewall-cmd --permanent --add-port=3128/tcp && firewall-cmd --reload
setsebool -P squid_connect_any on
tail -f /var/log/squid/access.log
grep "TCP_DENIED" /var/log/squid/access.log
```

## Ejemplo de /etc/squid/squid.conf

```text
acl red_local src 192.168.10.0/24
acl bloqueados dstdomain .facebook.com .youtube.com
acl descargas url_regex -i \.exe$ \.zip$ \.mp3$
acl laboral time MTWHF 08:00-18:00
http_access deny bloqueados laboral
http_access deny descargas
http_access allow red_local
http_access deny all
```

## Autenticación básica

```bash
htpasswd -c /etc/squid/passwords usuario1
chmod 640 /etc/squid/passwords && chown squid:squid /etc/squid/passwords
```

Concepto: [[Proxy y ACL de Squid]]
