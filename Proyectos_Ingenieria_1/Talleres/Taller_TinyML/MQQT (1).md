# SenseCraft AI y comunicación MQTT

# Estudiantes:

# Deza Mamani Erick Armando

# Sanchez Ticllasuca Brenda Estefany

Objetivo de clase : Desarrollar un modelo de inteligencia artificial capaz de reconocer lapiceros mediante clasificación de imágenes y enviar los resultados usando el protocolo MQTT.

# Metodología:

Se definieron tres categorías de clasificación correspondientes a distintos tipos de lapiceros negro, azul y rojo, con el propósito de entrenar un modelo de reconocimiento de imágenes.

![](images/0f36f9179d74998f01df7d8d3abef47b7c03b35eea6a682c9c4cdb03b06c3c9f.jpg)

<details>
<summary>text_image</summary>

Paso 1: Hecoleccion de datos de clasincacion
Lapicero Rojo ?
238 Image Samples
Lapicero Negro ?
228 Image Samples
XIAO ESP32S3 Sense
Desconectar
Mantener para grabar
Detener
Importar Conjunto de Datos
Exportar Conjunto de Datos
Limpiar
Vista previa de resultados
99% Lapicero Azul
0%
Lapicero Rojo
Lapicero Ne...
Paso 2: Entrenar
XIAO ESP32S3 Sense
Iniciar entrenamiento
</details>

Para cada categoría se capturaron 200-250 imágenes desde diferentes ángulos, distancias y condiciones de iluminación, con el fin de mejorar la capacidad de aprendizaje y reconocimiento del modelo.

![](images/ae7dd1ca11e9e5ecaf67defd9e866566b5659af093db310f7917f1634ed48a07.jpg)

<details>
<summary>text_image</summary>

SenseCraft | SenseCraft AI
Inicio Aplicaciones Modelos Comunidad
Epic Armando De
Paso 1: Hecoieccion de datos de clasmcacion
Lapicero Rojo ...
238 Image Samples
Lapicero Negro ...
228 Image Samples
Importar Conjunto de Datos Exportar Conjunto de Datos Limpiar
Paso 2: Entrenar
XIAO ESP32S3 Sense Iniciar entrenamiento
Webcam
Mantener para grabar
Vista previa de resultados
2%
Lapicero Azu
0%
Lapicero Roja
78%
Lapicero Ne...
Configuración avanzada
</details>

Las imágenes obtenidas fueron cargadas en la plataforma SenseCraft AI, organizándose según su respectiva clase de clasificación. Posteriormente, se realizó el proceso de entrenamiento del modelo de inteligencia artificial utilizando el dispositivo XIAO ESP32S3 Sense como plataforma de despliegue.

Una vez finalizado el entrenamiento, el modelo fue implementado en el dispositivo para realizar pruebas de reconocimiento en tiempo real mediante la cámara integrada. en tiempo real. Se configuró la conexión de red del dispositivo XIAO ESP32S3 Sense mediante una red WiFi con acceso a internet.

![](images/11271c7fd8655bc73cb121d0c0dd9f420ef63b53ac6c18c5da4b72aab3f92d8e.jpg)

<details>
<summary>text_image</summary>

SenseCraft | SenseCraft AI
MQTT
GPIO
Puerto Serie
Audio
Vibration
Vista previa
Detener
encender ①:
UART[USB]
WIFI & MQTT
Configuración
Dirección IP:
Estado del servicio:    MQTT no inicializado o no conectado
Registro del dispositivo
perf: {"preprocess":110,"inference":426,"postprocess":0}
perf: {"preprocess":110,"inference":426,"postprocess":0}
perf: {"preprocess":111,"inference":426,"postprocess":0}
perf: {"preprocess":109,"inference":426,"postprocess":0}
perf: {"preprocess":111,"inference":426,"postprocess":0}
perf: {"preprocess":110,"inference":426,"postprocess":0}
perf: {"preprocess":107,"inference":426,"postprocess":0}
</details>

# Configuración MQTT:

