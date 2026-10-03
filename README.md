# Minería de Datos en Spotify Music Dataset: Predicción e Interpretación de Audio Features
https://colab.research.google.com/drive/1LiizKxvbj4vBOxLtx6APX1mtKqm0Kxew#scrollTo=f_pFiGwmGmXU 

## Descripción del Proyecto
Este proyecto aplica la metodología **CRISP-DM** (*Cross-Industry Standard Process for Data Mining*) sobre el dataset de Spotify Music de Kaggle. El objetivo principal es predecir la **popularidad de canciones** mediante algoritmos de Machine Learning supervisado (Random Forest, Decision Tree, Logistic Regression) y realizar un **agrupamiento sonoro (*Mood Clustering*)** no supervisado con $K$-Means.

---

## Principales Resultados

| Modelo | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Logistic Regression** | 81.2% | 62.4% | 48.5% | 0.546 | 0.783 |
| **Decision Tree** | 82.5% | 64.1% | 61.0% | 0.625 | 0.748 |
| **Random Forest** | **88.4%** | **78.2%** | **71.5%** | **0.747** | **0.891** |

* **Mejor Modelo:** Random Forest ($88.4\%$ Accuracy, $0.891$ ROC-AUC).
* **Factor más influyente:** Presencia en Playlists (`in_spotify_playlists`), seguido por `danceability` y `energy`.
* **Clustereado $K$-Means ($K=4$):** Separación exitosa entre temas *High Energy/Party*, *Acoustic/Calm*, *Melancholic/Mood* y *Urban/Speech-Heavy*.

---

## Estructura del Repositorio


│__ Spotify_Data_Mining.ipynb    # interactivo ejecutado en Google Colab
├── requirements.txt                 # Dependencias del proyecto
└── README.md                        # Documentación principal
