# sprint7-final-project
# sprint7-final-project
## Objetivo del Proyecto
Este proyecto tiene como objetivo realizar un **análisis integral de la base de clientes de ConnectaTel**, una empresa de telecomunicaciones, para optimizar su estrategia comercial y mejorar la satisfacción del cliente.

### Objetivos Específicos:
- **Analizar el comportamiento de uso** de los clientes actuales (llamadas y mensajes)
- **Identificar patrones de consumo** por grupo demográfico y tipo de plan
- **Segmentar la base de clientes** en grupos estratégicos para personalizar ofertas
- **Evaluar la efectividad** de los planes actuales (Básico y Premium)
- **Generar recomendaciones** para nuevos planes y mejoras en la oferta existente

### Valor de Negocio:
El análisis permitirá a ConnectaTel tomar decisiones basadas en datos para:
- Reducir la rotación de clientes (churn)
- Aumentar la satisfacción del cliente
- Optimizar la estructura de precios
- Identificar oportunidades de crecimiento

## Datasets Utilizados
### Dataset Principal: `connecta_tel_data.csv`
**Descripción:** Base de datos de clientes de ConnectaTel con información demográfica y de uso.

**Estructura del Dataset:**
- **Registros:** 1,000 clientes únicos
- **Período:** Datos de uso mensual actual
- **Fuente:** Sistema interno de facturación de ConnectaTel

**Variables Incluidas:**
| Variable | Tipo | Descripción |
|----------|------|-------------|
| `user_id` | Entero | Identificador único del cliente |
| `age` | Entero | Edad del cliente (años) |
| `plan` | Categórica | Tipo de plan (Básico/Premium) |
| `monthly_charges` | Numérica | Cargo mensual en pesos |
| `calls_made` | Entero | Número de llamadas realizadas en el mes |
| `messages_sent` | Entero | Número de mensajes enviados en el mes |

**Calidad de los Datos:**
- Sin valores faltantes (missing values)
- Datos validados y limpios
- Rango de edades: 18-80 años
- Distribución equilibrada entre planes

## Etapas del Análisis Realizadas
### 1. Exploración y Preparación de Datos
- Carga del dataset y verificación de estructura
- Análisis de tipos de datos y valores faltantes
- Estadísticas descriptivas básicas
- Identificación de outliers y valores atípicos

### 2. Análisis Estadístico Descriptivo
- 2.1 Distribución de variables numéricas (edad, cargos, uso)
- 2.2 Análisis de variables categóricas (distribución por planes)
- 2.3 Correlaciones entre variables
- 2.4 Identificación de patrones de comportamiento

### 3. Segmentación de Clientes
- 3.1 Creación de segmentos por nivel de uso:
  - Alto uso (>10 llamadas y >10 mensajes)
  - Uso medio (5-10 llamadas o mensajes)
  - Bajo uso (<5 llamadas y <5 mensajes)
- 3.2 Segmentación demográfica por edad:
  - Jóvenes (<30 años)
  - Adultos (30-60 años)
  - Adultos mayores (>60 años)

### 4. Análisis Comparativo por Planes
- Comparación de uso entre plan Básico vs Premium
- Análisis de satisfacción por segmento
- Identificación de oportunidades y recomendaciones

## Cómo Ejecutar el Notebook
### Opción 1: Google Colab (Recomendado)
1. Haz clic en el siguiente enlace para abrir el notebook en Google Colab:
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/tu-usuario/tu-repositorio/blob/main/nombre-del-notebook.ipynb)
2. Una vez abierto, ve a `Archivo > Guardar una copia en Drive` para crear tu propia versión
3. Ejecuta las celdas secuencialmente usando `Shift + Enter` o el botón ▶️

### Opción 2: Jupyter Notebook Local
1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu-usuario/tu-repositorio.git

Instala las dependencias:
bash
pip install pandas numpy matplotlib seaborn
Abre Jupyter Notebook:
bash
jupyter notebook
Navega al archivo nombre-del-notebook.ipynb y ábrelo
```
📋 Guía de Reproducción
## Guía de Reproducción

### Requisitos Previos
- Python 3.7 o superior
- Librerías: pandas, numpy, matplotlib, seaborn

### Pasos para Reproducir el Análisis

1. **Preparación de Datos**
   - El dataset `connecta_tel_data.csv` debe estar en la misma carpeta que el notebook
   - Verificar que el archivo contenga las columnas: user_id, age, plan, monthly_charges, calls_made, messages_sent

2. **Ejecución Secuencial**
   - Ejecutar las celdas en orden desde la primera hasta la última
   - **No saltar celdas** ya que cada una depende de las anteriores
   - Tiempo estimado de ejecución: 5-10 minutos

3. **Secciones del Análisis**
   - **Sección 1**: Carga y exploración inicial de datos
   - **Sección 2**: Análisis estadístico descriptivo
   - **Sección 3**: Segmentación de clientes
   - **Sección 4**: Visualizaciones y conclusiones

4. **Verificación de Resultados**
   - Al final del notebook encontrarás un resumen ejecutivo
   - Los gráficos deben mostrarse correctamente
   - Las tablas de segmentación deben contener datos coherentes

### Solución de Problemas Comunes
- Si hay errores de importación: verificar que todas las librerías estén instaladas
- Si no se muestran los gráficos: ejecutar `%matplotlib inline` al inicio
- Si hay errores de archivo: verificar la ruta del dataset
