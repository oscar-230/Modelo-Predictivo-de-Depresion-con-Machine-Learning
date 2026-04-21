# 🧠 Proyecto de Machine Learning: Predicción de Depresión

---

## 🎓 Información Académica

- **Universidad:** Universidad del Valle  
- **Escuela:** Escuela de Ingeniería de Sistemas y Computación  
- **Asignatura:** Inteligencia Artificial  
- **Tipo de trabajo:** Informe sobre Machine Learning  
- **Estudiante:** Oscar David Cuaical 

---

## 📌 Descripción del Proyecto

Para la experimentación con técnicas de **Machine Learning**, se utilizó un conjunto de datos de **27,901 estudiantes** que participaron en un estudio sobre depresión.

Dentro de la información recolectada se incluyen datos relacionados con:

- Estilo de vida  
- Hábitos académicos o laborales  
- Salud mental  

Cada individuo está descrito mediante **9 atributos**, y el objetivo es predecir la variable:

> 🎯 **Depression (0 o 1)**  
> - `0`: No presenta depresión  
> - `1`: Presenta síntomas de depresión  

---

## 📊 Descripción del Dataset

### 🧾 Tabla de atributos

| # | Atributo | Descripción | Tipo de variable | Posibles valores |
|--|----------|------------|------------------|------------------|
| 1 | Gender | Sexo de la persona | Categórica | Female, Male |
| 2 | Age | Edad de la persona en años | Numérica | 18.0 - 59.0 |
| 3 | CGPA | Promedio acumulado (Cumulative Grade Point Average) | Numérica | 0.0 - 10.0 |
| 4 | Sleep Duration | Duración habitual del sueño por noche | Categórica | Less than 5 hours, 5-6 hours, 7-8 hours, More than 8 hours, Others |
| 5 | Degree | Nivel educativo actual | Categórica | High school, Undergraduate, Postgraduate, Doctorate, Others |
| 6 | Suicidal Thoughts | Presencia de pensamientos suicidas | Categórica | No, Yes |
| 7 | Work/Study Hours | Horas dedicadas a estudio o trabajo por día | Numérica | 0.0 - 12.0 |
| 8 | Family History of Mental Illness | Antecedentes familiares | Categórica | No, Yes |
| 9 | Depression | Variable objetivo | Binaria | 0 = No, 1 = Sí |

---

## ⚙️ Metodología General

Se desarrollaron **dos notebooks**, cada uno aplicando diferentes técnicas de Machine Learning:

- 🤖 Redes Neuronales
- 🌳 Árboles de Decisión

En ambos casos se realizaron:

- División de datos (80% entrenamiento / 20% prueba)
- Normalización de variables numéricas
- Codificación de variables categóricas

---

# 🤖 PARTE 1: Redes Neuronales

## 📌 Objetivo

Construir y evaluar múltiples modelos de redes neuronales variando su arquitectura e hiperparámetros.

---

## 🔹 Procedimiento

Se realizaron las siguientes tareas:

1. Lectura del dataset  
2. División en entrenamiento y prueba  
3. Preprocesamiento de datos  
4. Construcción de 5 modelos con diferentes configuraciones  
5. Evaluación mediante accuracy  
6. Selección del mejor modelo  
7. Ajuste de hiperparámetro adicional (`alpha`)  

---

## 📊 Resultados

### Modelos evaluados

| Modelo | Arquitectura | Accuracy |
|--------|-------------|----------|
| Modelo 1 | (50) | 0.779789 |
| Modelo 2 | (100, 50) | 0.730693 |
| Modelo 3 | (100, 100) | 0.780326 |
| Modelo 4 | (150, 100, 50) | 0.707221 |
| Modelo 5 | (200) | 0.760079 |

---

### Ajuste de hiperparámetro (alpha)

| Configuración | Accuracy |
|--------------|----------|
| Original | 0.780326 |
| alpha = 0.01 | 0.752732 |
| alpha = 0.1 | **0.781939** |

---

## ✅ Conclusión PARTE 1

- El mejor modelo fue:  
  👉 **Modelo 3 con alpha = 0.1**

- Accuracy máximo: **0.781939**

📌 El ajuste del hiperparámetro `alpha` permitió mejorar ligeramente el rendimiento, mostrando la importancia de la regularización.

---

# 🌳 PARTE 2: Árboles de Decisión

## 📌 Objetivo

Evaluar el desempeño de árboles de decisión variando la profundidad del modelo y el criterio de división.

---

## 🔹 Procedimiento

Se realizaron las siguientes tareas:

1. Lectura del dataset  
2. División de datos (80/20)  
3. Preprocesamiento  
4. Entrenamiento con `criterion = gini` variando `max_depth`  
5. Evaluación de resultados  
6. Repetición con `criterion = entropy`  
7. Comparación de resultados  
8. Selección del mejor modelo  
9. Evaluación de hiperparámetro adicional (`min_samples_split`)  

---

## 📊 Resultados

### Mejor modelo con Gini

- `max_depth = 6`
- Accuracy: **0.782297**

### Mejor modelo con Entropy

- `max_depth = 6`
- Accuracy: **0.781580**

---

### Evaluación de hiperparámetro adicional

| min_samples_split | Accuracy |
|-------------------|----------|
| 2 | 0.782297 |
| 10 | 0.782297 |
| 20 | 0.782297 |

---

## ✅ Conclusión PARTE 2

- El mejor modelo corresponde a:  
  👉 **Árbol de decisión con Gini y max_depth = 6**

- No se observaron mejoras al modificar `min_samples_split`

📌 El modelo alcanza su mejor desempeño en una profundidad intermedia, evitando tanto el subajuste como el sobreajuste.

---

# 🏆 Conclusión General del Proyecto

- Los **árboles de decisión** superaron ligeramente a las redes neuronales  
- El mejor modelo global fue:  

👉 **Decision Tree (Gini, depth = 6)**  
👉 Accuracy: **0.782297**

- La mejora mediante ajuste de hiperparámetros fue limitada  
- El equilibrio entre complejidad y generalización es clave  

---

## 🛠️ Tecnologías Utilizadas

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Scikit-learn  

---
