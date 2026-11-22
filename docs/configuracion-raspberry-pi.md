# Configuración inicial de Raspberry Pi — ANDCORE

**Responsable de esta etapa:** Emanuel Flores Torrico  
**Grupo:** ORION X  
**Equipo:** Raspberry Pi 4 Model B, 4 GB de RAM

Este documento registra lo que se preparó en la Raspberry Pi para comenzar el trabajo de ANDCORE. Se basa en las capturas del procedimiento y en la información confirmada por el integrante responsable.

## 1. Preparación del equipo

Se trabajó con una Raspberry Pi 4 Model B de 4 GB. Antes de comenzar con el desarrollo se preparó el almacenamiento para instalar el sistema operativo usando Raspberry Pi Imager.

En una de las capturas se observa Raspberry Pi Imager v2.0.12 realizando la verificación de los datos escritos. Esa imagen corresponde al proceso de verificación en curso; no se utiliza como prueba de que esa pantalla ya había terminado.

## 2. Conexión de red y acceso remoto

Se realizaron comprobaciones desde la Mac para localizar la Raspberry Pi dentro de la red local. En las primeras pruebas, el nombre raspberrypi.local no se resolvió, por lo que se continuó revisando los dispositivos de la red.

En la terminal de la Raspberry Pi se ejecutó el comando hostname -I. La captura muestra como dirección local 192.168.20.17.

También se trabajó con SSH para acceder a la Raspberry Pi de forma remota desde la Mac. Este acceso permite administrar el equipo desde la terminal sin depender de tener monitor y teclado conectados todo el tiempo.

> La dirección IP de la captura es una dirección privada de la red local. Puede cambiar cuando el router asigna una nueva dirección.

## 3. Sistema y herramientas instaladas

Las capturas de la terminal permiten registrar estos datos:

| Elemento | Dato observado |
|---|---|
| Distribución | Debian GNU/Linux 13 (Trixie), arquitectura arm64 |
| Kernel | 6.18.5+rpt-rpi-v8 |
| Python | 3.13.5 |
| Git | 2.47.3 |
| Memoria detectada | 3.7 GiB en la salida de free -h |
| Almacenamiento | Partición principal /dev/mmcblk0p2, con 58 GB mostrados en df -h |

También aparece el comando de instalación:

    sudo apt install -y git python3-venv python3-pip python3-dev

En la captura, los paquetes indicados aparecen como instalados o en su versión más reciente. Se comprobó Git y Python desde la terminal.

## 4. Entorno virtual de Python

Dentro de la carpeta del proyecto se creó el entorno virtual con estos comandos:

    mkdir -p ~/ANDCORE
    cd ~/ANDCORE
    python3 -m venv --system-site-packages .venv
    source .venv/bin/activate

Con el entorno activado se realizaron estas comprobaciones:

    python --version
    git --version
    free -h
    df -h

La terminal muestra Python 3.13.5 y Git 2.47.3. El prefijo (.venv) en la terminal permite reconocer que el entorno virtual estaba activado.

La opción --system-site-packages se utilizó al crear el entorno, tal como aparece en la captura. No se debe asumir que ya están instaladas todas las bibliotecas que se usarán en el observatorio.

## 5. Estructura inicial del proyecto en la Raspberry Pi

La salida de tree -a -L 2 muestra esta estructura:

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
        ├── bin/
        ├── include/
        ├── lib/
        ├── lib64 -> lib
        └── pyvenv.cfg

Esta es la estructura inicial observada en la Raspberry Pi. Las carpetas se prepararon para separar las distintas partes que tendrá el proyecto:

- captura/: espacio previsto para el trabajo de captura.
- dashboard/: espacio previsto para el panel de visualización.
- datos/: espacio previsto para guardar información.
- estadistica/: espacio previsto para los análisis.
- procesamiento/: espacio previsto para el procesamiento.
- pruebas/: espacio previsto para pruebas.
- main.py: archivo principal previsto para organizar la ejecución.
- requirements.txt: archivo previsto para registrar dependencias.
- .venv/: entorno virtual local de Python.

**Importante:** la existencia de estos nombres y carpetas no significa que los módulos ya estén desarrollados. Se trata de la organización inicial que se preparó para continuar trabajando.

El entorno .venv es local y no se debe subir a GitHub. Para recrearlo se pueden seguir los comandos de la sección 4.

## 6. Refrigeración del equipo

Como parte de la preparación física de la Raspberry Pi se realizó el montaje de un ventilador y se colocaron disipadores sobre los componentes. La finalidad es ayudar a reducir la acumulación de calor durante el funcionamiento del equipo.

Las fotografías muestran la placa, los disipadores y el cableado conectado a los pines GPIO. El montaje del ventilador forma parte del trabajo de hardware realizado para ANDCORE.

## 7. Estado después de esta etapa

Al terminar esta parte del trabajo, se cuenta con:

- Raspberry Pi 4 Model B de 4 GB preparada.
- Sistema instalado y equipo accesible para continuar la configuración.
- Acceso remoto mediante SSH trabajado desde la Mac.
- Python 3.13.5 y Git 2.47.3 comprobados.
- Entorno virtual .venv creado y activado.
- Estructura inicial de carpetas de ANDCORE preparada.
- Ventilador y disipadores incorporados como apoyo para la refrigeración.

Todavía queda pendiente integrar la cámara y desarrollar los módulos de captura, procesamiento, análisis estadístico y visualización.

---
**Registro de configuración inicial · ANDCORE · Grupo ORION X**
