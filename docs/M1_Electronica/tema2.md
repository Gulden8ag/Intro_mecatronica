# MCU 101

**Materiales y software**

- **Tarjeta**: ESP32 DevKit V1 (WROOM-32). **Importante:** debe ser ESP32 “clásico”; las variantes S3/C3 **no tienen Bluetooth Classic** y los ejemplos de `BluetoothSerial` no compilan en ellas.
- **Cable**: USB de datos.
- **Breadboard**: + jumpers.
- **LED**: 1 + 1 resistor 220 Ω.
- **Botón**: 1 (push button).
- **Resistor**: (Opcional) 1 10 kΩ si no usamos pull-up interno.

**Software**:

- Arduino IDE + Paquete de tarjetas ESP32.
- (Opcional) VS Code + Extensión Arduino.

## Introducción a los Microcontroladores

Los microcontroladores (MCU) son pequeños ordenadores en un solo chip que contienen un procesador, memoria y periféricos de entrada/salida. 

Ejemplos comunes de microcontroladores incluyen:


- **Arduino Uno**: Basado en el microcontrolador ATmega328P.

![PINOUT Arduino Uno](../recursos/imgs/B1_UNO.png){ style="display:block; margin:auto;" width="80%"}

- **ESP32**: Un microcontrolador potente con conectividad Wi-Fi y Bluetooth.

![PINOUT ESP32](../recursos/imgs/esp32_devkitC_v4_pinlayout.png){ style="display:block; margin:auto;" width="80%"}

- **Raspberry Pi Pico**: Basado en el microcontrolador RP2040.

![PINOUT Raspberry Pi Pico](../recursos/imgs/pico-2-r4-pinout.svg){ style="display:block; margin:auto;" width="80%"}

- **STM32**: Una familia de microcontroladores basados en ARM Cortex-M.

![PINOUT STM32](../recursos/imgs/Bluepillpinout.webp){ style="display:block; margin:auto;" width="80%"}

## IDEs y Herramientas

Un IDE (Integrated Development Environment) es una “app todo-en-uno” para escribir, compilar y cargar programas al microcontrolador. Reúne:

- **Editor** de código (colores, autocompletado).
- **Compilador y toolchain** (traduce C/C++ a binario para ESP32).
- **Build system** (botón “Compilar/Subir”, manejo de dependencias).
- **Depuración** (mensajes en consola, a veces depurador paso a paso).
- **Monitor Serial** (ver/mandar texto por el puerto del ESP32).
- **Gestor** de placas y librerías (instalar soporte ESP32 y paquetes).

Opciones populares:

- **Arduino IDE**: Muy sencillo, ideal para principiantes. Soporta muchas placas.
- **VS Code + Extensión**: Más avanzado, con muchas funciones adicionales.
    - **PlatformIO**: Extensión para VS Code, potente y flexible, ideal para proyectos complejos.
    - **Extensión Arduino**: Permite usar VS Code como IDE de Arduino.
- **Espressif IDE**: IDE oficial de Espressif para ESP32, más complejo pero muy completo.

## Configuración del Entorno de Desarrollo

