---
tipo: comando
categoria: Linux
cursos: ["[[Sistemas Operativos de Codigo Abierto]]", "[[Servicios de Red]]"]
aliases: [chmod, chown]
tags: []
---

# Bash — Permisos

```bash
ls -l archivo
chmod 640 archivo            # rw- r-- ---
chmod u+x script.sh
chmod a-w /home/proveedor1   # quitar escritura a todos
chown root:named zona.db
chgrp ventas carpeta
chmod +t /compartido         # sticky bit
chmod g+s /compartido        # SGID: hereda el grupo
umask 022
```

| Octal | Permisos |
|---|---|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |

- **Sticky bit**: en una carpeta compartida, solo el dueño puede borrar sus archivos.

Lab: [[SOA Lab 04 - Usuarios y grupos]]
