# 🌌 ANDCORE

**Observatorio Estadístico: Predicción de Eventos Astronómicos Visibles desde Cochabamba**

Proyecto Final de *Probabilidad y Estadística* — Ingeniería en Sistemas
Universidad Privada Franz Tamayo (Unifranz) · Cochabamba, Bolivia · 2026
Docente: Diego Patrick Cardenas Sejas

> 🚧 **Estado del proyecto:** en desarrollo. Este README se actualiza a medida que avanzamos.

---

## 📖 ¿Qué es ANDCORE?

ANDCORE es una estación de observación del cielo nocturno hecha con una **Raspberry Pi** y una cámara, que combina:

1. **Datos propios:** imágenes y video del cielo de Cochabamba, procesados con visión por computadora para detectar posibles meteoros y satélites.
2. **Datos abiertos:** información de la **NASA** (asteroides cercanos a la Tierra) y la **NOAA** (actividad geomagnética, índice Kp).
3. **Estadística y probabilidad:** con todo lo anterior estimamos *qué tan probable es ver un evento astronómico desde Cochabamba en una fecha determinada*, tomando en cuenta factores locales como la nubosidad y la temporada del año.

El resultado final es una predicción entendible para cualquier persona, por ejemplo:

> *"Probabilidad de observar la lluvia de meteoros Oriónidas esta semana desde Cochabamba: 70%"*

---

## ❓ Problema que resuelve

Hoy, quien quiere observar un fenómeno astronómico en Cochabamba depende de fuentes internacionales genéricas que dicen *cuándo ocurre* el evento, pero no *qué tan probable es verlo desde aquí*. Una lluvia de meteoros puede estar en su pico, pero si la noche está nublada (algo común en la temporada de lluvias, de noviembre a marzo) o hay mucha luz en la ciudad, la experiencia cambia por completo.

Además, en Unifranz no existen antecedentes de proyectos estudiantiles que unan datos astronómicos reales con métodos estadísticos. ANDCORE busca ser ese primer antecedente.

### ¿A quién le sirve?

- **Estudiantes y aficionados a la astronomía** que quieren saber cuándo salir a observar.
- **Colegios y universidades**, como recurso didáctico.
- **Radioaficionados, aviación local y agricultura de precisión**, sensibles a tormentas geomagnéticas.
- **Turismo local**, para promocionar noches de observación en zonas como el Parque Tunari o el Cerro San Pedro.

---

## 🎯 Objetivos

1. Capturar imágenes del cielo nocturno con una Raspberry Pi (meta: al menos 4 horas por noche durante el periodo de prueba).
2. Detectar eventos (destellos/movimiento compatibles con meteoros o satélites) usando **OpenCV**, y medir los falsos positivos con revisión manual de una muestra.
3. Integrar la API **NASA NeoWs** y el índice **Kp de la NOAA** en una base de datos histórica.
4. Aplicar **estadística descriptiva e inferencial** (distribución de frecuencias, intervalos de confianza, regresión) para estimar la probabilidad de observación.
5. Mostrar los resultados en un **dashboard** claro para usuarios no especializados.
6. Evaluar la precisión del modelo comparándolo con al menos **3 eventos reales** ocurridos durante el desarrollo.

---

## 🧱 Arquitectura general

```
   ┌───────────────┐      ┌────────────────┐      ┌──────────────────┐
   │ Cámara + RPi  │ ───▶ │  Detección de  │ ───▶ │                  │
   │ (cielo real)  │      │  eventos (CV)  │      │   Base de datos  │
   └───────────────┘      └────────────────┘      │  (CSV / SQLite)  │
                                                  │                  │
   ┌───────────────┐      ┌────────────────┐      │                  │
   │ NASA NeoWs    │ ───▶ │  Recolección   │ ───▶ │                  │
   │ NOAA Kp       │      │  de APIs       │      └────────┬─────────┘
   └───────────────┘      └────────────────┘               │
                                                           ▼
                                              ┌──────────────────────┐
                                              │ Análisis estadístico │
                                              │ (pandas, scipy)      │
                                              └──────────┬───────────┘
                                                         ▼
                                              ┌──────────────────────┐
                                              │ Dashboard (Streamlit)│
                                              │ "Probabilidad: 70%"  │
                                              └──────────────────────┘
```

---

## 🛠️ Tecnologías

| Componente | Tecnología |
|---|---|
| Hardware | Raspberry Pi 4 (4GB), módulo de cámara o webcam USB, trípode |
| Sensor (opcional) | DHT22 o BME280 (temperatura y humedad) |
| Lenguaje | Python 3 |
| Visión por computadora | OpenCV |
| Análisis estadístico | pandas, numpy, scipy |
| Visualización | matplotlib, Streamlit |
| Datos abiertos | NASA NeoWs, NOAA SWPC |

Todo el software es **100% código abierto y gratuito**.

---

## 💰 Costo estimado del hardware

