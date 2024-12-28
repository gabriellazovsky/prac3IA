# Práctica 3
# Predicción de propiedades moleculares mediante un modelo de machine learning

**Equipo de trabajo**

- Juan Antonio Peregrina
- Sergio Díaz
- Alejandro Figari
- Jorge Ángel Vázquez
- Javier Rozalén
- Gabriel Lazovsky

# Contenido

1. Introducción
1. Implementación del código
    1. Pasos previos
    1. Preprocesamiento de los datos
    1. Entrenamiento del modelo y estimación del error
        - Otros modelos probados        
    1. Generación de predicciones y exportación de resultados
1. Análisis de los resultados
    1. Predicciones vs. Valores reales en el conjunto de validación
    1. Errores vs. Predicciones en el conjunto de validación
    1. Distribución de Predicciones vs. Valores reales en el conjunto de validación
    1. Importancia de características
1. Conclusiones

# Introducción

En el ámbito de la química computacional y el aprendizaje automático, la predicción de propiedades moleculares ha surgido como una herramienta fundamental para acelerar procesos en áreas como el desarrollo de fármacos y la identificación de compuestos químicos. Entre estas propiedades, la Collision Cross Section (CCS) es particularmente relevante en espectrometría de masas, ya que describe cómo interactúan las moléculas con partículas en su entorno. La CCS es clave para identificar moléculas desconocidas comparando sus valores medidos con bases de datos de referencia. Sin embargo, los procedimientos experimentales para medir la CCS suelen ser costosos y laboriosos.

Esta práctica tiene como objetivo desarrollar un modelo de aprendizaje automático capaz de predecir la CCS de nuevas moléculas, utilizando como base datos preprocesados que incluyen descriptores moleculares, fingerprints estructurales y características categóricas. La implementación de un modelo predictivo robusto permitirá optimizar recursos en laboratorios, facilitar la identificación molecular y ampliar las bases de datos de referencia con valores calculados de CCS.

A lo largo de este trabajo se presentan las técnicas empleadas para el preprocesamiento de los datos, el entrenamiento y ajuste de un modelo, la estimación del error cometido sobre un conjunto de validación empleando como métrica el Median Absolute Error (MEDAE) y la generación de predicciones y exportación de los resultados.

Durante el desarrollo de la práctica se probaron dos modelos (**RandomForestRegressor** y **LightGBM**) y distintas técnicas de optimización de hiperparámetros (**GridSearchCV** y **RandomizedSearchCV**). Asimismo, se realizó una selección de características empleando el modelo **LassoCV**.

Finalmente, se realiza un análisis de resultados, se evalúan las limitaciones encontradas, posibles mejoras y lecciones aprendidas.
