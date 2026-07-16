# 📱 Análisis Exploratorio del Modelo Comercial de Celulares

> **Diploma Data Analyst — DMC Institute**  
> Módulo: Friendly SQL & Python para Analytics

---

## 📋 Descripción del dataset

El dataset `ModeloComercial.xlsx` contiene **1,499 facturas de venta** de una empresa distribuidora de smartphones, registradas entre **2014 y 2020**. Está compuesto por 8 hojas relacionadas:

| Hoja | Descripción | Filas |
|---|---|---|
| Ventas | Tabla de hechos principal | 1,499 |
| Tienda | 7 puntos de venta retail | 7 |
| Vendedor | Equipo comercial | 5 |
| Cliente | Corporaciones distribuidoras | 10 |
| País | Mercados internacionales | 24 |
| Modelo | Catálogo de smartphones | 29 |
| Marca | Marcas comercializadas | 6 |
| Operador | Aliados de telecomunicaciones | 5 |

**Fuente:** Dataset propio del curso (ModeloComercial.xlsx)

---

## 🎯 Objetivo del análisis

Identificar patrones de rentabilidad, desempeño por tienda, tendencias de venta y riesgo de cobranza mediante análisis exploratorio de datos (EDA), visualizaciones interactivas y consultas SQL.

---

## 🔍 Etapas del análisis

1. **Carga del dataset** — lectura con `pandas`, merge de 8 tablas, variables derivadas
2. **Exploración inicial** — `info()`, `shape`, `head()`, `tail()`, tipos de datos
3. **Calidad de datos** — nulos, duplicados, inconsistencias de precios
4. **Estadística descriptiva** — variables numéricas y categóricas, KPIs generales
5. **Visualizaciones con Plotly** — 6 gráficos interactivos (barras, línea, dona, boxplot, histograma, scatter)
6. **Consultas SQL con DuckDB** — 6 consultas (SELECT/LIMIT, WHERE, GROUP BY, ORDER BY, CTE + LAG)
7. **Hallazgos y conclusiones** — insights accionables para el negocio

---

## 🛠️ Tecnologías utilizadas

![Python](https://img.shields.io/badge/Python-3.10-blue)
![pandas](https://img.shields.io/badge/pandas-2.x-green)
![numpy](https://img.shields.io/badge/numpy-1.x-orange)
![DuckDB](https://img.shields.io/badge/DuckDB-latest-yellow)
![Plotly](https://img.shields.io/badge/Plotly-5.x-purple)

---

## 📁 Estructura del repositorio

```
📦 modelo-comercial-celulares/
├── 📓 notebook_analisis_sql_python.ipynb   ← Notebook principal
├── 📊 ModeloComercial.xlsx                 ← Dataset fuente
├── 📄 README.md                            ← Este archivo
└── 📋 requirements.txt                     ← Dependencias
```

---

## ▶️ Cómo ejecutar el notebook

### Opción A — Google Colab (recomendado)
1. Subir `ModeloComercial.xlsx` a Google Drive
2. Abrir el notebook en Colab
3. Descomentar la celda de instalación: `!pip install duckdb plotly openpyxl -q`
4. Ajustar la ruta del archivo y ejecutar todas las celdas

### Opción B — Local
```bash
# Clonar repositorio
git clone https://github.com/TU_USUARIO/modelo-comercial-celulares.git
cd modelo-comercial-celulares

# Instalar dependencias
pip install -r requirements.txt

# Abrir el notebook
jupyter notebook notebook_analisis_sql_python.ipynb
```

---

## 💡 Principales hallazgos

- **Tottus y Oeschle** concentran el **55%** de las ventas totales (S/21.2M)
- Las ventas cayeron un **53%** entre 2017 y 2020 — señal de alerta estratégica
- El **margen global es 5.55%** — Oeschle tiene margen inferior a pesar de su alto volumen
- **María** lidera ventas individuales con S/13.4M (35% del total del equipo)
- La cobranza es mayormente saludable — solo 3 de 10 clientes presentan retrasos

---

## 📦 Dependencias (requirements.txt)

```
pandas>=1.5.0
numpy>=1.23.0
duckdb>=0.9.0
plotly>=5.15.0
openpyxl>=3.1.0
jupyter>=1.0.0
```
