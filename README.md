# PYTHON_PySpark_ApacheSpark

Este repositorio contiene proyectos desarrollados en Python que permiten practicar la gestión y análisis de datos con Apache Spark, utilizando Jupyter Notebooks en Google Colab como entorno interactivo.

# 📘 Contenido del Repositorio

El repositorio incluye **cuatro** notebooks diseñados de forma pedagógica para introducir progresivamente conceptos clave del ecosistema Apache Spark:

## 1️⃣ [Apache Spark RDD.ipynb]

**Conexión a Apache Spark y trabajo con RDDs**

Este notebook explica:

- Cómo inicializar una sesión de Spark (`SparkSession`) en Google Colab.
- Cómo cargar datos desde un archivo CSV.
- Cómo asignar los datos a un RDD (*Resilient Distributed Dataset*).
- Casos de uso simples para entender el procesamiento distribuido basado en RDDs.

🎯 Ideal para quienes están comenzando con PySpark y desean comprender el enfoque más básico de procesamiento de datos.

---

## 2️⃣ [Apache Spark DF SQL.ipynb]

**Spark SQL, DataFrames y Motores de Optimización**

Este notebook avanza hacia un enfoque más estructurado con:

- Configuración de `SparkSession`.
- Carga de datos desde CSV directamente en un `DataFrame`.
- Uso de consultas SQL sobre DataFrames con `spark.sql()`.
- Creación de funciones en Python registradas como UDFs (*User Defined Functions*) en el contexto SQL.
- Explicación de los motores de optimización internos de Apache Spark:
  - 🔍 **Catalyst:** optimización lógica y reescritura de planes de ejecución SQL.
  - ⚙️ **Tungsten:** mejoras físicas a nivel de memoria y ejecución.

🎯 Este segundo notebook es ideal para quienes desean avanzar en el uso eficiente de Spark SQL y comprender cómo Spark optimiza sus operaciones internas.

---

## 3️⃣ [Apache Spark Streaming.ipynb]

**Simulación de procesamiento en tiempo real con Spark Structured Streaming**

Este notebook introduce el procesamiento de flujos de datos simulados utilizando Apache Spark Streaming en Google Colab, ideal para comprender cómo funciona el modelo de *micro-batches* en contextos reales.

En este proyecto aprenderás a:

- ⚙️ Configurar un entorno Spark Streaming desde cero en Google Colab.
- 📁 Simular la llegada de datos en tiempo real usando archivos CSV copiados como micro-lotes.
- 🧱 Definir esquemas estructurados (`StructType`) para la lectura de datos en modo `readStream`.
- 📊 Aplicar transformaciones en tiempo real como `groupBy` y `count` sobre flujos continuos.
- 🖨️ Utilizar `foreachBatch` para imprimir resultados procesados por cada micro-batch.
- 🧠 Comprender conceptos clave como:
  - 📦 **Micro-batch:** pequeñas porciones de datos procesadas a intervalos definidos.
  - 📝 **Checkpoint:** carpeta donde Spark guarda el estado de ejecución para tolerancia a fallos.
  - 🔄 **Diferencias entre batch y streaming:** ejecución tradicional vs. flujo continuo.

🎯 Este tercer notebook es especialmente útil para quienes desean iniciarse en el **procesamiento de datos en tiempo real** de manera progresiva, sin depender de herramientas externas como Kafka o Flink.

---

## 4️⃣ [4 - Apache Spark MLlib.ipynb]

**Aprendizaje automático con Spark MLlib (API DataFrame)**

Introducción práctica al aprendizaje automático con un flujo completo desde el preprocesamiento hasta la evaluación y persistencia del modelo.

En este notebook trabajarás con:

- 🧹 **Preparación de datos para ML**
  - Limpieza básica y tratamiento de valores nulos.
  - Manejo de variables categóricas con `StringIndexer` y `OneHotEncoder`.
  - Ensamble de características con `VectorAssembler`.
  - Escalamiento/normalización con `StandardScaler`.

- 🧱 **Pipelines de ML reproducibles**
  - Creación de un `Pipeline` con *stages* encadenados (indexado → codificación → ensamblado → escalado → estimador).
  - Uso de `PipelineModel` para transformar datos de entrenamiento y prueba de forma consistente.

- 🤖 **Modelos incluidos**
  - **Regresión:** `LinearRegression`, `RandomForestRegressor` (visión general).
  - **Clasificación:** `LogisticRegression`, `RandomForestClassifier`.
  - Interpretación básica: coeficientes y *feature importances*.

- 🧪 **Entrenamiento, validación y evaluación**
  - División `train/test` con semilla fija para reproducibilidad.
  - Métricas con `RegressionEvaluator` (RMSE, R²) y `MulticlassClassificationEvaluator` (accuracy, F1).
  - Visualización de resultados y predicciones con `transform()` y `show(truncate=False)`.

🎯 Este cuarto notebook es ideal para quienes desean **dar el salto del procesamiento de datos al modelado de ML** en Spark, utilizando flujos reproducibles y escalables que siguen las mejores prácticas de la API de MLlib.
