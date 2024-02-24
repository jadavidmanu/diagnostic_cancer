# Análisis de Modelos de Clasificación para el Diagnóstico de Cáncer

## Nombre: David Maldonado

## Introducción

Este documento detalla la comparativa de varios modelos de clasificación aplicados a un dataset de diagnóstico de cáncer de mama. Se seleccionaron los algoritmos K Vecinos, Regresión Logística y Random Forest debido a su popularidad y rendimiento comprobado en tareas de clasificación binaria.

## Justificación de los Modelos

- **K Vecinos (KNN)**: Es un algoritmo bueno para sistemas donde se espera que los casos similares tengan la misma clasificación.

- **Regresión Logística**: Este modelo es ampliamente utilizado para problemas de clasificación binaria. En el caso nos ayudaría, ya que se requiere una decisión binaria clara y justificada.

- **Random Forest**: Este algoritmo utiliza múltiples árboles de decisión para mejorar la precisión predictiva y controlar el sobreajuste, lo cual es clave cuando se trabaja con datasets de alta dimensionalidad.

## Evaluación de Modelos

El rendimiento de los modelos se evaluó con un enfoque en minimizar los falsos negativos, que son críticos en el contexto médico para evitar omitir diagnósticos que requieren atención.

Los modelos de **Regresión Logística y Random Forest** mostraron el menor número de falsos negativos. Esto indica un rendimiento superior en la detección de diagnósticos positivos, lo que es esencial para garantizar que todos los casos de cáncer se traten adecuadamente.
Sin embargo, si se debe elegir al mejor modelo se puede considerar a la **Regresión Logistica**, ya que es un modelo más facil de interpretar (considerando el dataset no va a cambiar).

## Impacto del Oversampling

El oversampling mediante SMOTE se probó con el fin de abordar el desbalanceo de clases presente en el dataset. Sin embargo, los resultados indicaron que el oversampling no benefició a los modelos de Regresión Logística y Random Forest, ya que no hubo una reducción en los falsos negativos. En el caso del algoritmo K Vecinos, el oversampling aumentó los falsos negativos, lo cual sugiere que esta técnica podría no ser adecuada para este algoritmo en particular con este dataset.

## Conclusión

Para concluir, para este dataset de diagnóstico de cáncer, la Regresión Logística y el Random Forest sin aplicar técnicas de oversampling fueron los modelos más efectivos.