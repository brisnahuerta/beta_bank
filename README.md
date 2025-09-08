# Beta Bank - Predicción de abandono de clientes

Este repositorio se creó para practicar ejercicios de *Data Science* y desarrollar un modelo que anticipe la deserción de clientes en Beta Bank.

## Descripción del problema
Los clientes de Beta Bank se están yendo poco a poco cada mes. Los banqueros han descubierto que es más barato retener a los clientes existentes que atraer nuevos. Por ello, necesitamos predecir si un cliente dejará el banco pronto. El conjunto de datos `Churn.csv` contiene información histórica sobre el comportamiento de los clientes y la terminación de contratos con el banco.

## Objetivo
- Entrenar un modelo con el mayor valor F1 posible (meta ≥ 0.59).
- Verificar el valor F1 en el conjunto de prueba.
- Medir la métrica AUC-ROC y compararla con el F1.

## Herramientas utilizadas
- **Python 3** y **Jupyter Notebook** para el desarrollo interactivo.
- **Pandas** y **NumPy** para el manejo y la exploración de datos.
- **scikit-learn** para la construcción y evaluación de modelos:
  - `DecisionTreeClassifier`
  - `RandomForestClassifier`
  - `LogisticRegression`
- **GridSearchCV** para la optimización de hiperparámetros.

## Modelos desarrollados
Se entrenaron varios modelos de clasificación para identificar clientes propensos a abandonar:

| Modelo | F1 (prueba) | AUC-ROC |
|-------|-------------|---------|
| Random Forest | ≈0.60 | ≈0.83 |
| Decision Tree | ≈0.60 | ≈0.81 |
| Logistic Regression | ≈0.45 | ≈0.71 |

El **Random Forest** mostró el mejor equilibrio entre precisión y capacidad de discriminación, por lo que se recomienda como modelo final.

## Estructura del repositorio
- `beta_bank.ipynb`: notebook con todo el análisis, entrenamiento de modelos y evaluación.
- `Churn.csv`: datos de clientes utilizados para el entrenamiento y validación.

## Cómo reproducir
1. Instalar las dependencias principales: `pandas`, `numpy`, `scikit-learn`, `jupyter`.
2. Abrir el notebook `beta_bank.ipynb` y ejecutar las celdas en orden.

---
Este proyecto es una práctica de *Data Science* orientada a problemas reales de churn en el sector bancario.
