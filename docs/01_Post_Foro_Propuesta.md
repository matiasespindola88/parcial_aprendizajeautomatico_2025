# 1. Post Original en el Foro - Propuesta de Proyecto

## Dominio de Interés y Contexto del problema
El dominio de interés se centra en la **Ingeniería Eléctrica y el Mantenimiento Predictivo** (Diagnóstico de Sistemas).

El contexto del problema se centra en sistemas de potencia: las interrupciones o anomalías pueden tener múltiples causas (**cortocircuito, sobrecarga, daño en componentes**). El desafío es que los sistemas de monitoreo arrojan datos sin procesar (voltaje, corriente).

## Motivación de la elección y objetivo del modelo
Elegí este proyecto porque aplica los modelos de **clasificación** a un problema de ingeniería con **alto valor práctico**. Permite la implementación de **k-Vecinos Más Cercanos (k-NN)** y **Regresión Logística** a través de una tarea de **clasificación multiclase**.

El objetivo del modelo es desarrollar un modelo de **Clasificación Multiclase** que prediga la etiqueta categórica de la **Causa de la Falla** (Y) a partir de las mediciones eléctricas en tiempo real (X), transformando los datos brutos en un diagnóstico automatizado.

## Características del Dataset y Variables Involucradas

Para este proyecto, voy a utilizar un dataset de diagnóstico eléctrico específico y estructurado, alineado con problemas de ingeniería real.

### Variables Involucradas

| Tipo de Variable | Variables Involucradas | Descripción en el Dataset |
| :--- | :--- | :--- |
| **Predictoras (X)** | I25a, i25b, i25c (corrientes) – v25a, v25b, v25c (voltajes) – pg, gg (potencias) | Todas **numéricas**. Son las mediciones de los parámetros eléctricos clave que definen el estado del sistema. |
| **Objetivo (Y)** | Target o Class | **Categórica discreta**. El valor de esta columna representa la clase de falla específica (ej. 1= Cortocircuito, 2= Falla de rotor). |

## Técnicas de Aprendizaje Automático
El proyecto utilizará los modelos vistos en la cursada:

* **K-NN:** Se utilizará para clasificar un nuevo evento de falla buscando **similitud con los patrones** de fallas históricas más cercanas. Demuestra cómo se aplica la distancia a un problema de diagnóstico.
* **Regresión Logística Multiclase:** Se implementará para predecir la **probabilidad** de que el evento pertenezca a cada una de las posibles clases de falla.

**Métricas:** La evaluación se realizará mediante métricas de **clasificación multiclase** (**matriz de confusión, precisión, recall y F1-Score** por clase), cruciales para entender el rendimiento del modelo en el diagnóstico de fallas menos frecuentes.

El proyecto se diferencia al aplicar algoritmos de clasificación a un problema de ingeniería de diagnóstico, lo que requiere un preprocesamiento cuidadoso (**normalización de variables**) y una interpretación de métricas orientada a la eficiencia operativa (ej. Minimizar el Falso Negativo en la detección de fallas críticas).