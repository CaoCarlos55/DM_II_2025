# Asignación #1 - Preprocesamiento - Ranking de Universidades del Mundo 2023

Para garantizar la integridad y el valor de los datos del `ranking universitario 2023`, se implementó un proceso de transformación riguroso para que cumpla con los requerimientos estructurales y funcionales.

---

Inicialmente, se aplicó una transformación estructural para normalizar los nombres de las variables al formato snake_case, eliminando espacios y caracteres especiales que dificultan el procesamiento. Asimismo, se abordó la variable compuesta de género donde se dividio en indicadores porcentuales independientes para mujeres y hombres. Continuando las transformaciones funcionales, se limpiaron los comas y símbolos de porcentaje en columnas que deberian ser numerica, asegurando que cada variable tuviera el tipo de dato correcto para los analisis estadísticos. Para resolver el problema de las puntuaciones expresadas en intervalos, se calculó el punto medio de cada rango, convirtiendo estos datos en valores numéricos representativos.

El tratamiento de datos nulo se realizó de varias formas:

- Se descartaron los registros no poseían nombre o ubicación, ya que estas variables son fundamentales para la identidad y el análisis geográfico de las universidades.

- Para las proporciones de género y datos poblacionales, se utilizó la mediana para rellenar los huecos sin distorsionar la tendencia central.

- En el caso de las puntuaciones de rendimiento, se aplicó una imputación por muestreo aleatorio de los valores existentes. Esta técnica es superior en este contexto porque preserva la variabilidad de los datos, evitando el sesgo que generaría el uso de un valor fijo como la media.

