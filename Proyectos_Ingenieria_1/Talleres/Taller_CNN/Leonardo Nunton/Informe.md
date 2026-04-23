# Informe Técnico: Clasificación de Imágenes de Ultrasonido con CNN
**Estudiante:** Leonardo Fabián  
**Institución:** Universidad Peruana Cayetano Heredia (UPCH)  
**Dataset:** BreastMNIST (MedMNIST v2)

## 1. Resumen de la Actividad
Se realizó el entrenamiento y optimización de una Red Neuronal Convolucional (CNN) para la detección de nódulos en imágenes de ultrasonido de mama. El objetivo principal fue adaptar un flujo de trabajo de clasificación médica, optimizando la arquitectura y los hiperparámetros para un entrenamiento de **25 épocas**.

## 2. Configuración del Dataset
* **Nombre:** BreastMNIST.
* **Tipo:** Ultrasonido 2D (escala de grises).
* **Clases:** 2 (Maligno y Benigno).
* **Tamaño:** Imágenes de 28x28 píxeles.

## 3. Desarrollo Técnico y Optimizaciones
Para cumplir con los objetivos académicos y mejorar la robustez del modelo, se realizaron las siguientes modificaciones:

### A. Mejora de la Arquitectura (SimpleCNN)
Se implementó una red con 3 bloques convolucionales integrando:
* **Batch Normalization**: Para estabilizar el aprendizaje y permitir una convergencia más rápida en las 25 épocas.
* **Dropout (0.1, 0.2, 0.5)**: Aplicado estratégicamente en las capas de características y en el clasificador final para mitigar el sobreajuste (overfitting).
* **Adaptive Average Pooling**: Para reducir la sensibilidad de la red a la ubicación exacta de la lesión en la imagen de ultrasonido.

### B. Estrategia de Entrenamiento
* **Épocas:** 25.
* **Optimizador:** Adam (LR inicial: 0.001).
* **Learning Rate Scheduler:** Se utilizó un `StepLR` que redujo el ritmo de aprendizaje cada 7 épocas, permitiendo que el modelo se estabilizara en los mínimos locales de la función de pérdida.

## 4. Análisis de Resultados

### Métricas de Rendimiento
El modelo alcanzó una convergencia saludable:
* **ROC-AUC:** Cerca de **0.78**, demostrando una capacidad sólida para discriminar entre tejido sano y patológico.
* **Accuracy:** Estabilizado en el rango de **73% - 78%**.
* **Pérdida (Loss):** Reducción constante hasta **0.49**, mostrando que el modelo no se "estancó" durante las 25 épocas.

### Evaluación Diagnóstica
1. **Matriz de Confusión:** El modelo muestra un excelente desempeño en la detección de casos **Benignos** (Clase 1), logrando 109 aciertos. Se identifica la reducción de falsos positivos como la principal área de optimización clínica futura.
2. **Interpretación (Grad-CAM):** Las visualizaciones de mapas de calor confirman que la red está aprendiendo a identificar las regiones de mayor densidad y textura irregular dentro del parénquima mamario, validando la relevancia clínica de las características aprendidas.

## 5. Conclusión
La actividad fue completada exitosamente. La combinación de una arquitectura con **BatchNorm/Dropout** y un entrenamiento extendido a **25 épocas** permitió que el modelo superara las limitaciones iniciales de un entrenamiento estándar. El flujo de trabajo implementado garantiza un equilibrio entre la precisión técnica y la generalización necesaria para el análisis de imágenes médicas.