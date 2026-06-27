# Capítulo 21: Sistemas Embebidos e IoT con IA

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

Los sistemas embebidos son la columna vertebral del mundo físico digitalizado. Microcontroladores dentro de lavadoras, sensores en tuberías de agua potable, actuadores en brazos robóticos de maquilas, módulos de telemetría en camiones de carga — todo esto es programación embebida. En 2026, la convergencia de IoT con Inteligencia Artificial crea una nueva disciplina: *TinyML* y *Edge AI*, donde modelos de aprendizaje automático corren directamente en microcontroladores de 256 KB de RAM. Este capítulo combina la profundidad técnica del hardware con las técnicas modernas de IA, con aplicaciones directamente relevantes para el contexto industrial de Tijuana y la región fronteriza.

## Fundamentos de Sistemas Embebidos

**1.** Programar un ESP32 o Raspberry Pi Pico W para leer la temperatura y humedad de un sensor DHT22 cada 30 segundos. Calcular el promedio móvil de las últimas 10 lecturas, detectar si la temperatura supera 35°C (condición de alerta), y encender un LED rojo usando PWM con intensidad proporcional a qué tan por encima del umbral está la temperatura. Sin sistema operativo — bare metal.

**2.** Implementar comunicación UART entre dos microcontroladores: el Transmisor lee un sensor analógico de CO2 (MQ-135) y envía paquetes con formato `[START][timestamp_32bit][valor_ppm_16bit][checksum_8bit][END]` a 115200 baudios. El Receptor verifica el checksum, descarta paquetes corruptos e imprime los valores válidos en un display OLED SSD1306.

**3.** Implementar un sistema de control PID para temperatura usando un microcontrolador: la planta es una resistencia calefactora controlada por PWM, el sensor es un termistor NTC 10K. Implementar el controlador PID en punto fijo (sin FPU) con coeficientes $K_p = 2.0$, $K_i = 0.5$, $K_d = 0.1$. El sistema debe alcanzar la temperatura de referencia en menos de 60 segundos con sobreimpulso menor al 10%.

**4.** Diseñar el firmware de un data logger para monitoreo ambiental de un laboratorio del TecNM: muestrear temperatura, humedad, CO2 y luz cada 5 minutos, almacenar en tarjeta SD en formato CSV con timestamp RTC, entrar en modo de bajo consumo (*deep sleep*) entre muestras. La batería LiPo de 2000 mAh debe durar al menos 30 días.

**5.** Implementar un stack de comunicación LoRa para una red de sensores de humedad de suelo en el Valle de Mexicali: nodos ESP32 + SX1276 envían lecturas cada 15 minutos al gateway, el gateway las reenvía al servidor por WiFi. Implementar: esquema de direccionamiento, confirmación de entrega, reintentos ante pérdida, y rotación de spreading factor para optimizar alcance vs. consumo.

## IoT y Conectividad

**6.** Construir un sistema de monitoreo de calidad de agua para la Comisión Estatal de Servicios Públicos de Tijuana: sensores de pH, turbidez, cloro residual y caudal conectados a un ESP32 publican cada minuto a un broker MQTT. Un servidor Node-RED procesa los datos, los almacena en InfluxDB y muestra un dashboard en Grafana con alertas cuando algún parámetro sale del rango establecido por la NOM-127-SSA1-2021.

**7.** Implementar un gateway LoRaWAN compatible con TTN (The Things Network) usando un Raspberry Pi + HAT Dragino: recibir paquetes de 10 nodos sensores de temperatura distribuidos en el campus del TecNM, decodificar el payload Cayenne LPP, y reenviar a la nube por MQTT. Medir el RSSI y SNR de cada nodo para construir un mapa de cobertura del campus.

**8.** Construir un sistema de control domótico para un aula inteligente del TecNM: sensores PIR detectan presencia, sensor de CO2 controla la ventilación, el sistema de iluminación se ajusta según la luz natural medida por un fotorresistor. Todo controlado por un ESP32 con interfaz web local (sin dependencia de internet). Si el CO2 supera 1200 ppm, la ventilación se activa automáticamente.

**9.** Implementar OTA (Over-The-Air) firmware update seguro para una flota de 50 sensores IoT distribuidos en una maquila de Tijuana: el servidor calcula el hash SHA-256 del nuevo firmware, los dispositivos descargan por HTTPS, verifican la integridad, instalan en partición de respaldo, arrancan desde ella y confirman éxito antes de activarla permanentemente. Si la actualización falla, el dispositivo revierte automáticamente.

## TinyML y Edge AI

