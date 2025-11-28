# 🌍 Dashboard de Monitoreo de Emisiones Fugitivas

Dashboard interactivo desarrollado con Streamlit para el análisis y visualización de emisiones de metano (CH₄) y otros gases de efecto invernadero detectados mediante tecnología satelital.

## 🚀 Demo en Vivo

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://your-app-url.streamlit.app)

## ✨ Características Principales

### 📊 KPIs y Métricas
- **Indicadores de Emission Rate**: Total, Mayor/Menor emisor, Promedio por instalación
- **Métricas de Concentración CH₄**: Total de puntos, Pico máximo/mínimo, Promedio

### 🗺️ Visualización Geoespacial
- Mapa satelital interactivo con Folium
- Marcadores coloreados por intensidad de emisión
- Navegación a puntos críticos con un clic
- Detección automática de campos/instalaciones

### 📈 Análisis Avanzados

#### 1. **Ranking de Emisiones**
- Top instalaciones ordenadas por tasa de emisión
- Gráfico de barras horizontales interactivo
- Estadísticas detalladas por instalación

#### 2. **Correlación Emission Rate vs CH₄**
- Scatter plot interactivo con umbrales configurables
- Análisis por cuadrantes (Crítico, Anomalía, Revisar, Óptimo)
- Tablas de instalaciones que requieren atención

#### 3. **Serie Temporal**
- Evolución de emisiones en el tiempo
- Filtros por instalación con multiselect
- Agregación por día o mes
- Detección de patrones y tendencias

#### 4. **Inventario de Emisiones**
- Total acumulado por instalación
- Vista mensual con desglose temporal
- Top 3 contribuyentes al total
- Métricas OGMP-ready

#### 5. **Análisis de Viento**
- Rosa de vientos por instalación
- Distribución de velocidad y dirección
- Correlación viento-emisiones

#### 6. **Estadísticas y Exportación**
- Resumen estadístico completo
- Exportación a Excel con múltiples hojas
- Filtros por fecha y campo

## 🛠️ Instalación Local

### Prerrequisitos
- Python 3.8 o superior
- pip

### Pasos de Instalación

```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/tu-repositorio.git
cd tu-repositorio

# Crear entorno virtual (recomendado)
python -m venv .venv

# Activar entorno virtual
# Windows PowerShell:
.\.venv\Scripts\Activate.ps1
# Windows CMD:
.\.venv\Scripts\activate.bat
# Linux/Mac:
source .venv/bin/activate

# Instalar dependencias
pip install -r requirements.txt

# Ejecutar la aplicación
streamlit run app.py
```

## 📦 Dependencias Principales

- `streamlit` - Framework web interactivo
- `pandas` - Procesamiento de datos
- `plotly` - Visualizaciones interactivas
- `folium` - Mapas geoespaciales
- `openpyxl` - Lectura de archivos Excel

## 📂 Estructura del Proyecto

```
.
├── app.py                 # Aplicación principal
├── requirements.txt       # Dependencias
├── README.md             # Este archivo
├── .gitignore            # Archivos ignorados por Git
└── .streamlit/
    └── config.toml       # Configuración de Streamlit
```

## 🎯 Uso

1. **Cargar Datos**: Suba un archivo Excel (.xlsx) con datos de emisiones
2. **Seleccionar Hoja**: Elija la hoja que contiene los datos
3. **Verificar Columnas**: Confirme la detección automática de columnas
4. **Aplicar Filtros**: Use los filtros del sidebar para segmentar datos
5. **Explorar Tabs**: Navegue entre Mapa, Análisis de Emisiones, Viento y Estadísticas

### Formato de Datos Esperado

El archivo Excel debe contener al menos:
- **Latitud** (Latitude/Lat)
- **Longitud** (Longitude/Lon/Long)
- **Emission Rate** (kg/h)
- **Concentración CH₄** (ppm)
- **Facility Name** (nombre de instalación)
- **Fecha/Hora** (Scan Date Time UTC)

## 🎨 Paleta de Colores

La aplicación usa una paleta energética consistente:
- 🟢 Primary: #1ABC9C (Turquesa)
- 🔵 Secondary: #3498DB (Azul)
- 🟣 Accent: #9B59B6 (Púrpura)
- 🔴 Danger: #E74C3C (Rojo)
- 🟠 Warning: #F39C12 (Naranja)
- 🟢 Success: #27AE60 (Verde)

## 📊 Deployment en Streamlit Cloud

1. Sube tu repositorio a GitHub
2. Ve a [share.streamlit.io](https://share.streamlit.io)
3. Conecta tu repositorio
4. Selecciona `app.py` como archivo principal
5. Despliega

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:
1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📝 Licencia

Este proyecto está bajo licencia MIT. Ver archivo `LICENSE` para más detalles.

## 👥 Autores

- **Tu Nombre** - *Desarrollo Inicial*

## 🙏 Agradecimientos

- Streamlit por el framework
- Plotly por las visualizaciones
- Folium por los mapas interactivos
