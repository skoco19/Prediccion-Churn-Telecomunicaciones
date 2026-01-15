# Proyecto de Predicción de Fuga de Clientes (Churn) en Telecomunicaciones

## Descripción del Proyecto

Este proyecto se enfoca en el desarrollo y optimización de un modelo predictivo para la identificación temprana de clientes propensos a la fuga (churn) en una empresa de telecomunicaciones. El objetivo principal es proporcionar una herramienta robusta que permita a la empresa implementar estrategias de retención proactivas, minimizando así las pérdidas económicas y maximizando la lealtad del cliente.

El análisis abarca desde el preprocesamiento de datos hasta la construcción y evaluación de modelos avanzados de Machine Learning, con un enfoque particular en la interpretación de los resultados para la toma de decisiones estratégicas.

## Características Clave y Logros

*   **Desarrollo de Modelos Predictivos**: Construcción y optimización de modelos de clasificación utilizando **Random Forest** y **Regresión Logística**.
*   **Alta Capacidad de Detección**: **Logro de un Recall del 86%** en la identificación de clientes en riesgo de fuga en el conjunto de prueba, demostrando una alta eficacia en la detección de casos positivos (churners).
*   **Feature Engineering Avanzado**: Creación de nuevas características significativas a partir de datos existentes (ej., `FamilyMembers`, `NoInternet`, `Extras`, `ContractMtM`, `Contract2year`, `InternetServiceFiber`, `PaidElectronicCheck`) para mejorar la capacidad predictiva del modelo.
*   **Manejo de Clases Desbalanceadas**: Implementación de técnicas como `class_weight='balanced'` para abordar el desbalance entre las clases de clientes con y sin fuga, asegurando un rendimiento equitativo del modelo.
*   **Análisis de Factores Clave**: Identificación de las variables más influyentes en el churn, incluyendo el tipo de contrato (especialmente mes a mes), la antigüedad del cliente (`tenure`), los cargos mensuales y totales, y el tipo de servicio de Internet (fibra óptica).
*   **Interpretación de Resultados**: Visualización detallada de métricas clave como el F2-score (priorizando el recall), matrices de confusión y reportes de clasificación para una comprensión profunda del rendimiento del modelo.
*   **Generación de Conocimiento Accionable**: Provisión de insights valiosos que pueden guiar el diseño de campañas de retención personalizadas y estrategias comerciales.

## Resultados del Modelo (Regresión Logística en Test Set, umbral 0.45)

*   **F2-score**: 0.748
*   **Recall (Clase Churn)**: 0.86 (86% de los clientes que se fugan son correctamente identificados)
*   **Precision (Clase Churn)**: 0.49
*   **Accuracy**: 0.72

## Factores de Churn más Influyentes (Basado en Random Forest Feature Importance)

1.  **ContractMtM** (Contrato mes a mes)
2.  **tenure** (Antigüedad del cliente)
3.  **InternetServiceFiber** (Servicio de Internet de Fibra Óptica)
4.  **Contract2year** (Contrato de dos años)
5.  **TotalCharges** (Cargos totales)
6.  **MonthlyCharges** (Cargos mensuales)

## Tecnologías Utilizadas

*   **Python**: Lenguaje de programación principal.
*   **Pandas**: Manipulación y análisis de datos.
*   **NumPy**: Computación numérica.
*   **Scikit-learn**: Modelado predictivo (RandomForestClassifier, LogisticRegression, StandardScaler, train_test_split).
*   **Imblearn**: Manejo de clases desbalanceadas (SMOTE, aunque `class_weight` fue usado directamente en los modelos finales).
*   **Matplotlib & Seaborn**: Visualización de datos y resultados.
*   **ydata-profiling**: Análisis exploratorio de datos automatizado.


