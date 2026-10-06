# CC219 – Aplicaciones de Data Science (2026-2)
## Hito 1 (Trabajo Parcial): Triage Inteligente y Clasificación de Reseñas Móviles

### Integrantes del Grupo
* **Flores Burga, Austin Bryan**
* **Alarcón Castellanos, Ericks Santiago**
* **Flores Mamani, Diego Alejandro**

---

### 1. Objetivo del Trabajo
Diseñar, implementar y evaluar un pipeline integral de Procesamiento de Lenguaje Natural (NLP) y Machine Learning para la ingesta, normalización, análisis exploratorio y clasificación automatizada de opiniones no estructuradas provenientes de aplicaciones móviles, buscando agilizar el triage operativo y reducir la latencia de respuesta frente a incidencias críticas.

---

### 2. Descripción del Dataset
* **Nombre:** Multilingual Mobile App Review Dataset Sept 2025 (Kaggle).
* **Volumen:** 2,514 observaciones y 15 variables tabulares/textuales.
* **Muestra depurada:** 2,418 registros válidos tras la remoción de valores faltantes.
* **Variables clave:**
  * `review_text`: Cuerpo no estructurado en lenguaje natural con la opinión del usuario.
  * `rating`: Puntuación numérica continua de 1.0 a 5.0 otorgada por el usuario.
  * `app_name`: Nombre de la aplicación evaluada (41 aplicaciones representadas).
  * `app_category`: Segmento funcional (18 categorías, ej. Entertainment, Productivity, Games).

---

CC219-TP-TF-2026-2-CC92/

├── data/
│   │
│   ├── multilingual_mobile_app_reviews_2025.csv  # Dataset original
│   │
│   └── reviews_cleaned_nlp.csv                   # Dataset preprocesado tras limpieza NLP
│
├── code/
│   │
│   └── Hito1_EDA_Normalizacion.ipynb             # Notebook reproducible con EDA y Pipeline NLP
│
├── LICENSE
│
└── README.md


---

### 4. Conclusiones y Estado del Hito 1
1. **Calidad y consistencia:** El análisis exploratorio identificó una distribución bimodal centrada en una media de rating de 3.02, validando la viabilidad de clasificar polaridades extremas frente a intermedias.
2. **Normalización NLP:** La sanitización con Regex y la remoción de *stopwords* aisló términos semánticamente determinantes (`features`, `crashes`, `performance`, `support`), sentando las bases léxicas para la vectorización TF-IDF y el modelado con Transformers del Hito 2.
3. **Trabajo a futuro:** Para el Hito Final se entrenarán y contrastarán clasificadores supervisados clásicos frente al ajuste fino (*Fine-Tuning*) de modelos basados en BERT/BETO.

---

### 5. Licencia
Este proyecto se distribuye bajo los términos de la Licencia **MIT**.
