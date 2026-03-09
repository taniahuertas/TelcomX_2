# Telecom X - Análisis y Predicción de Churn

## 📋 Descripción del Proyecto

Este proyecto desarrolla un **modelo predictivo de churn (cancelación de servicios)** para una empresa de telecomunicaciones. El objetivo es identificar qué clientes tienen mayor probabilidad de abandonar el servicio, permitiendo a la empresa implementar estrategias proactivas de retención.

## 🎯 Contexto de Negocio

En la industria de telecomunicaciones, el **churn** (abandono de clientes) es uno de los desafíos operacionales más críticos. Adquirir nuevos clientes es significativamente más costoso que retener los existentes. 

**Valor del Proyecto:**
- Identificar clientes en riesgo antes de que se vayan
- Implementar campañas de retención dirigidas y personalizadas
- Reducir costos de adquisición optimizando recursos
- Mejorar la tasa de retención y el lifetime value de los clientes

## 📊 Dataset

- **Registros:** 7,267 clientes
- **Variables:** 23 atributos (demográficos, servicios, cargos)
- **Variable Objetivo:** Churn (26% churners, 74% no-churners)
- **Fuente:** Dataset balanceado con SMOTE para compensar desbalance de clases

## 🔑 Hallazgos Principales

### Factores Críticos de Churn:

1. **Tipo de Contrato** - Los contratos mes a mes tienen 5x más probabilidad de churn que contratos anuales
2. **Antigüedad (Tenure)** - Clientes nuevos (<6 meses) tienen riesgo 10x mayor
3. **Servicios Complementarios** - Ausencia de Online Security y Tech Support aumenta churn
4. **Tipo de Internet** - Fibra óptica correlaciona con mayor abandono
5. **Método de Pago** - Cheque electrónico muestra mayor propensión al churn

## 🛠️ Tecnologías Utilizadas

### Librerías de Datos y Análisis
- **pandas** - Manipulación y exploración de datos
- **numpy** - Operaciones numéricas
- **matplotlib & seaborn** - Visualización y análisis exploratorio

### Preprocesamiento
- **scikit-learn** - Encoding, escalado, train-test split
- **imbalanced-learn (SMOTE)** - Balanceo de clases

### Modelado Predictivo
- **XGBoost** - Gradient boosting (27 hiperparámetros optimizados)
- **RandomForest** - Ensemble learning (18 hiperparámetros optimizados)
- **GridSearchCV** - Búsqueda exhaustiva de mejores parámetros

## 📈 Resultados de Modelos

### Random Forest (Modelo Final)
- **Accuracy:** 77.6%
- **Recall Churn:** 69% (detecta 7 de cada 10 clientes que se van)
- **Precision:** 52%
- **Gap Entrenamiento-Validación:** 6pp (modelo robusto)

### XGBoost (Modelo Final)
- **Accuracy:** 77.2%
- **Recall Churn:** 63%
- **Precision:** 56%
- **F1-Score:** 0.59

**Modelo Recomendado:** Random Forest por su superior capacidad de identificar clientes en riesgo (recall).



