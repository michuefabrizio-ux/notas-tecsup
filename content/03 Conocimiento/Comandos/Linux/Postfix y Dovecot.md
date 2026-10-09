---
tipo: comando
categoria: Linux
cursos: ["[[Servicios de Red]]"]
aliases: [Postfix, Dovecot]
tags: []
---

# Postfix y Dovecot

```bash
dnf install -y postfix dovecot cyrus-sasl
systemctl enable --now postfix dovecot
firewall-cmd --permanent --add-service=smtp --add-service=imap && firewall-cmd --reload
```

## Revisar configuración

```bash
postconf -n                       # parámetros activos de Postfix
postconf -e "mydomain=dominio.lab"
postfix check
doveconf -n                       # o dovecot -n
newaliases                        # tras editar /etc/aliases
```

## Probar y monitorear

```bash
mail -s "Asunto" usuario
mailq
tail -f /var/log/maillog
setsebool -P postfix_local_write_mail_spool on
```

| Parámetro Postfix | Uso |
|---|---|
| `myhostname`, `mydomain` | Nombre del servidor y dominio |
| `mydestination` | Dominios que se entregan localmente |
| `mynetworks` | Redes que pueden enviar sin autenticarse |
| `home_mailbox = Maildir/` | Formato del buzón |

Concepto: [[Correo SMTP e IMAP]]