Posteriormente, se establecieron los parámetros de conexión MQTT, definiendo como host el servidor rp10.rcr-labs.com, utilizando el puerto 1883, el usuario Alumno y la contraseña Cayetano 2026, correspondientes a la configuración del protocolo MQTT estándar.

![](images/b78d912739db123feb8363fa29c485b7163180938937a6880551677d16c3d4e9.jpg)

<details>
<summary>text_image</summary>

Configuración
* SSID OPPO Reno10 5G
Contraseña ..........
Cifrado AUTO
MQTT No Yes Flujo de comunicación MQTT
* Modo Modo personalizado
* Host rp10.rcr-labs.com
* Puerto 1883
ID de cliente equipo-3
Nombre de usuario Alumno
Contraseña ..........
SSL No Yes
Cancelar Aplicación
</details>

Asimismo, se configuraron los tópicos de publicación y suscripción para el envío y recepción de información en tiempo real. Se configuró la conexión de red del dispositivo XIAO ESP32S3 Sense mediante una red WiFi con acceso a internet.

![](images/280db844420f621eb1f6f5da282223b21259ad81127db9df594ae3259ed7b16d.jpg)

<details>
<summary>text_image</summary>

Subscribe
Topic
Dashboard
Subscribe
sscma/v0/equipo-3/rx
Enabled
Publish
sscma/v0/equipo-3/tx
Enabled
Settings
sscma/v0/equipo-3/tx
Enabled
sscma/v0/equipo-3/tx
Enabled
sscma/v0/equipo-3/tx
Enabled
sscma/v0/equipo-3/tx
Enabled
sscma/v0/equipo-3/tx
Enabled
</details>

Posteriormente, se establecieron los parámetros de conexión MQTT, definiendo como host el servidor rp10.rcr-labs.com y utilizando el puerto 1883, correspondiente al protocolo MQTT estándar.

![](images/68309aa624d3beded0e832d64e3344d7b7d811f9140a77cba19cd534b14059c4.jpg)

<details>
<summary>text_image</summary>

MQTT Broker
Host
rp10.rcr-labs.com
Port
1883
MQTT V3
✓ MQTT V5
Credentials
Username (optional)
Alumno
Password (optional)
..........
Advanced
Connect
</details>

Finalmente, se verificó la correcta conexión con el broker MQTT y la transmisión de mensajes desde el dispositivo.

# Discusión

El análisis de la implementación revela una discrepancia entre el rendimiento del algoritmo de inferencia y la capa de transporte de datos. Si bien el despliegue del modelo de TinyML en el dispositivo XIAO ESP32S3 Sense fue exitoso, la fase de telemetría mediante el protocolo MQTT presentó una interrupción en el flujo de datos hacia la interfaz móvil. Este comportamiento se puede dar debido a diferentes variables como:

1. Priorización de Procesamiento (CPU Contention): La ejecución de redes neuronales convolucionales en tiempo real demanda una alta tasa de ciclos de reloj. Se postula que la carga computacional de la inferencia limitó los recursos destinados al stack de red, generando una latencia superior al umbral de Keep-Alive del broker, lo que resulta en desconexiones intermitentes.

2. Arquitectura del Broker y Encapsulamiento: La falta de visibilidad de los datos sugiere una incompatibilidad en la capa de transporte. Mientras que el microcontrolador opera sobre TCP/IP (puerto 1883), las aplicaciones móviles suelen requerir una encapsulación mediante WebSockets. La ausencia de un bridge configurado en el servidor MQTT explicaría la nulidad en la recepción de los payloads.

3. Restricciones de la Infraestructura de Red: Factores externos como la segmentación de red o la implementación de políticas de seguridad en el router (aislamiento de nodos) pudieron actuar como barreras para el tráfico de paquetes entre los clientes suscriptores y el publicador.

# Conclusión

El modelo de inteligencia artificial logró reconocer y detectar correctamente los diferentes colores lapiceros en tiempo real mediante la cámara del dispositivo XIAO ESP32S3 Sense
