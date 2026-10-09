---
tipo: comando
categoria: Linux
cursos: ["[[Servicios de Red]]"]
aliases: [semanage, restorecon]
tags: []
---

# SELinux

```bash
getenforce
setenforce 1                         # enforcing (temporal)
sestatus
ls -Z /var/www/html
semanage fcontext -a -t httpd_sys_content_t "/srv/web(/.*)?"
restorecon -Rv /srv/web
getsebool -a | grep ftp
setsebool -P ftpd_use_passive_mode on
ausearch -m avc -ts recent
```

- El modo permanente se define en `/etc/selinux/config` (`SELINUX=enforcing`).

Concepto: [[SELinux modos y contextos]]
