# ANDCORE 🌌
## Observatorio estadístico de eventos astronómicos visibles desde Cochabamba

Proyecto de Probabilidad y Estadística — Ingeniería en Sistemas  
Universidad Privada Franz Tamayo (Unifranz), Cochabamba · 2026  
**Grupo: ORION X**

## ¿Qué es ANDCORE?

ANDCORE es un proyecto que busca estudiar eventos astronómicos que se puedan observar desde Cochabamba. La idea es reunir información del cielo y utilizar programación y estadística para analizar los datos y, más adelante, estimar la posibilidad de observar ciertos eventos.

El proyecto se está realizando por etapas. Primero trabajamos en preparar la Raspberry Pi y dejar listo el entorno para poder continuar con el desarrollo. Todavía estamos buscando una cámara compatible para empezar con las pruebas de captura del cielo.

## Avance del proyecto

Hasta el momento se trabajó en la preparación inicial del equipo:

| Área | Avance |
|---|---|
| Hardware | Se identificó y preparó una Raspberry Pi 4 Model B de 4 GB. |
| Sistema operativo | Se preparó la tarjeta de almacenamiento con Raspberry Pi Imager. |
| Conexión | Se trabajó en la conexión de red y el acceso remoto mediante SSH. |
| Refrigeración | Se instaló un ventilador y se colocaron disipadores para ayudar a controlar la temperatura de la Raspberry Pi. |
| Python | Se instaló y comprobó Python 3.13.5. |
| Entorno virtual | Se creó y activó el entorno virtual `.venv` dentro de la carpeta de trabajo. |
| Herramientas | Se instalaron o comprobaron Git 2.47.3, `python3-venv`, `python3-pip` y `python3-dev`. |
| Organización | Se creó la estructura inicial de carpetas para separar las distintas partes del proyecto. |
| Cámara | Seguimos buscando una cámara que sea compatible con la Raspberry Pi 4. |
| Programación | El grupo continúa trabajando en el desarrollo del código Python. |

Por ahora, el avance corresponde principalmente a la preparación del hardware y del entorno de trabajo. Los módulos del observatorio todavía deben desarrollarse y probarse.

## Trabajo realizado en la Raspberry Pi

Como parte de la preparación inicial se realizaron estos pasos:

1. Identificación de la Raspberry Pi 4 Model B de 4 GB.
2. Preparación de la tarjeta de almacenamiento utilizando Raspberry Pi Imager.
3. Configuración de la conexión de red y del acceso remoto por SSH.
4. Comprobación de la dirección IP local desde la terminal.
5. Instalación y comprobación de Python, Git y las herramientas necesarias.
6. Creación y activación de un entorno virtual de Python.
7. Creación de las carpetas iniciales para organizar el proyecto.
8. Instalación del ventilador y colocación de disipadores para mejorar la refrigeración del equipo.

Los comandos y datos técnicos que se pudieron registrar están en [Configuración inicial de Raspberry Pi](docs/configuracion-raspberry-pi.md). También se puede revisar el [avance de hardware](docs/avance-hardware.md).

## Estructura inicial de trabajo

En la terminal de la Raspberry Pi se creó la siguiente estructura dentro de la carpeta `~/ANDCORE`:

```text
ANDCORE/
├── captura/
├── dashboard/
├── datos/
├── estadistica/
├── main.py
├── procesamiento/
├── pruebas/
├── README.md
├── requirements.txt
└── .venv/
```

Esta es la estructura que se preparó en la Raspberry Pi para organizar el trabajo. La presencia de los archivos y carpetas en esa estructura no significa que todos los módulos ya estén desarrollados. El entorno virtual `.venv` es local y no se incluye en este repositorio.

## Herramientas y recursos

| Recurso | Uso en el proyecto |
|---|---|
| Raspberry Pi 4 Model B (4 GB) | Equipo principal para las pruebas del observatorio. |
| Raspberry Pi OS | Sistema operativo de la Raspberry Pi. |
| SSH | Acceso remoto al equipo desde otra computadora. |
| Python 3.13.5 | Lenguaje preparado para el desarrollo. |
| Git 2.47.3 y GitHub | Control de versiones y almacenamiento del proyecto. |
| Ventilador y disipadores | Ayudan a mantener la temperatura del equipo. |

Para las siguientes etapas se tiene previsto trabajar con herramientas como OpenCV, NumPy, pandas, SciPy, Matplotlib y Streamlit. También se considera utilizar información abierta de NASA y NOAA. Su integración se realizará conforme avance el desarrollo.

## Integrantes y responsabilidades

| Integrante | Responsabilidad |
|---|---|
| Emanuel Flores Torrico | Hardware y captura. |
| Jhenny Puma Velásquez | Investigación y desarrollo. |
| Marcelo Andrés Gantier Rodríguez | Dashboard. |

El grupo continúa avanzando en el código Python y en la búsqueda de una cámara adecuada para la Raspberry Pi 4.

## Evidencias del trabajo

En [docs/evidencias](docs/evidencias/) se encuentran las 10 fotografías del trabajo realizado con la Raspberry Pi. En ellas se puede observar la placa, la preparación del almacenamiento, las comprobaciones de red, el trabajo desde la terminal, la instalación de herramientas, la estructura inicial y el montaje del sistema de refrigeración.

Estas imágenes corresponden al proceso realizado y sirven como respaldo del avance de hardware y configuración.

## Estado del software

En esta etapa todavía no contamos con una versión completa del observatorio lista para ejecutar. Primero se preparó el equipo y el entorno donde se continuará trabajando. Por eso, las funciones de captura, procesamiento, detección de eventos, análisis estadístico y dashboard siguen pendientes de desarrollo e integración.

Cuando estén implementadas, se agregarán aquí las instrucciones para instalar las dependencias, ejecutar el programa y revisar las pruebas realizadas.

## Próximas tareas

- Elegir y probar una cámara compatible con la Raspberry Pi 4.
- Realizar las primeras pruebas de captura de imágenes.
- Continuar desarrollando los módulos en Python.
- Trabajar en el procesamiento de imágenes y la detección de posibles eventos.
- Incorporar datos de fuentes abiertas, como NASA y NOAA.
- Realizar el análisis estadístico y preparar el dashboard.
- Registrar las pruebas y los resultados obtenidos.

## Fuentes que se tienen previstas

- NASA Open APIs: https://api.nasa.gov
- NOAA Space Weather Prediction Center: https://www.swpc.noaa.gov

---

**Grupo ORION X · Unifranz · 2026**
