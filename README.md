# 🎓 UNIVERSIDAD PERUANA CAYETANO HEREDIA

<p align="center">
  <img width="340" height="148" alt="logo UPCH" src="https://github.com/user-attachments/assets/80cbe9aa-bd46-4400-a791-c427f82c725b" />
</p>
    
## Grupo 3 - Proyectos de Ingeniería I 

# "Riego automatizado por gravedad e interpolación espacial"

## 🔎 Objetivo del Proyecto 

Diseñar y desarrollar un sistema inteligente y autónomo que permita monitorear en tiempo real variables críticas del suelo, específicamente humedad, temperatura y macronutrientes (NPK). Utilizando tecnología de transmisión LoRa y microcontroladores ESP32, los datos capturados en campo alimentan un algoritmo de interpolación espacial en un servidor base, el cual estima las condiciones del suelo en áreas sin cobertura física de sensores. 

El proyecto está dirigido a pequeños y medianos agricultores, permitiéndoles visualizar mapas de estado a través de una aplicación móvil y recibir notificaciones de alerta automatizadas. A través de esta solución, se controla con precisión la apertura del riego por gravedad, logrando mejorar la eficiencia en el uso del agua, evitar la lixiviación de nutrientes y aumentar la productividad agrícola.

## 👥 Integrantes del Equipo y Roles

Para el desarrollo integral del prototipo, las tareas se dividieron de forma multidisciplinaria aprovechando los perfiles de Ingeniería Informática e Ingeniería Ambiental:

| Integrantes | Carrera | Cargo / Rol Principal | Contacto |
| :--- | :--- | :--- | :--- |
| Deza Mamani, Erick Armando | Ingeniería Ambiental | **Gestor de Datos:** Lógica ambiental para el algoritmo de interpolación y validación de umbrales NPK. | erick.deza@upch.pe |
| Herrera Tumba, Oscar Manuel | Ingeniería Ambiental | **Control de Calidad:** Redacción de la documentación técnica, validación de normativas y pruebas de campo. | oscar.herrera@upch.pe |
| Nunton Fajardo, Leonardo Javier | Ingeniería Informática | **Desarrollador IoT:** Programación de microcontroladores, conexiones de hardware y administración del repositorio. | leonardo.nunton@upch.pe |
| Orozco Mendoza, Enrique Alejandro | Ingeniería Informática | **Diseñador de Hardware:** Documentación del circuito electrónico, esquemáticos y modelado 3D de estructuras. | enrique.orozco@upch.pe |
| Sanchez Ticllasuca, Brenda Estefany | Ingeniería Ambiental | **Especialista Agrícola:** Gestión de cultivos, macetas de prueba (rabanitos) y validación de sustrato. | brenda.sanchez@upch.pe |

## 🛠️ Tecnologías y Herramientas

* **Microcontroladores:** ESP32 (SoC con Wi-Fi/Bluetooth).
* **Telecomunicaciones:** Radiofrecuencia LoRa (Módulo SX1278).
* **Sensores de Suelo:** Sensor industrial NPK (RS485), capacitivos de humedad y sondas DS18B20.
* **Gestión de Energía:** Baterías Li-ion 18650, módulos TP4056 y elevadores MT3608.
* **Plataforma IoT:** Dashboard en App móvil para visualización y alertas push.

## 🏗️ Arquitectura del Sistema

El flujo de información opera bajo la siguiente topología:
1. **Captura (Nodo Emisor):** El ESP32 en campo lee los datos del suelo y gestiona la energía.
2. **Transmisión (LoRa):** Envío de datos inalámbricos a larga distancia hacia la base.
3. **Procesamiento (Nodo Base):** Recepción de datos, ejecución del algoritmo de interpolación espacial y control de la electroválvula.
4. **Visualización:** Sincronización con la nube para actualizar la App móvil del usuario.

## 📂 Estructura del Repositorio

El repositorio está organizado para separar la documentación oficial de las prácticas del curso:

```text
📁 PI_Grupo3/
├── 📄 README.md                        # Presentación principal del proyecto
└── 📁 Proyectos_Ingenieria_1/
    ├── 📁 Proyecto/                    # Documentación técnica oficial
    │   ├── 📁 img/                     # Recursos visuales y diagramas
    │   ├── 📄 1.1 Definición del problema.md
    │   ├── 📄 1.2 Contextos.md
    │   ├── 📄 2. Estado del arte.md
    │   ├── 📄 3. Lista_exigencias.md
    │   ├── 📄 4. Caja_negra.md
    │   ├── 📄 5. Esquema_de_funciones.md
    │   └── 📄 6. Matriz_morfologica.md
    └── 📁 Talleres/                    # Prácticas y asignaciones del curso
        ├── 📁 Taller_DL/
        ├── 📁 Taller_EasyEDA/
        ├── 📁 Taller_Machine_Learning/
        ├── 📁 Taller_semana_2/
        └── 📁 Taller_semana5/