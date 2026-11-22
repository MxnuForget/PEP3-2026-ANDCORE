# Avance de hardware y configuración inicial — ANDCORE

**Integrante responsable:** Emanuel Flores Torrico  
**Grupo:** ORION X  
**Proyecto:** ANDCORE — Observatorio estadístico de eventos astronómicos visibles desde Cochabamba

## Trabajo realizado

En esta etapa me encargué de preparar la parte física y la configuración inicial de la Raspberry Pi que vamos a utilizar en ANDCORE. El equipo es una Raspberry Pi 4 Model B de 4 GB.

Primero trabajé en la preparación del almacenamiento con Raspberry Pi Imager y en dejar listo el sistema para comenzar a utilizar la placa. Después realicé las comprobaciones de red para localizar la Raspberry Pi y trabajar con ella desde mi Mac.

También configuré el acceso remoto mediante SSH. De esta forma puedo entrar a la terminal de la Raspberry Pi desde la Mac y continuar con la configuración sin tener que usar siempre un monitor y teclado conectados directamente al equipo.

Una vez dentro del sistema, instalé y comprobé las herramientas necesarias para comenzar a trabajar con Python. Se verificaron Python 3.13.5 y Git 2.47.3, además de los paquetes python3-venv, python3-pip y python3-dev.

Después creé el entorno virtual .venv dentro de la carpeta ANDCORE y preparé una estructura inicial para separar las partes del proyecto: captura, dashboard, datos, estadística, procesamiento y pruebas.

Por último, como parte del cuidado del hardware, realicé el montaje de un ventilador y coloqué disipadores para ayudar a controlar la temperatura de la Raspberry Pi durante su funcionamiento.

## Resultado de esta etapa

- Raspberry Pi 4 Model B de 4 GB preparada para continuar con el proyecto.
- Acceso remoto por SSH trabajado desde la Mac.
- Python y Git instalados y comprobados.
- Entorno virtual de Python creado y activado.
- Carpetas iniciales de ANDCORE organizadas en la Raspberry Pi.
- Ventilador y disipadores incorporados para apoyar la refrigeración.

## Lo que sigue

El equipo continúa trabajando en el desarrollo del código Python y en la búsqueda de una cámara que sea compatible con la Raspberry Pi 4. Cuando se tenga la cámara, se podrá avanzar con las pruebas de captura y después con los módulos de procesamiento y análisis.

## Evidencias

Las capturas del procedimiento se registran en la guía de [evidencias](evidencias/README.md). El detalle técnico de comandos, versiones y estructura está en [configuración inicial de Raspberry Pi](configuracion-raspberry-pi.md).

**Nota:** este avance corresponde a la preparación del hardware y del entorno. No afirma que la captura astronómica, la detección de eventos o el dashboard estén terminados.
