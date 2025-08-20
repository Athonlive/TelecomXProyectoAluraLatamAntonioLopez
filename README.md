# TelecomXProyectoAluraLatamAntonioLopez
Segundo challenge de alura latam
# 📊 TelecomX - Análisis de Datos de Telecomunicaciones

## 🎯 Propósito del Análisis

Este proyecto forma parte del **Desafío Alura Data Science** y tiene como objetivo principal **analizar el comportamiento de churn (abandono) de clientes** en una empresa de telecomunicaciones ficticia llamada TelecomX.

### Objetivos Específicos:

1. **Identificar patrones de churn** en la base de clientes
2. **Analizar factores de riesgo** que contribuyen al abandono de clientes
3. **Segmentar clientes** según su probabilidad de churn
4. **Generar insights accionables** para estrategias de retención
5. **Crear visualizaciones informativas** para stakeholders

### Preguntas de Negocio Respondidas:

- ¿Cuál es la tasa actual de churn y cómo se distribuye?
- ¿Qué características demográficas influyen en el churn?
- ¿Cómo afecta el tipo de contrato a la retención de clientes?
- ¿Qué servicios están asociados con mayor/menor churn?
- ¿Cuál es la relación entre permanencia y probabilidad de abandono?

## 🗂️ Estructura del Proyecto

```
TelecomX/
│
├── 📄 README.md                          # Documentación principal
├── 📓 TelecomX_Analisis.ipynb           # Notebook principal de análisis
├── 📁 datos/                            # Carpeta de datos
│   ├── telecom_clientes.csv            # Dataset principal
│   └── diccionario_datos.txt           # Descripción de variables
├── 📁 visualizaciones/                  # Gráficos generados
│   ├── churn_general.png               # Distribución general de churn
│   ├── churn_por_servicios.png         # Análisis por servicios
│   ├── permanencia_analisis.png        # Análisis de permanencia
│   └── matriz_correlacion.png          # Matriz de correlación
├── 📁 resultados/                       # Archivos de resultados
│   ├── resumen_metricas.csv            # Métricas principales
│   ├── insights_principales.txt        # Hallazgos clave
│   └── recomendaciones.md              # Recomendaciones estratégicas
└── 📁 scripts/                         # Scripts auxiliares
    ├── funciones_analisis.py           # Funciones reutilizables
    ├── visualizaciones.py              # Código de gráficos
    └── utils.py                        # Utilidades generales
```

## 📈 Ejemplos de Gráficos e Insights

### 1. Distribución General de Churn

**Gráfico:** Gráfico de torta mostrando la distribución entre clientes que permanecen vs. clientes que abandonan.

**Insight Clave:** 
- 27% de los clientes abandonaron el servicio
- Representa una oportunidad de mejora significativa
- La tasa está dentro del rango típico de la industria (20-35%)

### 2. Churn por Tipo de Contrato

**Gráfico:** Gráfico de barras comparando tasas de churn entre diferentes tipos de contrato.

**Insights Clave:**
- Contratos "Mes a mes": ~42% de churn
- Contratos "Un año": ~11% de churn  
- Contratos "Dos años": ~3% de churn
- **Recomendación:** Incentivar contratos de mayor duración

### 3. Análisis de Servicios

**Gráfico:** Heatmap mostrando correlación entre servicios contratados y churn.

**Insights Clave:**
- Clientes con fibra óptica tienen mayor tendencia al churn
- Servicios premium (streaming) pueden indicar mayor compromiso
- Clientes sin servicios adicionales son más propensos a irse

### 4. Permanencia vs. Churn

**Gráfico:** Histograma y boxplot mostrando distribución de meses de permanencia.

**Insights Clave:**
- Clientes con churn: promedio 18 meses de permanencia
- Clientes leales: promedio 37 meses de permanencia
- Primeros 6 meses son críticos para retención

### 5. Matriz de Correlación

**Gráfico:** Heatmap de correlaciones entre variables numéricas.

**Insights Clave:**
- Correlación negativa entre permanencia y churn (-0.35)
- Cargos mensuales altos se asocian con mayor churn
- Edad y churn tienen correlación débil

## 🚀 Instrucciones para Ejecutar el Notebook

### Prerrequisitos

1. **Python 3.8 o superior**
2. **Jupyter Notebook o JupyterLab**
3. **Librerías requeridas:**

```bash
pip install pandas numpy matplotlib seaborn plotly scikit-learn
```

### Opción 1: Instalación con requirements.txt

```bash
# Clonar el repositorio
git clone https://github.com/usuario/TelecomX.git
cd TelecomX

# Crear entorno virtual (recomendado)
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate

# Instalar dependencias
pip install -r requirements.txt

# Iniciar Jupyter
jupyter notebook
```

### Opción 2: Usando Anaconda

```bash
# Crear entorno conda
conda create -n telecomx python=3.9
conda activate telecomx

# Instalar librerías
conda install pandas numpy matplotlib seaborn jupyter
conda install -c plotly plotly

# Iniciar Jupyter
jupyter notebook
```

### Ejecución Paso a Paso

1. **Abrir el notebook:** `TelecomX_Analisis.ipynb`

2. **Ejecutar celdas secuencialmente:**
   - Importación de librerías
   - Carga de datos
   - Análisis exploratorio
   - Visualizaciones
   - Conclusiones

3. **Tiempo estimado:** 15-20 minutos para ejecución completa

4. **Datos:** El notebook incluye generación de datos sintéticos, pero puede adaptarse para usar datos reales

### Personalización

Para usar tus propios datos:

1. Reemplaza la función `cargar_datos()` 
2. Ajusta las columnas según tu dataset
3. Modifica las visualizaciones según necesites

```python
# Ejemplo para cargar datos reales
def cargar_datos():
    return pd.read_csv('ruta/a/tus/datos.csv')
```

## 📊 Métricas Principales del Análisis

| Métrica | Valor |
|---------|-------|
| **Total de Clientes** | 7,043 |
| **Tasa de Churn** | 27.3% |
| **Permanencia Promedio** | 32.4 meses |
| **Cargo Mensual Promedio** | $64.76 |
| **Clientes de Alto Riesgo** | 1,869 (26.5%) |

## 🎯 Principales Recomendaciones

### 1. **Estrategias de Retención**
- Programa de fidelización para primeros 6 meses
- Incentivos para migrar a contratos anuales
- Seguimiento proactivo de clientes de alto riesgo

### 2. **Optimización de Servicios**
- Revisar pricing de fibra óptica
- Bundles atractivos para servicios premium
- Mejora en experiencia de usuario

### 3. **Segmentación de Clientes**
- **Alto Riesgo:** < 6 meses, contrato mensual
- **Estables:** Contratos anuales, múltiples servicios
- **Leales:** > 24 meses, contratos bianuales

## 🛠️ Tecnologías Utilizadas

- **Python 3.9+** - Lenguaje principal
- **Pandas** - Manipulación de datos
- **NumPy** - Operaciones numéricas
- **Matplotlib/Seaborn** - Visualizaciones estáticas
- **Plotly** - Visualizaciones interactivas
- **Jupyter Notebook** - Entorno de desarrollo

## 👨‍💻 Autor

- Enfoque en insights de negocio
- Código modular y reutilizable

