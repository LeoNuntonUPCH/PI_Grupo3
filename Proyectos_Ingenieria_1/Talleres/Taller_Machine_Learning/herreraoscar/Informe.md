Este informe se desarrolla siguiendo la estructura propuesta en la guía del curso :contentReference[oaicite:0]{index=0}, incluyendo...

## Introducción

El análisis de la calidad del aire es un tema relevante en el ámbito de la ingeniería, ya que permite comprender el impacto de los contaminantes en el ambiente y en la salud pública. En este contexto, se utilizó información proporcionada por la Agencia de Protección Ambiental de los Estados Unidos (EPA), específicamente datos relacionados con la concentración de dióxido de nitrógeno (NO₂).

El objetivo principal de este trabajo es aplicar técnicas de regresión para modelar y predecir la concentración diaria máxima de NO₂ a partir de variables temporales y geográficas. Para ello, se emplearon datos correspondientes a distintos años, lo que permite observar patrones y comportamientos en el tiempo.

Este informe se desarrolla siguiendo la estructura propuesta en la guía del curso :contentReference[oaicite:0]{index=0}, incluyendo la descripción de la metodología, los resultados obtenidos y una breve discusión de los mismos.

---

## Metodología

### Obtención de datos

Los datos fueron obtenidos desde el portal oficial de la EPA, en la sección de calidad del aire. Se descargaron archivos en formato CSV correspondientes a mediciones diarias de NO₂ para diferentes años.

Posteriormente, los datasets fueron cargados utilizando la librería `pandas` y combinados en un solo DataFrame para facilitar su procesamiento.

### Preprocesamiento

Se realizó un proceso de limpieza y preparación de los datos, incluyendo:

- Unión de datasets de distintos años.
- Selección de la variable objetivo:
  - **Daily Max 1-hour NO2 Concentration**
- Construcción de variables predictoras, tales como:
  - Año, mes y día de la semana.
  - Día del año.
  - Coordenadas geográficas (latitud y longitud).
  - Variables rezagadas (valores de NO₂ de días anteriores).

Además, se aplicaron transformaciones mediante un pipeline que incluye:

- Codificación de variables categóricas (One-Hot Encoding).
- Escalamiento de variables numéricas.

### Modelos utilizados

Se implementaron dos enfoques principales de regresión:

#### 1. Modelo base (Regresión)

Se entrenó un modelo de regresión utilizando un conjunto de entrenamiento (80%) y se evaluó con un conjunto de prueba (20%).

#### 2. Random Forest Regressor

Se utilizó un modelo más robusto basado en ensambles:

- `RandomForestRegressor`
- Parámetros principales:
  - `n_estimators = 200`
  - `max_depth = 10`

Este modelo fue integrado dentro de un pipeline que incluye el preprocesamiento de datos.

### Evaluación del modelo

El desempeño se evaluó mediante:

- Gráfico de valores reales vs predichos.
- Análisis de residuos.
- Métrica RMSE (Root Mean Squared Error).

---

## Resultados

Los resultados muestran que el modelo logra capturar de manera aceptable la relación entre las variables predictoras y la concentración de NO₂.

### Predicciones vs valores reales

Se generó un gráfico de dispersión comparando los valores reales con las predicciones del modelo. En este gráfico se observa que:

- Existe una tendencia positiva clara.
- Los puntos se concentran alrededor de la línea diagonal, lo que indica buen ajuste.

### Error del modelo

Se calculó el RMSE como métrica principal de error:

- El valor obtenido indica que el modelo tiene un margen de error moderado, lo cual es razonable considerando la variabilidad de los datos ambientales.

### Análisis de residuos

El gráfico de residuos muestra que:

- No existe un patrón claramente definido.
- Los errores se distribuyen alrededor de cero.

Esto sugiere que el modelo no presenta sesgos evidentes y que las predicciones son relativamente consistentes.

### Modelo Random Forest

El modelo basado en Random Forest mostró un mejor desempeño en comparación con el modelo base, debido a:

- Su capacidad para capturar relaciones no lineales.
- Mayor robustez frente a variabilidad en los datos.

---

## Discusión

Los resultados obtenidos permiten afirmar que las técnicas de regresión son útiles para modelar la concentración de contaminantes atmosféricos como el NO₂. Sin embargo, existen algunos aspectos a considerar:

- Los datos presentan variabilidad inherente debido a factores externos (clima, tráfico, etc.) que no fueron incluidos en el modelo.
- La inclusión de variables adicionales podría mejorar el desempeño, como condiciones meteorológicas.
- El uso de modelos más complejos, como Random Forest, mejora la precisión, pero también incrementa el costo computacional.

En general, el modelo logra un equilibrio adecuado entre simplicidad y capacidad predictiva.

---

## Referencias

[1] United States Environmental Protection Agency, “Outdoor Air Quality Data,” Disponible en: https://www.epa.gov/outdoor-air-quality-data

[2] United States Environmental Protection Agency, “Data,” Disponible en: https://www.epa.gov/data

[3] Documentación oficial de Scikit-learn, “Machine Learning in Python,” Disponible en: https://scikit-learn.org/
