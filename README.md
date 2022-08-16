# Flow-7-Medicion-De-Temperatura-ESP32CAM-DHT11-MQTT
Medición de temperatura y humedad mediante el microcontrolador ESP32 CAM con sensor DHT11 y transmisión de datos por MQTT en formato json

### Descripción
Este programa usa el ESP32 CAM y un sensor DHT11 para monitorear la temperatura y humedad relativa de un ambiente, esta información es transmitida mediante el protocolo MQTT a un servidor Node Red en localhost, en este servidor la información es desplegada en dos gauges y dos gráficas, una para la temperatura y otra para humedad relativa.
Posteriormente con la información de la temperatura se activará el led flash del microcontrolador simulando el encendido y apagado de un aire acondicionado. Este se activará al superar los 25°C.

# Requisitos
Para que el código de este repositorio funcione, es necesario contar con lo siguiente:

- ESP32CAM
- Programador FTDI con su cable
- Sensor DHT11
- Ubuntu 20.04
- IDE de Arduino 1.8 o superior
- Biblioteca PubSubClient para Arduino IDE
- Biblioteca WiFi para Arduino IDE
- Biblioiteca DHT de AdaFruit para Arduino IDE
- Broker Mosquitto funcionando de forma local en el puerto 1883
- NodeRed corriendo de forma local en el puerto 1880
- Nodos Dashboard para NodeRed

### Funcionamiento

Para observar el funcionamiento de este proyecto deberás realizar lo siguiente.

1. Carga el flow Node-Red-Graficaión-y-control.json en NodeRed.
2. Comprueba que el broker MQTT esté funcionando.
3. Carga el programa ESP32ACM-DHT11-MQTT.ino en el ESP32CAM.
4. Visita el dashboard de NodeRed

![](https://github.com/EduCabreraMendoza/Flow-7-Medicion-De-Temperatura-ESP32CAM-DHT11-MQTT/blob/main/esp32cam-dht11-mqtt.jpeg)

Creado el 16-ago-2022 por [Eduardo Cabrera](https://github.com/EduCabreraMendoza)