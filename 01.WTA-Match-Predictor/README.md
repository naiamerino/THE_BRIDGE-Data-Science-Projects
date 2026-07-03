# 🤖 WTA Match Predictor

Proyecto de Machine Learning desarrollado durante el bootcamp de Data Science de The Bridge.

El objetivo del proyecto es predecir resultados de partidos del circuito WTA utilizando modelos de clasificación entrenados sobre datos históricos de tenis femenino. Además del predictor de partidos, el proyecto incluye una simulación completa de torneos mediante Monte Carlo y una aplicación interactiva desarrollada con Streamlit.

---

# 📌 Objetivos del proyecto

* Construir un modelo capaz de predecir la ganadora de un partido WTA.
* Superar el baseline basado únicamente en el ranking WTA.
* Simular torneos completos utilizando probabilidades generadas por el modelo.
* Desplegar una aplicación interactiva para realizar predicciones y simulaciones.

---

# 📊 Dataset

Se utilizaron datos históricos del circuito WTA desde 2007 hasta 2026.

## Fuente principal

Dataset de Kaggle:

* `wta.csv`
* Partidos WTA históricos
* Rankings
* Superficie
* Rondas
* Cuotas de apuestas
* Resultados

## Fuente secundaria

Dataset de Jeff Sackmann con estadísticas avanzadas de servicio:

* aces
* dobles faltas
* porcentaje de primer servicio
* break points
* estadísticas avanzadas de partido

---

# 🧠 Tecnologías utilizadas

* Python 🐍
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Streamlit
* Matplotlib
* Seaborn

---

# ⚙️ Conceptos trabajados

* Limpieza y transformación de datos
* Feature Engineering
* Ratings ELO
* Clasificación supervisada
* Random Forest
* XGBoost
* Pipelines de Scikit-learn
* OneHotEncoder y StandardScaler
* Validación temporal train/test
* Simulación Monte Carlo
* Desarrollo de aplicaciones con Streamlit

---

# 🏗️ Estructura del proyecto

```bash
03.Machine-Learning/
│
src/
├── data/
│   ├── wta.csv
│   ├── wta_limpio.csv
│   └── historico_partidos.csv
├── model/
│   ├── gbx_red.model
│   ├── gbx_v3.model
│   └── production/
│       └── gbx_v3.model
├── notebooks/
│   ├── 01_EDA_FeatureEngineering.ipynb
│   ├── 02_Modelo_ML.ipynb
│   └── 03_SimulacionTorneo.ipynb
├── utils/
│   └── features.py
├── app.py
├── memoria.ipynb
└── README.md
```

---

# 🤖 Modelos entrenados

Durante el proyecto se entrenaron distintos modelos de clasificación:

* Random Forest
* XGBoost
* Voting Classifier

El modelo final seleccionado fue **XGBoost**, por ofrecer el mejor equilibrio entre accuracy y AUC-ROC.

---

# 🎾 Simulación de torneos

El proyecto incluye un simulador de torneos basado en Monte Carlo.

A partir de un cuadro real de competición:

1. Se generan las probabilidades de cada partido.
2. Se simulan miles de torneos.
3. Se calcula la probabilidad de victoria de cada jugadora.

La simulación fue aplicada sobre Roland Garros 2026.

---

# 💻 Aplicación Streamlit

La aplicación desarrollada permite:

✅ Predecir partidos individuales  
✅ Simular torneos completos  
✅ Visualizar probabilidades de victoria  
✅ Ejecutar simulaciones Monte Carlo  

---

# 🚀 Ejecución del proyecto

El proyecto fue desarrollado en Python utilizando notebooks de Jupyter y Streamlit.

Para ejecutar la aplicación es necesario disponer de las librerías indicadas en los notebooks y ejecutar:

```bash
streamlit run src/app.py

---

# 📚 Aprendizajes

Este proyecto permitió trabajar un flujo completo de Machine Learning:

* Obtención y limpieza de datos
* Construcción de variables predictivas
* Entrenamiento y evaluación de modelos
* Prevención de data leakage
* Simulación probabilística
* Desarrollo y despliegue de aplicaciones interactivas

---

# 📌 Estado del proyecto

✅ Proyecto finalizado

🚧 Posibles mejoras futuras:

* Incorporar estadísticas avanzadas de juego
* Mejorar calibración de probabilidades
* Optimizar tiempos de simulación
* Automatizar actualización de cuadros de torneos

---

# 👩‍💻 Autor

Naia Merino
Bootcamp Data Science — The Bridge
