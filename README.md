# EV-Prototipado

Revitank IoT – Monitoreo de Nivel de Agua con ESP8266

![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino_IDE-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![ESP8266](https://img.shields.io/badge/ESP8266-000000?style=for-the-badge&logo=espressif&logoColor=white)
![Blynk](https://img.shields.io/badge/Blynk_IoT-27AE60?style=for-the-badge&logo=blynk&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-000000?style=for-the-badge&logo=github&logoColor=white)

Revitank IoT es un sistema de monitoreo de niveles de agua diseñado con
ESP8266, un sensor ultrasónico HC-SR04 y un sensor de agua digital. El
dispositivo envía datos en tiempo real a Blynk IoT, permitiendo
visualizar nivel del tanque, porcentaje de llenado y alertas desde
cualquier dispositivo.

🚀 Características Principales

-   Monitoreo de nivel de agua en tiempo real mediante sensor
    ultrasónico.
-   Cálculo automático de porcentaje de llenado según dimensiones del
    recipiente.
-   Sensor de agua digital 0/1 para detectar humedad o filtraciones.
-   Dashboard en Blynk IoT con widgets personalizables.
-   Actualización de datos cada segundo sin bloquear el
    microcontrolador.
-   Código modular y fácil de expandir.

🛠️ Hardware Utilizado

-   ESP8266 (NodeMCU / Wemos D1 mini)
-   HC-SR04 – Sensor ultrasónico
-   Sensor de agua (– + S)
-   LED indicador (opcional)
-   Resistencias 1kΩ y 2kΩ
-   Protoboard y cables dupont

📡 Arquitectura del Sistema

  Componente                  Función                  Blynk Pin
  --------------------------- ------------------------ -----------
  Sensor de agua (0/1)        Detecta humedad          V1
  HC-SR04 – distancia cruda   Distancia al agua        V2
  Nivel invertido en cm       Distancia transformada   V3
  Porcentaje de nivel         % de llenado             V4

🔌 Conexiones Principales

Sensor de Agua (– + S) - – → GND - + → D1 - S → A0

HC-SR04 - VCC → VIN (5V) - GND → GND - TRIG → D6 - ECHO → D7 (con
divisor de voltaje)

LED indicador - D2 → Resistencia → LED → GND

📥 Instalación

1.  Instalar dependencias en Arduino IDE.

2.  Configurar Datastreams en Blynk:

    -   V1 = Sensor agua
    -   V2 = Distancia
    -   V3 = Nivel cm
    -   V4 = Porcentaje

▶️ Ejecución

1.  Abrir código en Arduino IDE.
2.  Configurar WiFi
3.  Seleccionar placa NodeMCU 1.0.
4.  Subir código.
5.  Visualizar datos en Blynk IoT.

👤 Realizado por

Grupo 8

📄 Licencia

MIT License
