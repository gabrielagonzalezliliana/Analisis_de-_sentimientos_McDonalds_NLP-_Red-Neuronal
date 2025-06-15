# 🧠 Análisis de Sentimientos - NLP y Red Neuronal

Este proyecto analiza las opiniones de clientes de McDonald's a través de técnicas de Procesamiento de Lenguaje Natural (NLP) y modelos de machine learning, incluyendo una red neuronal, para clasificar el sentimiento de las reseñas como positivas o negativas.

---

## 🎯 Objetivo del proyecto

Aplicar técnicas de NLP y algoritmos de clasificación para:

- Clasificar comentarios como **positivos o negativos**
- Identificar **patrones lingüísticos frecuentes**
- Evaluar **polaridad y subjetividad** emocional
- Comparar el rendimiento entre un modelo tradicional (Naive Bayes) y una red neuronal

En un contexto donde la percepción del cliente impacta en la reputación de marca, este análisis ayuda a detectar oportunidades de mejora en la experiencia del consumidor.

---

## 🔗 Acceso al proyecto en Google Colab

Haz clic para ver y ejecutar el notebook:  
👉 [Abrir en Colab](https://colab.research.google.com/drive/1mENMX4ck2LnXJXUIdJz7MEoFZSy7rOKW?usp=sharing)


---

## 🗃️ Dataset

- Fuente: Reseñas públicas de clientes en locales de McDonald's
- Variables clave: `review`, `rating`

---

## 🔧 Herramientas y tecnologías

- **Python**
- **Pandas**, **Seaborn**, **Matplotlib**
- **spaCy**, **NLTK**, **TextBlob**
- **TensorFlow / Keras**
- **WordCloud**, **LDA**

---

## 🔍 Pipeline del proyecto

### 1. Carga y exploración del dataset
- Análisis de la distribución de ratings
- Observación de polarización (5★ y 1★ predominantes)

### 2. Preprocesamiento de texto
- Limpieza profunda: URLs, puntuación, emojis, etc.
- Tokenización, Stopwords, Lematización, Stemming

### 3. Visualización de texto
- Nube de palabras
- Gráfico de palabras más frecuentes
- Distribución de polaridad y subjetividad

### 4. Modelado de temas (LDA)
- Extracción de 5 temas clave presentes en las reseñas

### 5. Análisis de polaridad y subjetividad
- Categorización: Positivo / Neutral / Negativo
- Subjetividad: Baja / Media / Alta

---

## 🤖 Modelos implementados

### 🔹 Clasificador Naive Bayes (TF-IDF)

- Accuracy: **85.2%**
- Clasificación binaria: `rating > 3` → positivo

```python
Accuracy: 0.852

### 🤖 Red Neuronal (Keras)

Se implementó una red neuronal simple utilizando Keras para clasificar las reseñas en sentimientos positivos o negativos, con entrada basada en TF-IDF.

#### 📐 Arquitectura

```python
model = Sequential([
    Dense(64, input_shape=(X_array.shape[1],), activation='relu'),
    Dropout(0.5),
    Dense(1, activation='sigmoid')
])

```precision alcanzada
Accuracy: 0.8763



