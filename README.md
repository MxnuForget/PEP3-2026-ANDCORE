# ANDCORE 🌌
## Observatorio estadístico de eventos astronómicos visibles desde Cochabamba

Proyecto de la materia de Probabilidad y Estadística — Ingeniería en Sistemas  
Universidad Privada Franz Tamayo (Unifranz) · Cochabamba, Bolivia · 2026  
Grupo: **ORION X**

---

## ¿De qué trata el proyecto?

ANDCORE busca desarrollar un observatorio que permita estudiar eventos astronómicos visibles desde Cochabamba. La idea es reunir información del cielo, consultar datos de fuentes abiertas y utilizar herramientas estadísticas para analizar las condiciones de observación.

A futuro, el proyecto contempla utilizar una Raspberry Pi con una cámara, procesamiento de imágenes y un panel donde se puedan consultar los resultados. El desarrollo se realizará por etapas, por lo que no todas esas funciones están implementadas todavía.

## Avance actual de implementación

En esta etapa se trabajó principalmente en la preparación del equipo Raspberry Pi y en la organización inicial del proyecto.

| Área | Avance comprobable hasta esta entrega | Estado |
|---|---|---|
| Raspberry Pi | Preparación inicial del equipo y configuración para poder trabajar con él. | En proceso |
| Conexión remota | Conexión a la Raspberry Pi mediante SSH. | Realizado |
| Refrigeración | Instalación de un ventilador para ayudar a mantener la temperatura del equipo. | Realizado |
| Estructura del proyecto | Organización inicial de la documentación y planificación en GitHub. | Realizado |
| Captura de imágenes | Todavía no implementada; falta incorporar y probar la cámara. | Pendiente |
| Detección de eventos | Todavía no implementada. | Pendiente |
| Recolección de datos NASA / NOAA | Planificada, falta desarrollar la conexión y guardar los datos. | Pendiente |
| Análisis estadístico | Planificado, falta implementar los cálculos con datos recopilados. | Pendiente |
| Dashboard | Planificado, todavía no implementado. | Pendiente |

**Importante:** el proyecto sigue en desarrollo. En esta entrega se presenta el avance real de preparación del hardware y configuración inicial. No se considera implementada una función hasta que exista código y una prueba que lo demuestre.

## Tecnologías y recursos

| Recurso | Uso en el proyecto |
|---|---|
| Raspberry Pi 4 | Equipo principal para el observatorio. |
| Raspberry Pi OS | Sistema operativo del equipo. |
| SSH | Acceso remoto a la Raspberry Pi desde otro dispositivo. |
| Ventilador | Apoyo para la refrigeración de la Raspberry Pi. |
| Python 3 | Lenguaje previsto para el desarrollo del software. |
| Git y GitHub | Control de versiones, documentación y seguimiento del proyecto. |

Para las siguientes etapas se tiene previsto trabajar con OpenCV, pandas, NumPy, SciPy, Matplotlib y Streamlit. Estas herramientas forman parte de la planificación y no deben confundirse con módulos ya terminados.

## Organización del equipo

| Integrante | Responsabilidad registrada |
|---|---|
| Emanuel Flores Torrico | Hardware y captura. |
| Jhenny Puma Velásquez | Investigación y desarrollo. |
| Marcelo Andrés Gantier Rodríguez | Dashboard. |

## Evidencias del avance

Se cuenta con capturas del proceso de preparación y conexión de la Raspberry Pi, incluyendo los pasos de configuración por SSH y el trabajo realizado para instalar el ventilador.

Las capturas se incorporarán al repositorio en la carpeta `docs/evidencias/`, organizadas por etapas y con una breve descripción para que se pueda revisar el procedimiento.

> Las imágenes de evidencia deben corresponder a actividades realizadas por el equipo. No se utilizarán imágenes de ejemplo como si fueran pruebas del proyecto.

## Estructura actual del repositorio

```
PEP3-2026-ANDCORE/
├── ANDCORE/
│   ├── PLANIFICACION/
│   │   └── Gantt-ANDCORE-v1.jpeg
│   ├── PRESENTACIONES/
│   │   └── Presentacion-ANDCORE-v1..pdf
│   └── PROYECTO/
│       └── Documento-Proyecto-ANDCORE-v1.docx
├── docs/
│   └── evidencias/
├── Emanuel-Flores.txt
├── Jhenny-Puma.txt
├── Marcelo-Gantier.txt
├── LICENSE
└── README.md
```

La estructura se irá ampliando a medida que se desarrollen los módulos de software.

## Instalación y ejecución

Por el momento, el avance de esta etapa corresponde a la preparación y configuración inicial de la Raspberry Pi. Todavía no existe una aplicación completa de ANDCORE que se pueda ejecutar desde un único comando.

Cuando se incorporen los módulos de Python, se agregarán aquí los pasos de instalación de dependencias y ejecución de cada parte del sistema.

## Funcionalidades que faltan desarrollar

- Configurar e integrar la cámara para realizar capturas del cielo.
- Crear el módulo de recolección de información de fuentes abiertas, como NASA y NOAA.
- Guardar y organizar los datos obtenidos en archivos o una base de datos.
- Desarrollar una primera versión de detección de eventos con OpenCV.
- Aplicar análisis estadístico a los datos recopilados.
- Crear el dashboard para mostrar los resultados.
- Realizar pruebas y documentar los resultados obtenidos.

## Fuentes previstas

- NASA Open APIs: https://api.nasa.gov
- NOAA Space Weather Prediction Center: https://www.swpc.noaa.gov

Estas fuentes están consideradas para una etapa posterior de integración.

## Estado general

ANDCORE se encuentra en una etapa inicial de implementación. Ya se cuenta con la preparación básica de la Raspberry Pi, el acceso remoto mediante SSH, la instalación de un ventilador y la documentación de planificación del proyecto. El siguiente paso es continuar con la integración de la cámara y comenzar el desarrollo de los módulos de software.

---
**Grupo ORION X · Unifranz · 2026**
