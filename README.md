# Proyecto de Detección de Fraude en Tarjetas de Crédito
## Descripción
Este proyecto está orientado a desarrollar un modelo de machine learning que permita detectar transacciones fraudulentas en tarjetas de crédito. La detección de fraude es crítica en sectores financieros, ya que permite reducir pérdidas y mejorar la confianza en las transacciones digitales. Para este proyecto, se cuenta con un dataset de transacciones históricas, donde se etiqueta cada transacción como fraudulenta o no.

## Objetivo del Proyecto
El objetivo principal es construir un modelo de clasificación que identifique con precisión las transacciones fraudulentas, minimizando tanto los falsos positivos como los falsos negativos, especialmente en una base de datos con una distribución de datos altamente desbalanceada.

## Pasos del Proyecto
1. Análisis Exploratorio de Datos (EDA)
- Análisis univariado y visualización: Se realizaron gráficos y análisis estadísticos para entender la distribución de las variables numéricas y categóricas.
- Análisis de datos atípicos: Se identificaron outliers (valores atípicos) que podrían afectar el desempeño del modelo, especialmente en las variables numéricas relacionadas con montos de transacciones.
2. Preparación y Limpieza de los Datos
- Tratamiento de datos faltantes: Se completaron o eliminaron valores nulos para asegurar que los datos estén listos para el entrenamiento del modelo.
- Corrección de valores atípicos: Se aplicó el método de rango intercuartílico para imputar los outliers y minimizar el impacto de valores extremos.
- Transformación de variables categóricas: Se transformaron las variables categóricas en numéricas, utilizando técnicas de codificación adecuadas (Label Encoding y One-Hot Encoding).
3. Balanceo de Datos
- Análisis de distribución de la variable objetivo: La variable objetivo ('IsFraud') estaba altamente desbalanceada, con el 99% de las transacciones no fraudulentas y solo el 1% fraudulentas.
Técnicas de balanceo aplicadas:
- Undersampling: Reducción de la clase mayoritaria para equilibrar las clases en el dataset.
1. Entrenamiento de Modelos de Machine Learning
- Se entrenaron diversos modelos, incluidos Regresión Lineal, Árbol de Decisión, Random Forest, y Stacking Regressor.
- Ajuste de hiperparámetros: Se realizó un ajuste de hiperparámetros para optimizar cada modelo y mejorar la precisión y recall, evitando el sobreajuste.
1. Evaluación de Modelos
- Métricas de evaluación: Se evaluaron precisión, recall, F1-score, y se analizó la matriz de confusión para cada modelo.
- Comparación de resultados: Se compararon los modelos con y sin balanceo de datos, observando un aumento significativo en el rendimiento del modelo balanceado.
Resultados del modelo óptimo:
Precisión: 0.99
Recall y F1-score: 0.99, con una alta capacidad para identificar fraudes sin aumentar los falsos positivos.
Resultados y Conclusiones
Los modelos entrenados con técnicas de balanceo de datos demostraron un rendimiento significativamente mejor en la detección de fraudes en comparación con el modelo sin balanceo. El modelo final logró identificar con precisión el 99% de los fraudes, con una tasa mínima de falsos negativos y una precisión general del 99%.

Recomendaciones para Mejoras Futuras
Pruebas en datos reales: Implementar el modelo en un entorno de producción para validar su rendimiento en datos en vivo.
** Validación cruzada y pruebas de robustez: Aplicar validación cruzada y métricas adicionales como el AUC-ROC. **
Explorar nuevas técnicas de balanceo: Investigar y probar técnicas avanzadas de balanceo para asegurar la estabilidad del modelo.