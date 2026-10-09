---
tipo: comando
categoria: Linux
cursos: ["[[Sistemas Operativos de Codigo Abierto]]", "[[Servicios de Red]]"]
aliases: [systemctl, journalctl]
tags: []
---

# Bash — Servicios y logs

```bash
systemctl status named
systemctl start|stop|restart|reload httpd
systemctl enable --now vsftpd
systemctl is-enabled squid
journalctl -u named -xe
journalctl -f
tail -f /var/log/maillog
```

Relacionado: [[Bash - Red y diagnostico]]
