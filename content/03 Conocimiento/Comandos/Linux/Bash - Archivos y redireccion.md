---
tipo: comando
categoria: Linux
cursos: ["[[Sistemas Operativos de Codigo Abierto]]"]
aliases: ["Redireccionamiento", "Tuberías"]
tags: []
---

# Bash — Archivos y redirección

## Archivos y directorios

```bash
pwd; ls -la; cd /etc
mkdir -p proyectos/2026
cp -r origen destino
mv viejo.txt nuevo.txt
rm archivo.txt            # usar con cuidado
find / -name "*.log" 2>/dev/null
grep -ri "error" /var/log/syslog
man ls; ls --help
w; who
```

## Redirección y tuberías

| Operador | Efecto |
|---|---|
| `>` | Sobrescribe stdout en un archivo |
| `>>` | Agrega al final |
| `2>` | Redirige stderr |
| `&>` | stdout y stderr juntos |
| `\|` | Pasa stdout al siguiente comando (no stderr) |

```bash
grep "Failed password" /var/log/auth.log | wc -l
cut -d' ' -f1 access.log | sort | uniq -c | sort -nr | head
comando >> registro.log 2>> errores.log
```

Lab: [[SOA Lab 07 - Redireccionamiento]] · [[SOA Lab 02 - Archivos y directorios]]
