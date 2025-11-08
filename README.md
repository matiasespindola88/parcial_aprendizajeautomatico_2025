# Proyecto: Clasificación de Fallas en Sistemas Eléctricos (Mantenimiento Predictivo)

## 1. Descripción del Proyecto
Este proyecto tiene como objetivo implementar modelos de Aprendizaje Supervisado para el diagnóstico automatizado de fallas en sistemas eléctricos. La tarea es realizar una **Clasificación Multiclase** de la causa raíz de una anomalía, optimizando la intervención técnica y la eficiencia del mantenimiento.

---

## 2. Descripción del Dataset (`data/faultdata-new.csv`)

### Origen y Acceso
El *dataset* es una fuente de datos sintéticos y etiquetados, ampliamente utilizada en la investigación de ingeniería eléctrica para el desarrollo de modelos de detección y diagnóstico de fallas en sistemas de potencia.

* **Fuente Principal:** [Electrical System Fault Diagnosis Dataset](https://www.kaggle.com/datasets/rahulvyasm/electrical-system-fault-diagnosis-dataset) (Kaggle).
* **Tipo de Datos:** Tabulares, simulando mediciones de sensores en tiempo real.
* **Licencia:** Dominio público o licencias de uso académico.

### Estructura del Dataset
| Característica | Detalle |
| :--- | :--- |
| **Instancias (Registros)** | 1,788 |
| **Características (Columnas)** | 19 |
| **Tipo de Problema** | Clasificación Multiclase (Aprendizaje Supervisado) |
| **Variables Predictoras ($X$)** | 19 (Mediciones eléctricas) |
| **Variable Objetivo ($Y$)** | 1 (`Target` o `Class` - La etiqueta de la falla) |

### Tipos de Variables

Todas las variables son **Numéricas**, lo que requiere un preprocesamiento cuidadoso (normalización o estandarización) debido a las diferentes escalas (ej., Corriente vs. Voltaje).

| Rol | Ejemplos de Variables | Tipo de Dato | Función en el Modelo |
| :--- | :--- | :--- | :--- |
| **Predictoras ($X$)** | `R`, `i25a`, `v25c`, `pg`, `qg`, etc. | Numérico Continuo | Mediciones de Resistencia, Corrientes, Voltajes y Potencias. |
| **Objetivo ($Y$)** | `Target` (o `Class`) | Numérico Discreto | La etiqueta que define el **Tipo de Falla** específica. |

---

## 3. Estructura del Repositorio (Objetividad de Cookiecutter)

La estructura del repositorio ha sido diseñada para ser objetiva y minimalista, siguiendo buenas prácticas de *Data Science* sin carpetas de relleno:
```
parcial_aprendizajeautomatico_2025/
 ├── data/
 │   ├── raw/
 │   │    └── faultdata-new.csv  # Dataset original del proyecto.
 │   └── processed/
 │        └── faultdata-escalado.csv #Dataset preprocesado.
 ├── docs/ # Documentación formal 
 │   ├── 01_Post_Propuesta_Foro.md # Documentación histórica del foro.
 │   ├── Propuesta_Parcial_Espindola_Matias.pdf # Primera entrega formal.
 │   ├── Diccionario de Datos.pdf # Archivo pdf con el diccionario de datos
 │   ├── Informe de Cierre de la Exploración de datos # Informe detallado del EDA
 │   └── Analisis de Metricas y Conclusiones.pdf # Informe Final del Proyecto
 ├── src/ # Código fuente del proyecto (notebooks y scripts).
 │   ├── Entrega02_Espindola_Matias.ipnyb # Notebook de exploración y entrenamiento.
 │   ├── Entrega03_Espindola_Matias.ipnyb # Notebook de comparación y selección del modelo optimo.
 │   └── Entrega_Parcial_Espindola_Matias.ipnyb # Notebook final del proyecto.
 ├── media/
 │   ├── Link_Video.txt # Archivo .txt que contiene el enlace a Google Drive para visualizar el video.
 │   └── Video_Parcial_Espindola_Matias.mp4 # Video explicativo del proyecto.
 ├── .gitignore # Para evitar subir archivos temporales/grandes.
 ├── README.md # Descripción completa del proyecto y dataset (este archivo).
 └── DESCRIPCION_PROYECTO.txt # Bloque de texto con objetivos y justificación.
 ```
