---
tipo: herramienta
categoria: Electronica
cursos: ["[[Electronica y Hardware de Computadoras]]"]
aliases: [Arduino]
tags: []
---

# Arduino Uno

## Qué es

- Placa con microcontrolador ATmega328P: 14 pines digitales (6 PWM), 6 entradas analógicas (ADC de 10 bits), 5 V.

## Estructura de un sketch

```cpp
void setup() {
  pinMode(13, OUTPUT);
  pinMode(2, INPUT);
  Serial.begin(9600);
}
void loop() {
  int boton = digitalRead(2);
  digitalWrite(13, boton);
  int luz = analogRead(A0);   // 0-1023
  analogWrite(9, luz / 4);    // PWM 0-255
  Serial.println(luz);
  delay(100);
}
```

## Para qué la usé

- [[EHC Lab 08 - Arduino displays y LCD]] · [[EHC Lab 09 - Arduino entradas y salidas digitales]] · [[EHC Lab 10 - Programacion Arduino]] · [[EHC Lab 11 - Sensor de inercia MPU-6050]] · [[EHC Lab 12 - Entradas y salidas analogicas]]

## Relacionado

- [[Tinkercad]] · [[ADC y DAC]]