| Recurso | Costo aprox. (Bs.) |
|---|---|
| Raspberry Pi 4 (4GB) | 450 – 600 |
| Módulo de cámara / webcam nocturna | 150 – 250 |
| Sensor DHT22 / BME280 (opcional) | 50 – 80 |
| Tarjeta microSD 32GB | 60 – 90 |
| Trípode / soporte fijo | 80 – 150 |
| Cables y accesorios | 50 – 100 |
| **Total aproximado** | **840 – 1.270** |

---

## 📁 Estructura del repositorio

> Estructura planificada; puede cambiar durante el desarrollo.

```
ANDCORE/
├── README.md
├── requirements.txt
├── captura/           # Scripts de captura con la cámara (Raspberry Pi)
├── deteccion/         # Algoritmo de detección de eventos con OpenCV
├── apis/              # Conexión con NASA NeoWs y NOAA Kp
├── analisis/          # Estadística descriptiva e inferencial
├── dashboard/         # Panel visual (Streamlit)
├── datos/             # Datos recolectados (CSV / SQLite)
└── docs/              # Informe, capturas y anexos
```

---

## ⚙️ Instalación

```bash
# 1. Clonar el repositorio
git clone <URL-DEL-REPOSITORIO>
cd ANDCORE

# 2. Crear un entorno virtual
python3 -m venv venv
source venv/bin/activate        # En Windows: venv\Scripts\activate

# 3. Instalar dependencias
pip install -r requirements.txt
```

**Dependencias principales:** `opencv-python`, `pandas`, `numpy`, `scipy`, `matplotlib`, `streamlit`, `requests`.

### Claves de API

- **NASA NeoWs:** se puede probar con la clave pública `DEMO_KEY`, pero tiene límites de uso. Se recomienda generar una clave gratuita en [api.nasa.gov](https://api.nasa.gov).
- **NOAA SWPC:** no requiere clave.

---

## ▶️ Uso

> Los scripts se irán agregando conforme avance el desarrollo.

```bash
# Capturar el cielo (en la Raspberry Pi)
python captura/capturar.py

# Descargar datos de NASA y NOAA
python apis/descargar_datos.py

# Ejecutar el análisis estadístico
python analisis/probabilidad.py

# Abrir el dashboard
streamlit run dashboard/app.py
```

---

## 📍 Contexto local: ¿por qué Cochabamba?

- **Ubicación:** aprox. 17.4° S, 66.2° O, a unos 2.550 m s. n. m. La altura ayuda: menos atmósfera entre la cámara y el cielo.
- **Temporada seca (mayo – agosto):** cielos más despejados, ideal para observar.
- **Temporada de lluvias (noviembre – marzo):** mayor nubosidad, lo que baja la probabilidad de observación. Este es justamente el tipo de factor que el modelo estadístico debe capturar.
- **Contaminación lumínica:** el centro de la ciudad dificulta la observación; zonas altas y alejadas como el Parque Tunari, Sipe Sipe o Pairumani ofrecen mejores condiciones.
- **Eventos de interés a lo largo del año:** Oriónidas (octubre), Leónidas (noviembre), Gemínidas (diciembre), Eta Acuáridas (mayo) y Delta Acuáridas (julio – agosto).

---

## 🗺️ Hoja de ruta

### Alcance actual (semestre)
- [ ] Definir roles y distribución de tareas del equipo
- [ ] Armar la estación (Raspberry Pi + cámara)
- [ ] Primeras capturas nocturnas de prueba
- [ ] Script de descarga de datos NASA / NOAA
- [ ] Detección básica de eventos con OpenCV
- [ ] Análisis estadístico inicial (frecuencias, intervalos de confianza)
- [ ] Dashboard simple con la probabilidad de observación
- [ ] Comparación con al menos 3 eventos reales
- [ ] Informe final y anexos

### Mejoras futuras
- Sensor de calidad de cielo (**SQM**) para medir la contaminación lumínica.
- **Red de mini-observatorios** en distintos puntos de Cochabamba (por ejemplo, ciudad, valle y zona alta) para comparar condiciones.
- **Machine learning** para mejorar la detección automática de eventos.
- Alertas automáticas por **Telegram o WhatsApp** a aficionados y colegios.
- Integración de datos de nubosidad de pronóstico (por ejemplo, desde SENAMHI u otros servicios abiertos).
- Calendario público de **astroturismo** para Cochabamba y zonas cercanas.

---

## 👥 Equipo

| Integrante | Rol | Responsabilidades |
|---|---|---|
| _Por definir_ | _Por definir_ | _Por definir_ |

> La organización del equipo aún está en definición.

---

## ⚠️ Limitaciones conocidas

- Las pruebas de campo dependen del clima nocturno.
- La cámara es de bajo costo, así que su sensibilidad es limitada frente a la de equipos profesionales.
- Con poco tiempo de captura, los datos propios serán una **muestra pequeña**; los resultados estadísticos deben leerse con ese cuidado.

---

## 🙏 Agradecimientos y fuentes de datos

- [NASA Open APIs (NeoWs)](https://api.nasa.gov)
- [NOAA Space Weather Prediction Center](https://www.swpc.noaa.gov)
- Universidad Privada Franz Tamayo — Ingeniería en Sistemas
- Docente: Diego Patrick Cardenas Sejas

---

## 📄 Licencia

-Por definir
