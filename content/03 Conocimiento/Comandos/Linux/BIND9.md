---
tipo: comando
categoria: Linux
cursos: ["[[Servicios de Red]]"]
aliases: [named, bind]
tags: []
---

# BIND9

Servidor DNS. En RHEL el servicio se llama `named`; en Ubuntu, `bind9`/`named`.

## Instalación y servicio

```bash
dnf install -y bind bind-utils          # RHEL
systemctl enable --now named
firewall-cmd --permanent --add-service=dns && firewall-cmd --reload
```

## Archivos

| Ruta (RHEL) | Uso |
|---|---|
| `/etc/named.conf` | Configuración principal (`options`, `zone`) |
| `/var/named/` | Archivos de zona |

## Validar y recargar

```bash
named-checkconf /etc/named.conf
named-checkzone dominio.lab /var/named/dominio.lab.zone
rndc reload
chown root:named /var/named/*.zone && chmod 640 /var/named/*.zone
restorecon -Rv /var/named/
```

## Probar

```bash
dig @127.0.0.1 www.dominio.lab A
dig @127.0.0.1 dominio.lab MX
dig -x 172.16.50.10        # inversa
host www.dominio.lab
journalctl -u named -xe
```

| Problema | Solución |
|---|---|
| `status: REFUSED` | Revisar `allow-query` / `allow-recursion` |
| named no lee la zona | `chown root:named`, `chmod 640`, `restorecon` |

Concepto: [[DNS zona directa e inversa]]
