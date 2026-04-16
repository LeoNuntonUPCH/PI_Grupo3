#  Predicción de Calidad del Aire (AQI) — Modelo de Regresión Lineal

---

# 1. Introducción

La calidad del aire es una variable ambiental crítica que influye directamente en la salud pública y la planificación urbana. En este proyecto se busca modelar y predecir el **Air Quality Index (AQI)** del día siguiente  utilizando datos históricos de contaminantes atmosféricos en California (2020–2023).

El objetivo principal es entender si el comportamiento reciente del AQI permite anticipar su evolución futura mediante un modelo de regresión lineal interpretable.

Este problema se formula como un problema de series temporales supervisadas, donde se intenta predecir el estado futuro del sistema a partir de su comportamiento pasado.

---

# 2. Metodología

## 2.1 Datos utilizados

Se utilizaron registros diarios de CO correspondientes a los años:

- 2020
- 2021
- 2022
- 2023

Cada observación corresponde a un día con información del AQI.

---

## 2.2 Variable objetivo (Target)

Se definió como:

###  Target:
\[
AQI_{t+1}
\]

Es decir, el **AQI del día siguiente**.

### Justificación del target

Este target se eligió porque:
- permite formulación predictiva real (forecasting)
- es útil para alertas tempranas de calidad del aire
- mantiene consistencia temporal del problema

---

## 2.3 Variables de entrada (Inputs)

Después de ingeniería de variables, se utilizaron:

### Variables finales:
- `AQI_roll7`  promedio móvil de 7 días
- `Month`  estacionalidad anual
- `DayOfWeek`  patrón semanal

---

## 2.4 Variables descartadas

Se descartaron variables por tres razones principales:

### 1. Redundancia (multicolinealidad)
- `AQI_lag1`
- `AQI_lag7`

 Motivo:
Estas variables representan información similar al promedio móvil (`AQI_roll7`), generando redundancia y mayor inestabilidad en el modelo.

---

### 2. Baja contribución
- `Days`

 Motivo:
No aportó información significativa y su coeficiente fue cercano a cero, indicando ausencia de tendencia lineal fuerte.

---

### 3. Ruido o baja relevancia
Variables operativas o constantes del dataset original  que no fueron usadas:
- metadata del sitio
- información geográfica constante
- variables de muestreo sin correlación significativa

---

## 2.5 Modelo utilizado

Se utilizó un modelo de:

###  Regresión Lineal (Sklearn LinearRegression)

Este modelo da:

- interpretabilidad alta
- adecuado para relaciones aproximadamente lineales
- permite análisis de coeficientes

---

## 2.6 División de datos

Se utilizó un enfoque temporal:

- **Train:** 80% inicial del tiempo
- **Test:** 20% final del tiempo


---

## 2.7 Métricas

- RMSE (Root Mean Squared Error)
- R² (Coeficiente de determinación)

---

# 3. Resultados

## 3.1 Rendimiento del modelo

| Conjunto | RMSE | R² |
|----------|------|----|
| Train    | 2.82 | 0.326 |
| Test     | 2.59 | 0.273 |

---

## 3.2 Interpretación del desempeño

###  R² ≈ 0.27 (test)

Esto indica que el modelo explica aproximadamente el **27% de la variabilidad del AQI futuro**.

### ¿Por qué no es más alto?

El AQI depende de factores no incluidos en el dataset:
- condiciones meteorológicas (viento, temperatura, presión)
- eventos externos (incendios forestales)
- emisiones industriales variables
- fenómenos atmosféricos no lineales

Por lo tanto, existe un **ruido estructural inherente al sistema**.

---

###  RMSE ≈ 2.6

Esto indica que el error promedio de predicción es de aproximadamente:

  - ±2.6 unidades de AQI

Dado que el AQI es una escala discreta y relativamente estable, este error es aceptable para un modelo lineal simple.

---

## 3.3 Interpretación de coeficientes

### Variable dominante:
- `AQI_roll7` es coeficiente ≈ 0.63

 Interpretación:
El promedio móvil de 7 días es el mejor predictor del AQI futuro, lo que indica fuerte autocorrelación temporal.

---

### Estacionalidad:
- Invierno (Nov–Feb) -> coeficientes positivos
- Verano (Jun–Aug) ->  coeficientes negativos

 Interpretación:
Peor calidad del aire en meses fríos debido a condiciones atmosféricas más estables y acumulación de contaminantes.

---

### Efecto semanal:
- Días laborales igual a  leve incremento de AQI
- Fines de semana igual a  menor impacto

 Interpretación:
Influencia moderada de actividad humana.

---

# 4. Discusión 

El modelo demuestra que la calidad del aire es un fenómeno altamente autocorrelacionado, donde el estado reciente del sistema domina la predicción.

Sin embargo, el rendimiento limitado del modelo (R² ≈ 0.27) sugiere que:

- el sistema es parcialmente no lineal
- existen variables externas no incluidas
- la variabilidad ambiental introduce ruido significativo

A pesar de esto, el modelo es útil para predicción básica y análisis interpretativo.

---

# 5. Conclusiones

- El mejor predictor del AQI futuro es el promedio móvil de 7 días.
- Existe fuerte estacionalidad en la calidad del aire.
- El modelo lineal es suficiente para capturar tendencias generales.
- El sistema tiene límites inherentes debido a factores externos no modelados.

---

# 6. Referencias (IEEE)

[1] U.S. Environmental Protection Agency, “Air Quality System (AQS),” EPA, 2024.  
[2] Scikit-learn Developers, “Linear Regression Documentation,” 2024. [Online]. Available: https://scikit-learn.org

