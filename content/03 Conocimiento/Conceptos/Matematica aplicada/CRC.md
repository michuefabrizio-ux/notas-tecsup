---
tipo: concepto
categoria: Matematica aplicada
cursos: ["[[Matematica para las Telecomunicaciones]]"]
aliases: ["Código de redundancia cíclica", FCS]
tags: []
---

# CRC (código de redundancia cíclica)

## Cómo funciona

1. La información I(x) se escribe como polinomio (101101 → x⁵ + x³ + x² + 1).
2. Se multiplica por xʳ (agregar r ceros), siendo r el grado del polinomio generador G(x).
3. Se divide en módulo 2 entre G(x) y se obtiene el residuo R(x).
4. Se transmite `C(x) = I(x)·xʳ + R(x)`.
5. El receptor divide entre G(x): residuo 0 → sin error detectado.

- Muy eficaz con **ráfagas** de errores; fácil de implementar con registros de desplazamiento.
- CRC-CCITT (HDLC): G(x) = x¹⁶ + x¹² + x⁵ + 1. Ethernet usa CRC-32 en el FCS.

## Dónde lo usé

- [[MPT S09 - CRC y codigos convolucionales]] · [[MPT Lab 10 - Protocolo HDLC]]

## Relacionado

- [[Codigos de deteccion y correccion de errores]] · [[Protocolo HDLC]] · [[Trama Ethernet]]
