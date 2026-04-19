# 🏎️ WRO Vision Pro — Future Engineers

**Sistema de Visión Artificial en Tiempo Real para WRO (World Robot Olympiad)**

Este proyecto es una plataforma avanzada de visión computacional basada en navegador, diseñada para la categoría **Future Engineers**. Permite el procesamiento de imágenes de alta velocidad, la toma de decisiones lógica y la comunicación directa con microcontroladores (Arduino, ESP32, Raspberry Pi) mediante protocolos industriales.

---

## 👤 Autor
**Creado por Ing. José Rojas**

---

## 🚀 Características Principales

### 🧠 Visión Computacional Avanzada
- **Segmentación de Paredes (Segmented Mask):** A diferencia de los métodos tradicionales de Bounding Box, este sistema utiliza una máscara de segmentación por píxeles para detectar la pista. Esto permite que la detección de paredes laterales no bloquee la lectura de los obstáculos centrales (Rojo/Verde), manteniendo el área de "Drive" despejada.
- **Detección Multi-Color (HSV Clustering):** Algoritmos optimizados para identificar:
  - 🔴 **Obstáculos Rojos:** Evasión hacia la derecha.
  - 🟢 **Obstáculos Verdes:** Evasión hacia la izquierda.
  - 🟣 **Zona de Meta (Parking):** Frenado de precisión.
  - 🟠🔵 **Líneas Guía:** Centrado automático en carril.
- **Auto-Calibración:** Interfaz interactiva para calibrar colores simplemente haciendo clic en el video.

### 📡 Comunicación y Telemetría
- **Web Serial API:** Conectividad USB directa a 115200 baudios (o más) sin necesidad de software intermedio.
- **WebSockets:** Soporte nativo para comunicación inalámbrica (WiFi) con ESP32 o Raspberry Pi.
- **Dashboard en Tiempo Real:** Visualización de ángulos de giro, estado de amenaza inminente y tasa de transmisión (Hz).

---

## 🛠️ Cómo Utilizar

1.  **Requisitos:** Utilizar un navegador basado en Chromium (**Google Chrome** o **Microsoft Edge**).
2.  **Apertura:** Abrir el archivo `index.html` localmente.
3.  **Conexión:** 
    - Conectar el robot vía USB.
    - Seleccionar el puerto serie en el panel "Enlace con el Robot".
4.  **Calibración:**
    - Hacer clic en "🎯 Auto" en los paneles de color.
    - Seleccionar el color correspondiente en el video/imagen para que el sistema aprenda el tono (Hue/Sat) ambiental.
5.  **Simulación:** Puedes usar la carpeta `media/` para cargar videos de pruebas previas y validar la lógica antes de poner el robot en pista.

---

## 📂 Estructura del Proyecto

- `index.html`: Núcleo de la aplicación (UI, Lógica de Visión, Motores de Comunicación).
- `media/`: Carpeta para almacenamiento de recursos (imágenes y videos de prueba).
- `README.md`: Documentación del sistema.

---

## ⚖️ Licencia
Este proyecto es una herramienta educativa de alto rendimiento para equipos de ingeniería WRO.