1. **Instalar Arduino IDE**:
    - Descargar desde [arduino.cc](https://www.arduino.cc/en/software).
    - Instalar siguiendo las instrucciones del sitio.
2. **Agregar soporte para ESP32**:
    - Abrir Arduino IDE.
    - dar clic en administrar placas (Herramientas > Placa > Gestor de tarjetas).
    - Buscar "esp32" e instalar el paquete de Espressif Systems.
    ![Instalar soporte ESP32](../recursos/imgs/esp32_install.png){ style="display:block; margin:auto;" width="100%"}

3. **Seleccionar la placa ESP32**:
    - Ir a Herramientas > Placa y seleccionar "DOIT ESP32 DEVKIT V1"
    - Configurar el puerto COM correcto (Herramientas > Puerto).


## Programación Básica en Arduino IDE

**Funciones principales de control de hardware**:

- `void setup(){}`: Se ejecuta una vez al inicio. Aquí se configuran pines, inicializa librerías, etc.
- `void loop(){}`: Se ejecuta repetidamente después de `setup()`. Aquí va el código principal.
- `pinMode(pin, mode)`: Configura un pin como entrada (`INPUT`) o salida (`OUTPUT`).
- `digitalWrite(pin, value)`: Escribe un valor alto (`HIGH`) o bajo (`LOW`) en un pin de salida.
- `digitalRead(pin)`: Lee el valor de un pin de entrada (retorna `HIGH` o `LOW`).
- `delay(ms)`: Pausa la ejecución por un número de milisegundos.
- `Serial.begin(baudrate)`: Inicia la comunicación serial a una velocidad dada (baudrate).
- `Serial.print(data)`: Envía datos al monitor serial.
- `Serial.println(data)`: Envía datos al monitor serial y añade un salto de línea

**Funciones Basicas de C/C++**:

- `int`, `float`, `char`, `bool`, `void`, `String`: Tipos de datos para variables basicos.
    - Ejemplos variables:
    ```cpp
    int numero = 10;          // Entero
    float decimal = 3.14;    // Número con decimales
    char letra = 'A';        // Carácter
    bool esVerdadero = true;  // Booleano (true/false)
    String texto = "Hola";    // Cadena de texto
    ```
- `==`, `!=`, `<`, `>`, `<=`, `>=`: Operadores de comparación.
- `+`, `-`, `*`, `/`, `%`: Operadores aritméticos
- `if`, `else`, `switch`: Estructuras de control de flujo.
    - Ejemplo `if`
    ```cpp
    if (condition) {
        // código a ejecutar si la condición es verdadera
    } else {
        // código a ejecutar si la condición es falsa
    }
    ```
    - Ejemplo `switch`
    ```cpp
    switch (variable) {
        case valor1:
            // código a ejecutar si variable == valor1
            break;
        case valor2:
            // código a ejecutar si variable == valor2
            break;
        default:
            // código a ejecutar si variable no coincide con ningún valor
    }
    ```
- `for`, `while`: Bucles de repetición.
    - Ejemplo `for`
    ```cpp
    for(int i=0; i<10; i++){
        Serial.println(i);
    }
    ```
    - Ejemplo `while`
    ```cpp 
    int i = 0;
    while(i < 10){
        Serial.println(i);
        i++;
    }
    ```

- `functionName()`: Llamada a funciones.
- `#define`: Definición de macros.
- `#include`: Inclusión de librerías.

## Estructura Básica de un Programa en Arduino

```cpp title="Estructura Básica"
void setup() {
    // Inicialización se ejecuta una vez
}

void loop() {
    // Código principal se ejecuta repetidamente
}
```

```cpp title="Blink"
//Revisar donde esta cableado el LED
#define LED 23

void setup() {
    pinMode(LED, OUTPUT); // Configura el pin del LED como salida
}

void loop() {
    digitalWrite(LED, HIGH); // Enciende el LED
    delay(1000); // Espera 1 segundo
    digitalWrite(LED, LOW); // Apaga el LED
    delay(1000); // Espera 1 segundo
}

```

![Esquema Blink](../recursos/imgs/blink_wiring.png){ style="display:block; margin:auto;" width="50%"}

**Blink con botón**

```cpp title="Blink con botón (pull-up interno)"

//Revisar donde esta cableado el botón y el LED
//Botón entre el pin y GND (con INPUT_PULLUP no necesita resistor externo)
#define LED 23
#define BUTTON 33

void setup() {
    pinMode(LED, OUTPUT);
    pinMode(BUTTON, INPUT_PULLUP); // pull-up interno: reposo = HIGH
}

void loop() {
    // Lógica invertida: presionado = LOW
    if (digitalRead(BUTTON) == LOW) {
        digitalWrite(LED, HIGH);
    } else {
        digitalWrite(LED, LOW);
    }
}
```

!!! info "¿Por qué lógica invertida?"
    Con `INPUT_PULLUP` el pin queda conectado internamente a 3.3 V a través de una resistencia,
    así que en reposo lee `HIGH`. Al presionar, el botón conecta el pin a GND y lee `LOW`.
    Ventaja: no necesitas el resistor externo de 10 kΩ.

**Antirrebote (debounce) por software**

Un botón mecánico "rebota": al presionarlo genera varios cambios HIGH/LOW en unos milisegundos.
Si cuentas presiones sin antirrebote, una sola presión puede contar 3 o 4 veces.

```cpp title="Toggle de LED con antirrebote (sin delay)"
#define LED 23
#define BUTTON 33

bool estadoLed = false;
int lecturaAnterior = HIGH;          // con pull-up, reposo = HIGH
unsigned long ultimoCambio = 0;
const unsigned long DEBOUNCE_MS = 30;

void setup() {
    pinMode(LED, OUTPUT);
    pinMode(BUTTON, INPUT_PULLUP);
}

void loop() {
    int lectura = digitalRead(BUTTON);

    // ¿Cambió la lectura y ya pasó el tiempo de antirrebote?
    if (lectura != lecturaAnterior && millis() - ultimoCambio > DEBOUNCE_MS) {
        ultimoCambio = millis();
        if (lectura == LOW) {              // flanco de presión
            estadoLed = !estadoLed;        // alterna el LED
            digitalWrite(LED, estadoLed);
        }
    }
    lecturaAnterior = lectura;
}
```

![Esquema Blink con botón](../recursos/imgs/button_blink_wiring.png){ style="display:block; margin:auto;" width="50%"}

**Imprimir en el Monitor Serial**

```cpp title="Monitor Serial"
void setup() {
    Serial.begin(115200);
}

void loop() {
    Serial.println("Hola, mundo!");
    delay(1000);
}
```
Para probar la comunicacion BT, es necesario emparejar el dispositivo con una app de terminal Bluetooth en el celular (por ejemplo, "Serial Bluetooth Terminal" en Android). Liga: [Serial Bluetooth Terminal](https://play.google.com/store/apps/details?id=de.kai_morich.serial_bluetooth_terminal&pcampaignid=web_share)

!!! note "Nota"
    El iphone no soporta la comunicacion serial por bluetooth, por lo que es necesario usar un dispositivo Android o una computadora con bluetooth.


**Comunicacion BT**

```cpp title="Bluetooth Serial"
#include "BluetoothSerial.h"
BluetoothSerial SerialBT;

void setup() {
    Serial.begin(115200);
    SerialBT.begin("ESP32");  // Nombre del dispositivo Bluetooth
    SerialBT.setTimeout(20);  // que readStringUntil no bloquee el loop
}

void loop() {
    if (SerialBT.available()) {
        // Lee hasta el salto de línea (manda tus comandos terminados en \n)
        String mensaje = SerialBT.readStringUntil('\n');
        mensaje.trim();  // quita espacios y \r
        Serial.println("Recibido: " + mensaje);
    }
    // Sin delay(): el loop debe girar rápido para responder al instante
}
```

!!! warning "Nunca pongas `delay()` en un loop que recibe comandos"
    Con `delay(1000)` el ESP32 atiende **un comando por segundo**: un carro controlado así
    tendría 1 s de retraso y sería inmanejable. Usa `readStringUntil('\n')` con `setTimeout`
    corto y deja el loop libre.

**Led con Bluetooth**

```cpp title="LED con Bluetooth"
#include "BluetoothSerial.h"
BluetoothSerial SerialBT;

#define LED 23

void setup() {
    Serial.begin(115200);
    SerialBT.begin("ESP32");
    SerialBT.setTimeout(20);
    pinMode(LED, OUTPUT);
}

void loop() {
    if (SerialBT.available()) {
        String mensaje = SerialBT.readStringUntil('\n');
        mensaje.trim();  // sin esto, "ON\r" != "ON" y la comparación falla
        Serial.println("Recibido: " + mensaje);
        if (mensaje == "ON") {
            digitalWrite(LED, HIGH);
        } else if (mensaje == "OFF") {
            digitalWrite(LED, LOW);
        }
    }
}
```

!!! tip "En la app de terminal Bluetooth"
    Configura la app para que agregue **Newline (\n)** al final de cada envío
    (en “Serial Bluetooth Terminal”: Settings → Send → Newline = LF).
