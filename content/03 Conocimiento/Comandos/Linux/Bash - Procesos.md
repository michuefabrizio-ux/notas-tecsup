---
tipo: comando
categoria: Linux
cursos: ["[[Sistemas Operativos de Codigo Abierto]]"]
aliases: [ps, top, kill]
tags: []
---

# Bash — Procesos

```bash
ps aux
ps -ef --forest          # árbol de procesos
pstree -p
top                      # o htop
sar -u 1 5               # CPU (paquete sysstat)
pgrep -a nginx
kill -15 1234            # SIGTERM: cierre ordenado
kill -9 1234             # SIGKILL: forzado, último recurso
nice -n 10 comando
renice 5 -p 1234
ls -l /proc/1234/exe     # binario real del proceso
```

Lab: [[SOA Lab 11 - Procesos y monitoreo]]
