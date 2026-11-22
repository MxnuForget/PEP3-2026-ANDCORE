# ANDCORE 🌌
## Observatorio estadístico de eventos astronómicos visibles desde Cochabamba

Proyecto de Probabilidad y Estadística — Ingeniería en Sistemas  
Universidad Privada Franz Tamayo (Unifranz), Cochabamba · 2026  
**Grupo: ORION X**

## ¿De qué trata ANDCORE?

ANDCORE es una propuesta de observatorio para estudiar eventos astronómicos que puedan observarse desde Cochabamba. La idea es reunir información del cielo, consultar fuentes abiertas y utilizar herramientas de programación y estadística para analizar los datos.

El proyecto se está desarrollando por etapas. En este momento el trabajo se concentró en preparar la Raspberry Pi, dejar listo el acceso remoto y organizar el entorno inicial para continuar con Python. La captura del cielo y el análisis de eventos todavía dependen de integrar y probar una cámara compatible.

## Avance actual

| Área | Trabajo realizado / estado |
|---|---|
| Hardware | Raspberry Pi 4 Model B de 4 GB identificada y preparada para el proyecto. |
| Sistema operativo | Preparación del almacenamiento mediante Raspberry Pi Imager. Las capturas muestran el proceso de escritura y verificación. |
| Red y acceso remoto | Se trabajó en la conexión de red y el acceso remoto por SSH. La terminal de la Raspberry muestra la IP local 192.168.20.17. |
| Refrigeración | Se realizó el montaje del ventilador y se colocaron disipadores para ayudar a controlar el calor del equipo. |
| Python | Python 3.13.5 instalado y comprobado desde la terminal. |
| Entorno virtual | Se creó y activó el entorno .venv dentro de la carpeta de trabajo ANDCORE. |
| Herramientas | Git 2.47.3, python3-venv, python3-pip y python3-dev aparecen instalados en las capturas. |
| Estructura inicial | Se organizaron carpetas para captura, dashboard, datos, estadística, procesamiento y pruebas. |
| Cámara | En búsqueda de un modelo compatible con la Raspberry Pi 4. |
| Software del observatorio | En desarrollo. Todavía no se presenta como terminado el procesamiento, la detección, el análisis ni el dashboard. |

**Aclaración:** la preparación del entorno y las carpetas es una base de trabajo. No significa que los módulos de captura, detección o análisis ya estén implementados.

## Preparación de la Raspberry Pi

El trabajo de hardware y configuración inicial registrado por Emanuel Flores Torrico incluye:

1. Preparación de la Raspberry Pi 4 Model B de 4 GB.
2. Preparación del almacenamiento con Raspberry Pi Imager.
3. Configuración de red y acceso remoto mediante SSH.
4. Comprobación de la dirección IP local desde la terminal de la Raspberry Pi.
5. Instalación y comprobación de Python y herramientas necesarias para trabajar.
6. Creación y activación de un entorno virtual de Python.
7. Organización de las carpetas iniciales del proyecto.
8. Montaje del ventilador y colocación de disipadores para apoyar la refrigeración.

El detalle de comandos, versiones y estructura observada está en [Configuración inicial de Raspberry Pi](docs/configuracion-raspberry-pi.md). El registro del trabajo de hardware está en [Avance de hardware](docs/avance-hardware.md).

## Estructura inicial creada en la Raspberry Pi

La captura de la terminal muestra esta organización dentro de ~/ANDCORE:

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

La carpeta .venv corresponde al entorno virtual local. No se debe subir al repositorio; se puede volver a crear siguiendo la documentación. Las carpetas representan la organización inicial y se irán completando conforme avance el desarrollo.

## Tecnologías y recursos

| Recurso | Uso |
|---|---|
| Raspberry Pi 4 Model B (4 GB) | Equipo principal del observatorio. |
| Raspberry Pi OS | Sistema operativo preparado para la placa. |
| SSH | Acceso remoto a la terminal. |
| Python 3.13.5 | Entorno de programación instalado. |
| Git 2.47.3 y GitHub | Control de versiones y documentación. |
| Ventilador y disipadores | Apoyo para la refrigeración. |

Para etapas posteriores se tiene previsto evaluar OpenCV, NumPy, pandas, SciPy, Matplotlib y Streamlit. También se considera consultar datos abiertos de NASA y NOAA. Estas herramientas e integraciones forman parte de la planificación y no se deben confundir con funciones ya terminadas.

## Organización del equipo

| Integrante | Responsabilidad registrada |
|---|---|
| Emanuel Flores Torrico | Hardware y captura. |
| Jhenny Puma Velásquez | Investigación y desarrollo. |
| Marcelo Andrés Gantier Rodríguez | Dashboard. |

El grupo continúa avanzando en la parte de programación en Python y en la búsqueda de una cámara que sea compatible con la Raspberry Pi 4.

## Evidencias

Se recibieron 10 capturas del proceso realizado: placa, preparación del almacenamiento, comprobaciones de red, terminal de la Raspberry, instalación de herramientas, entorno virtual, estructura de carpetas y montaje de refrigeración.

La guía para incorporarlas al repositorio está en [docs/evidencias](docs/evidencias/README.md). Las capturas deben conservarse como evidencia original y agregarse en esa carpeta; no se deben reemplazar por imágenes ilustrativas.

## Instalación y ejecución

Por ahora no existe una aplicación completa de ANDCORE lista para ejecutarse. Esta etapa corresponde a la preparación del equipo y del entorno de trabajo. Los pasos registrados para preparar Python y las carpetas están en la documentación técnica.

Cuando se implementen los módulos, se actualizará esta sección con las dependencias reales, comandos de ejecución y pruebas correspondientes.

## Próximas tareas

- Terminar la selección de una cámara compatible y realizar pruebas de captura.
- Desarrollar el módulo de captura de imágenes.
- Implementar la consulta y almacenamiento de información de fuentes abiertas como NASA y NOAA.
- Desarrollar el procesamiento de imágenes y la detección de posibles eventos.
- Aplicar el análisis estadístico a datos reales o de prueba, dejando claro su origen.
- Crear el dashboard y documentar pruebas de funcionamiento.

## Fuentes previstas

- NASA Open APIs: https://api.nasa.gov
- NOAA Space Weather Prediction Center: https://www.swpc.noaa.gov

**Estado general:** ANDCORE se encuentra en una etapa inicial. Ya se trabajó en la preparación de la Raspberry Pi, el acceso remoto, el entorno Python, la estructura de carpetas y la refrigeración. El equipo continúa con el desarrollo del software y la búsqueda de la cámara.

---
**Grupo ORION X · Unifranz · 2026**
