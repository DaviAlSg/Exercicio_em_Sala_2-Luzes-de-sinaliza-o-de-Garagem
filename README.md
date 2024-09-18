# Exercicio_em_Sala_2 : Luzes de sinalização de Garagem
-
-
# Arduino feito no Tinkercard
-
![Editing Components (1)](https://github.com/user-attachments/assets/84e73e50-2e80-4ef0-bfe6-23a2306c3dea)
-
-
# Materiais
-
Arduino Uno
2 LED’s
2 Resistores de 220Ω para o LED
Fios de conexão
Protoboard
-
-
# Códigos
-
const int ledPin1 = 13;
const int ledPin2 = 9;

const int interval = 500;

void setup() {
Serial.begin(9600);

pinMode(ledPin1, OUTPUT);
pinMode(ledPin2, OUTPUT);

Serial.print("LED 1 está conectado ao pino ");
Serial.println(ledPin1);
Serial.print("LED 2 está conectado ao pino ");
Serial.println(ledPin2);
}

void loop() {
       digitalWrite(ledPin1, HIGH); 
       digitalWrite(ledPin2, LOW);
        Serial.println("LED 1 aceso, LED 2 apagado");
       delay(interval);
       digitalWrite(ledPin1, LOW);
       digitalWrite(ledPin2, HIGH);
       Serial.println("LED 1 apagado, LED 2 aceso");
       delay(interval);
  }
