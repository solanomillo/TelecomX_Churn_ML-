# 📊 TelecomX LATAM – Predicción de Cancelación de Clientes (Churn Modeling)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github.com/solanomillo/TelecomX_Churn_ML-/blob/main/TelecomX2_ML.ipynb)
![Python](https://img.shields.io/badge/python-3.x-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/sklearn-latest-orange.svg)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=flat)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat)

### ▶️ Ejecución rápida en Google Colab
1. Haz clic en el badge **Open in Colab** arriba.
2. Ejecuta todas las celdas desde **Runtime → Run all**.
3. Explora el pipeline completo de Machine Learning sin necesidad de instalación local.

---

## 📌 Descripción del Proyecto
Este proyecto desarrolla un modelo predictivo de **Machine Learning** capaz de anticipar qué clientes tienen mayor probabilidad de cancelar el servicio (Churn). 

El enfoque profesional incluyó:
* **Preparación avanzada de datos:** Codificación, normalización y balanceo.
* **Validación robusta:** Cross-validation y comparación de múltiples modelos.
* **Visión de Negocio:** Interpretación de variables y traducción de resultados en decisiones estratégicas.

## 🎯 Objetivos del Proyecto
* Construir modelos de clasificación para optimizar la detección de riesgo.
* Evaluar modelos con métricas de **Precision, Recall y F1-score**.
* **Reducir falsos negativos** (clientes que cancelan sin ser detectados).
* Identificar variables clave e implementar estrategias de retención basadas en datos.

---

## 🧠 Metodología de Trabajo

### 1️⃣ Preparación de Datos
* **Limpieza:** Eliminación de identificadores irrelevantes.
* **Ingeniería de variables:** One-Hot Encoding para categóricas y conversión de la variable objetivo a formato numérico.
* **Balanceo de clases:** Aplicación de técnica **SMOTE** para manejar el desbalance.
* **Escalado:** Normalización para modelos sensibles a la magnitud.

### 2️⃣ Análisis de Correlación
Evaluación de relaciones clave entre:
* **Antigüedad (Tenure)** vs. **Churn**.
* **Cargos mensuales** vs. **Cargos totales**.
* Identificación de patrones críticos de comportamiento.

### 3️⃣ Modelado Predictivo
Se entrenaron y compararon:
* **Regresión Logística:** Para interpretabilidad y análisis de coeficientes.
* **Random Forest:** Para captar relaciones no lineales y jerarquía de variables.

### 4️⃣ Optimización
> 📌 **Decisión clave:** En problemas de churn, priorizamos el **Recall** sobre la Accuracy. Es preferible identificar a un cliente en riesgo (aunque sea un falso positivo) que perder a un cliente real por falta de detección.

---

## 📊 Resultados Finales
El modelo optimizado alcanzó un **Recall del 89%** para la clase Churn.

### Matriz de Confusión
| Métrica | Valor |
| :--- | :--- |
| **Verdaderos Positivos** | 334 |
| **Falsos Negativos** | 40 |
| **Falsos Positivos** | 414 |
| **Verdaderos Negativos** | 621 |

---

## 🔎 Variables Más Influyentes
El análisis de importancia de variables reveló los factores determinantes:

| 🔥 Factores que aumentan el Churn | 🛡️ Factores que reducen el Churn |
| :--- | :--- |
| Cargos Totales (ChargesTotal) | **Antigüedad (Tenure)** |
| Internet por Fibra Óptica | Contratos a largo plazo (1-2 años) |
| Streaming TV / Movies | Soporte Técnico (TechSupport) |
| Facturación electrónica / Cheque | Seguridad Online |

---

## 🚀 Recomendaciones Estratégicas
* **Retención Temprana:** Programas de fidelización en los primeros 3 meses.
* **Incentivos de Permanencia:** Descuentos agresivos para migrar a contratos de largo plazo.
* **Soporte Premium:** Prioridad para usuarios de Fibra Óptica (segmento de alto riesgo).
* **Cross-selling:** Promocionar servicios de seguridad y soporte para aumentar el "engagement".

---

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** Python
* **Análisis de datos:** Pandas, NumPy
* **ML:** Scikit-Learn, Imbalanced-Learn (SMOTE)
* **Visualización:** Matplotlib, Seaborn
* **Entorno:** Google Colab

## 📁 Estructura del Proyecto
```text
TelecomX_Churn_ML/
│
├── TelecomX2_ML.ipynb   # Notebook principal
├── README.md                 # Documentación
├── LICENSE                   # Licencia del proyecto
└── screenshots/              # Capturas de gráficos y resultados
```