**10.** Entrenar un modelo de detección de palabras clave (*keyword spotting*) para activar un asistente por voz: el modelo debe reconocer las palabras "encender", "apagar" y "temperatura" en audio capturado por un micrófono. Entrenar con TensorFlow Lite y cuantizar a INT8. El modelo final debe correr en un ESP32-S3 con menos de 80 KB de RAM y responder en menos de 500ms.

**11.** Implementar detección de anomalías en vibraciones de maquinaria industrial usando un acelerómetro MPU-6050: recopilar 10,000 medidas de operación normal, entrenar un autoencoder en TensorFlow Lite, cuantizarlo e implementarlo en un ESP32. El modelo debe detectar en tiempo real cuando la vibración indica desgaste o desbalance, con latencia menor a 100ms.

**12.** Construir un sistema de clasificación de gestos de mano usando un acelerómetro-giroscopio de 6 ejes y una red neuronal LSTM cuantizada: entrenar el modelo para reconocer 5 gestos (agitar, rotar, golpear, empujar, nada). El modelo final debe correr en un Arduino Nano 33 BLE Sense con 256 KB de RAM y clasificar cada gesto en menos de 50ms.

**13.** Implementar un sistema de visión artificial en el borde (*edge vision*) para control de calidad en línea de producción de la maquila: una cámara OV2640 conectada a un ESP32-S3 captura imágenes de piezas cada 2 segundos. Un modelo MobileNet cuantizado (< 1MB) clasifica la pieza como "buena", "defecto A" o "defecto B" en menos de 200ms. Las piezas defectuosas activan un actuador neumático para rechazarlas.

**14.** Construir un sistema de federated learning para una red de 10 sensores de calidad del aire en Tijuana: cada sensor entrena localmente su modelo con sus propias lecturas, envía solo los gradientes (no los datos crudos) al servidor central, el servidor agrega los gradientes con FedAvg y redistribuye el modelo actualizado. Demostrar que el modelo federado es más preciso que cualquier modelo individual y que los datos de cada nodo nunca salen del dispositivo.

## Optimización y Eficiencia Energética

**15.** Diseñar e implementar la gestión de energía para un nodo sensor solar: el sistema mide el nivel de la batería, la irradiación solar y la temperatura. Con batería al 100% envía datos cada 5 min, al 50% cada 15 min, al 20% solo envía alertas críticas. Cuando hay sol suficiente (> 300 W/m²) aumenta la frecuencia de muestreo para aprovechar la energía disponible. Modelar la duración estimada de la batería con cada estrategia.

**16.** Optimizar el uso de memoria RAM en un microcontrolador con 32 KB: dado un programa que procesa señales de audio con FFT de 512 puntos, implementarlo usando memoria estática (sin `malloc`), reordenar operaciones para maximizar la reutilización de buffers y medir el pico de uso de RAM. Usar técnicas de solapamiento de buffers para procesar ventanas de FFT con solo 2× el tamaño de la ventana en RAM.

---

## Problemas adicionales

**17.** Implementar un sistema de localización indoor para el campus del TecNM usando señales WiFi: un ESP32 móvil mide el RSSI de 5 puntos de acceso conocidos y usa trilateración para estimar su posición con error menor a 3 metros. Mejorar la precisión aplicando un filtro de Kalman que suaviza las estimaciones ruidosas de RSSI.

**18.** Construir un protótipo de medidor de energía eléctrica inteligente (AMI) para un hogar usando un sensor de corriente SCT-013 y un ESP32: medir el consumo instantáneo (Watts) y acumulado (kWh), calcular el costo aproximado en pesos según la tarifa doméstica DAC de la CFE, y publicar los datos cada minuto a un servidor MQTT. Detectar automáticamente si el consumo supera el límite de la tarifa básica.

**19.** Diseñar e implementar un sistema de alerta temprana para derrumbes en zonas de riesgo de Tijuana: acelerómetros de alta resolución instalados en laderas detectan vibraciones y movimiento incremental del suelo. Si el movimiento acumulado en 24 horas supera 2 mm, o si la aceleración instantánea supera 0.1g, el sistema envía una alerta por LoRa al servidor municipal y activa una sirena local con energía de respaldo.

**20.** Implementar un nodo sensor BLE Mesh para una red de sensores de temperatura en un almacén refrigerado: los nodos se auto-organizan en malla BLE 5.0, enrutan los datos del nodo más lejano al gateway usando múltiples saltos, y reconfigura automáticamente las rutas cuando un nodo se desconecta. El tiempo de reconvergencia tras un fallo debe ser menor a 30 segundos.
