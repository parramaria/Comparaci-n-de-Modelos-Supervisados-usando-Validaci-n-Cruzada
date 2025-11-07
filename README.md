# Comparación de Modelos Supervisados usando-Validación Cruzada
Trabajo N°2
## Autor: Maria Paula Sánchez parra


Este proyecto tiene como objetivo evaluar y comparar distintos modelos de aprendizaje supervisado utilizando Python y la librería scikit-learn.
El propósito principal es predecir el riesgo crediticio (alto o bajo) de un cliente, a partir de sus características financieras y demográficas.

## Contenido del Repositorio

-Evaluating_supervised_models.ipynb → Cuaderno principal con todo el flujo de análisis, modelado y evaluación.

-credit_customers.csv → Conjunto de datos utilizado (no incluido, asegúrate de tenerlo en el mismo directorio antes de ejecutar el notebook).

## Conjunto de Datos

-El dataset contiene información detallada sobre clientes de crédito, incluyendo variables como:

-Estado de cuenta corriente y de ahorros

-Historial crediticio

-Monto del crédito solicitado

-Edad, tipo de empleo, tipo de vivienda, entre otros

-La variable objetivo (class) clasifica a los clientes como de buen o mal riesgo crediticio.

 ## Metodología

El flujo de trabajo se estructura en las siguientes etapas:

**1. Análisis Exploratorio de Datos (EDA)**

-Revisión de estructura, tipos de datos y valores faltantes.

-Análisis de distribución de variables y correlaciones relevantes.

**2. Preprocesamiento**

-Codificación de variables categóricas mediante OneHotEncoder.

-Escalado de variables numéricas con StandardScaler.

-División en conjuntos de entrenamiento y prueba (train_test_split).

**3. Modelado**

-Se implementan y comparan distintos algoritmos supervisados:

-Regresión Logística

-Árbol de Decisión

-Bosque Aleatorio (Random Forest)

-K-Vecinos más Cercanos (KNN)

**4. Evaluación**

-Cada modelo fue evaluado mediante métricas clave:

-Exactitud (Accuracy)

-Matriz de confusión

-Informe de clasificación (Precision, Recall, F1)

-Curva ROC y AUC

## Resultados

A continuación, se presentan los principales resultados obtenidos tras la comparación de modelos:

| Modelo                  | Precisión (Entrenamiento / Prueba) | Puntuación F1 (Prueba) | Precisión del CV |
| ----------------------- | ---------------------------------- | ---------------------- | ---------------- |
| **KNN**                 | 0.804 / 0.736                      | 0.718                  | 0.711            |
| **Regresión Logística** | 0.780 / 0.772                      | 0.763                  | 0.733            |
| **Árbol de Decisión**   | 0.751 / 0.720                      | 0.719                  | 0.667            |


El análisis mostró que la Regresión Logística ofrece el mejor equilibrio entre precisión, interpretabilidad y generalización, mientras que los modelos basados en árboles son útiles para explorar relaciones no lineales, aunque presentan mayor sobreajuste.

## Conclusiones

-La correcta preparación de datos y el uso de métricas variadas permiten una evaluación integral del desempeño de los modelos.

-La Regresión Logística destaca como modelo base por su estabilidad, mientras que los modelos de conjunto (ensemble) como Random Forest podrían optimizarse en futuras versiones.

-Este enfoque puede ampliarse incorporando técnicas de selección de características, optimización de hiperparámetros y validación cruzada avanzada.
