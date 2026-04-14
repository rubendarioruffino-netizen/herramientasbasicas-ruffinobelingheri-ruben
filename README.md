📊 Herramientas Básicas para el Análisis de Datos — Trabajo Final Integrador
Autor: Rubén Darío Ruffino Belingheri  
Curso: Herramientas Básicas para el Análisis de Datos  
Institución: Centro de e-Learning UTN BA  
Repositorio: `herramientasbasicas-ruffinobelingheri-ruben`
---
🎯 Objetivo del Proyecto
Desarrollar un análisis de datos end-to-end sobre un dataset de ventas minoristas, integrando Python (pandas, matplotlib, seaborn), Power BI y GitHub como herramientas principales. El proyecto cubre desde la pregunta analítica inicial hasta la publicación del dashboard interactivo y la documentación del repositorio.
Pregunta principal:
> ¿Cómo evolucionaron las ventas y la rentabilidad por categoría de producto y región entre 2019 y 2022, y qué segmentos de clientes generan mayor margen de ganancia?
---
📁 Estructura del Repositorio
```
herramientasbasicas-ruffinobelingheri-ruben/
│
├── data/
│   └── raw/
│       └── superstore_original.csv       # Dataset fuente original
│
├── notebooks/
│   └── notebook_tp_final.ipynb           # Análisis exploratorio completo (EDA)
│
├── dashboard/
│   ├── dashboard_superstore.pbix         # Archivo Power BI
│   └── capturas/
│       ├── dashboard_ventas.png
│       └── dashboard_kpis.png
│
└── README.md                             # Este archivo
```
---
📦 Dataset
Nombre: Superstore Sales Dataset
Fuente: Kaggle — Superstore Dataset Final
Registros: ~9.994 filas × 21 columnas
Período: 2019–2022
Contenido: Transacciones de ventas de una tienda minorista de EE.UU., con información de categorías, regiones, segmentos de clientes, fechas de pedido y envío, ventas, descuentos y ganancias.
Justificación de elección: El dataset tiene un tamaño adecuado (dentro del rango 10k–2M filas recomendado), incluye variables numéricas, categóricas y temporales que permiten responder preguntas analíticas concretas sobre rentabilidad y tendencias de ventas.
---
🔧 Pasos Realizados
1. Carga e inspección inicial
Se cargó el CSV con `pandas` y se auditaron tipos de datos, valores nulos, duplicados y estadísticas descriptivas.
2. Limpieza y estandarización
Eliminación de filas duplicadas.
Conversión de columnas de fecha a tipo `datetime`.
Creación de columnas derivadas: `Year`, `Month`, `Quarter`, `YearMonth`.
Cálculo de `Profit Margin (%)` como indicador de rentabilidad.
Normalización de texto en columnas categóricas.
Identificación y reporte de outliers mediante método IQR (conservados para el análisis).
3. Exploración y visualización (EDA)
Se construyeron 5 gráficos con interpretación:
Evolución anual de ventas y ganancia (barras + línea doble eje)
Ventas por subcategoría (barras horizontales)
Mapa de calor: margen de ganancia por categoría y segmento
Distribución de ventas por región (torta + barras)
Tendencia mensual de ventas por categoría (líneas)
4. KPIs definidos
KPI	Descripción
Ventas y Ganancia por Año	Total acumulado y margen anual
Margen por Categoría	Ganancia / Ventas × 100 por categoría
Ventas por Región	Participación regional en el total de ventas
5. Dashboard en Power BI
Dashboard interactivo con 4 visualizaciones, 3 KPIs (tarjetas) y 1 panel de filtros por año, región y categoría.
---
🚀 Cómo reproducir el análisis
Clonar este repositorio:
```bash
   git clone https://github.com/tu-usuario/herramientasbasicas-ruffinobelingheri-ruben.git
   ```
Abrir `notebooks/notebook_tp_final.ipynb` en Google Colab o Jupyter.
Ejecutar todas las celdas en orden.
El CSV limpio (`superstore_limpio.csv`) se exporta automáticamente para usar en Power BI.
---
📚 Fuentes y Referencias
Vivek468. (2022). Superstore Dataset Final. Kaggle. https://www.kaggle.com/datasets/vivek468/superstore-dataset-final
McKinney, W. (2022). pandas documentation. https://pandas.pydata.org/docs/
Hunter, J. D. (2007). Matplotlib: A 2D Graphics Environment. https://matplotlib.org/stable/
Waskom, M. (2021). seaborn: statistical data visualization. https://seaborn.pydata.org/
Microsoft. (2024). Power BI Documentation. https://learn.microsoft.com/en-us/power-bi/
UTN BA Centro de e-Learning. (2025). Herramientas Básicas para el Análisis de Datos — Material de cursada.
---
Trabajo realizado en el marco del curso "Herramientas Básicas para el Análisis de Datos" — UTN BA Centro de e-Learning.
