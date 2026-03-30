# TALLER_ARDUINO

1. ¿Qué son las compuertas lógicas?


Las compuertas lógicas son circuitos electrónicos que toman señales de entrada (0 o 1) y producen una salida según una operación lógica. En Arduino simulamos esto con pulsadores como entradas y LEDs como salidas.


https://github.com/MiguelMejia77H/TALLER_ARDUINO/blob/main/COMPUERTAS%20LOGICAS.mp4


Materiales utilizados
1. Arduino UNO1
2. Pulsadores
3. LED verde
4. LED amarillo
5. lED rojo
6. Resistencias 220Ω


Codigo

int A = 2;
int B = 3;

int ledAND = 8;
int ledOR = 9;
int ledNOT = 10;

void setup() {
 pinMode(A, INPUT);
 pinMode(B, INPUT);
  
 pinMode(ledAND, OUTPUT);
 pinMode(ledOR, OUTPUT);
 pinMode(ledNOT, OUTPUT);
}

void loop() {
 int estadoA = digitalRead(A);
 int estadoB = digitalRead(B);
  
 // AND
 digitalWrite(ledAND, estadoA && estadoB);
  
 // OR
 digitalWrite(ledOR, estadoA || estadoB);
  
 // NOT (solo A)
 digitalWrite(ledNOT, !estadoA);
}
  


