# Motor DC

Já vimos o servo motor que gira para um ângulo específico de forma limitada… mas qual tipo de motor utilizamos para girar rodas e demais movimentos contínuos?

O motor DC (corrente contínua) é um motor que simplesmente RODA enquanto estiver ligado à energia!

Explicar que o motor tem apenas dois polos, e basta colocar uma tensão para ele rodar.

Se inverter os polos, ele gira para o outro sentido.

Se aumentar a tensão, ele gira mais rápido.

E é possível controlar a velocidade e direção dele!

Apresenta por cima a L298N.

Desafio:

A apresentação / aula deve preparar os alunos para resolverem o desafio no tinkerCAD:

(copiar e colar circuito no link: https://www.tinkercad.com/things/5Rww2qQjAgA-motor-dc-curso-maker?sharecode=oKP6hmRpfvv5HTerYt6WYe1Qb916us0uaEkRYpKv0hI)

Código que já está pronto no link:

```ino
// Pino ENABLE dita a velocidade do motor (de 0 a 255)
#define ENABLE 10

// Pinos IN1 e IN2 ditam a direção de rotação do motor (ver tabela)
#define IN1 7
#define IN2 6

void setup() {
 // configura os pinos como saída
 pinMode(ENABLE, OUTPUT);
 pinMode(IN1, OUTPUT);
 pinMode(IN2, OUTPUT);
}

void loop() {
  
 // Roda com 100% de velocidade
 // Para FRENTE
 analogWrite(ENABLE, 255);
 digitalWrite(IN1, HIGH);
 digitalWrite(IN2, LOW);
 delay(5000);
  
  
 // Roda com 70% de velocidade
 // Para FRENTE
 analogWrite(ENABLE, 0.70*255);
 digitalWrite(IN1, HIGH);
 digitalWrite(IN2, LOW);
 delay(5000);
  
  
 // Roda com 100% de velocidade
 // Para TRÁS
 analogWrite(ENABLE, 255);
 digitalWrite(IN1, LOW);
 digitalWrite(IN2, HIGH);
 delay(5000);
  

 // Roda com 40% de velocidade
 // Para TRÁS
 analogWrite(ENABLE, 0.40*255);
 digitalWrite(IN1, LOW);
 digitalWrite(IN2, HIGH);
 delay(5000);
  
  
  // DESAFIO
 // Roda com 50% de velocidade
 // Para FRENTE
 // -- * inserir código aqui * --

}
```
