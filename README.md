# aud5i022-2023-control

## pauta

- punto base
- asistencia
- materiales
- circuito
- código
- imágenes
- conclusiones

inspiracion: proyecto de estudiante del semestre pasado

* https://github.com/jibbx/AV-ERDDEL

// Adrian Vasquez, Camila Donoso y Victoria Claveria
// Semaforo de F1
// Creamos un sistema de luces que al presionar el boton se enciendan simulando un semaforo de cuenta regresiva de 5 tiempos con la inclusion de la perilla como regulador de intensidad de luz verde
// 28 de Abril de 2023

// Incluimos los valores de tiempo que se mantienen encendidas y apagadas las luces
int tiempoON = 1000;
int tiempoOFF = 100;
int tiempoONVERDE = 2000;

// Ingresamos los modos de los pines al codigo
void setup() {
  pinMode(7, INPUT);
  pinMode(6, OUTPUT);
  pinMode(5, OUTPUT);
  pinMode(4, OUTPUT);
  pinMode(3, OUTPUT);
  pinMode(2, OUTPUT);
}

void loop() {

//Si se lee 5V del pin 7 pasaran todas estas acciones
  if (digitalRead(7)) {
    digitalWrite(6, HIGH);
    delay(tiempoON);
    digitalWrite(6, LOW);
    delay(tiempoOFF);
    digitalWrite(5, HIGH);
    delay(tiempoON);
    digitalWrite(5, LOW);
    delay(tiempoOFF);
    digitalWrite(4, HIGH);
    delay(tiempoON);
    digitalWrite(4, LOW);
    delay(tiempoOFF);
    digitalWrite(3, HIGH);
    delay(tiempoON);
    digitalWrite(3, LOW);
    delay(tiempoOFF);
    digitalWrite(2, HIGH);
    delay(tiempoONVERDE);
    digitalWrite(2, LOW);
    delay(tiempoOFF);
  }
}
