# 💳 Credit Card Fraud Detection Project

## 📌 Descripción

Este proyecto tiene como objetivo detectar transacciones fraudulentas utilizando técnicas de análisis exploratorio, modelado supervisado, visualización interactiva en Power BI y análisis avanzado con reducción de dimensionalidad. El conjunto de datos altamente desbalanceado representa un caso realista del problema de fraude con tarjetas de crédito.

## 📂 Estructura del Proyecto

```
├── data/
│   └── creditcard.csv
├── dashboard/
│   └── dashboard_data.csv
├── outputs/
│   └── dimensionality_reduction_clusters.png
├── notebooks/
│   ├── 1_exploratory_analysis.ipynb
│   ├── 2_modeling.ipynb
│   └── 3_visual_clustering.ipynb
├── dashboard.pbix
└── README.md
```

## 🧪 Dataset

- Fuente: [Kaggle - Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)
- Observaciones: 284,807
- Variables: 30 características anónimas (`V1` a `V28`), `Time`, `Amount`, `Class` (0 = normal, 1 = fraude)

## 🧭 Flujo del Proyecto

### 1. 🔍 Análisis Exploratorio (EDA)

- Análisis de la distribución de clases: solo el 0.17% son fraudes.
- Identificación de variables con mayor correlación con la clase (`V14`, `V12`, `V10`, `V17`).
- Visualización de outliers mediante boxplots.
- Análisis del comportamiento del monto (`Amount`) y tiempo (`Time`).

### 2. 🧠 Modelado Supervisado

- Se entrenaron dos modelos:
  - Árbol de Decisión
  - Random Forest
- Métricas obtenidas:
  | Modelo         | Accuracy | Recall (fraude) | F1-Score (fraude) |
  |----------------|----------|------------------|-------------------|
  | Decision Tree  | 99.93%   | 79.7%            | 79.7%             |
  | Random Forest  | 99.95%   | 76.3%            | 83.3%             |

### 3. 📊 Dashboard Interactivo en Power BI

- KPIs: total de transacciones, total de fraudes, % de fraudes.
- Gráficos:
  - Distribución de clases (Normal vs Fraude)
  - Boxplot de montos (`Amount`)
  - Histograma de `V14` con escala logarítmica

### 4. 🔬 Análisis Avanzado – Clustering con Reducción de Dimensionalidad

- Aplicación de técnicas:
  - **PCA**
  - **Truncated SVD**
  - **t-SNE**
- Visualización de clusters usando scatter plots.
- Se observó que **t-SNE** permite distinguir mejor las transacciones fraudulentas de las normales.

![clusters](./outputs/charts/cluster_reduction_plot.png)

## 🧰 Herramientas y Tecnologías

- Python (pandas, scikit-learn, matplotlib, seaborn)
- Power BI
- Jupyter Notebook
- Git y GitHub

## 📈 Próximos pasos

- Aplicar técnicas de balanceo de clases como **SMOTE**.
- Probar modelos avanzados: **XGBoost**, **LightGBM**, etc.
- Hacer tuning de hiperparámetros.
- Desplegar una demo web o API (Streamlit, Flask).

## 👨‍💻 Autor

**Kevin Malca**  
[LinkedIn](https://www.linkedin.com/in/kevinmalca) • [GitHub](https://github.com/xKevO)  
**Analista de Datos | SQL • Power BI • Python • AWS en formación**
