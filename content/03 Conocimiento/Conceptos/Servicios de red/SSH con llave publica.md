---
tipo: concepto
categoria: Servicios de red
cursos: ["[[Servicios de Red]]"]
aliases: [SSH, OpenSSH]
tags: []
---

# SSH con llave pública

## Qué es

- **SSH** (TCP 22) es acceso remoto cifrado; reemplaza a **Telnet** (TCP 23), que envía todo en texto plano.

## Cómo funciona

1. **Negociación**: se acuerdan algoritmos simétricos (AES, ChaCha20) e intercambio de claves (Diffie-Hellman, ECDH).
2. **Autenticación**: el servidor prueba su identidad con su clave de host; el usuario se autentica con llave o contraseña cifrada.
3. **Sesión**: todo se cifra con una clave simétrica.

- Con llaves: la **pública** va en `~/.ssh/authorized_keys` del servidor; la **privada** nunca sale del cliente. El servidor envía un reto que solo la privada puede resolver.

```bash
ssh-keygen -t ed25519
ssh-copy-id usuario@servidor
ssh usuario@servidor
```

## Comparación

| Algoritmo | Seguridad | Nota |
|---|---|---|
| Ed25519 | Muy alta | No compatible con FIPS 140 |
| ECDSA | Alta | Compatible con FIPS |
| RSA ≥ 3072 | Media | Sistemas antiguos |

- RHEL 10: `PermitRootLogin prohibit-password` por defecto.

## Dónde lo usé

- [[SRD S08 - Acceso remoto SSH y NFS]]

## Relacionado

- [[NFSv4]] · [[PuTTY]] · [[Bastionado]]
