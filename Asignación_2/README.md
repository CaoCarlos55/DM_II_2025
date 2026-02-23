# Asignación #2 - Análisis Exploratorio de Datos (EDA) - Car Dataset

Para comprender a profundidad la estructura, descubrir patrones iniciales y evaluar la calidad del `car-dataset`, se hizo un Análisis Exploratorio de Datos para conocer la viabilidad de la información antes de cualquier etapa de modelado.

---

Inicialmente, se evaluó el volumen y los tipos de datos, confirmando una estructura mixta apta para el análisis estadístico. A través de la extracción de estadísticas descriptivas, se detectaron tempranamente fuertes asimetrías y diferencias entre las medianas y los valores máximos en variables clave como el precio y los caballos de fuerzas, alertando sobre la presencia de carros lujosos. Asimismo, la evaluación de valores faltantes reveló una pérdida de información del 31.41% en la variable de clasificacion de mercado, mientras que se confirmó que muchos atributos fundamentales y la variable objetivo mantuvieron casi la totalidad de la integridad, lo que resulta ideal para evitar sesgos por imputación en otras fases.

El análisis visual de distribuciones, detección de anomalías y correlaciones se abordó de varias formas:

- Para comprender el mercado, se generaron histogramas que aislaron la asimetría positiva extrema. Esto reveló que la mayoría de los carros se concentran entre los $20,000 y $40,000, y permitió descubrir un sesgo en el dataset provocado por autos de la década de 1990 ingresados con un valor base de $2,000.

- Se utilizaron diagramas de caja para confirmar e identificar los valores atípicos, evidenciando gráficamente la dispersión de superdeportivos de más de 1000 HP y carros ultra lujosos que superan la barrera del millón de dólares.

- Mediante mapas de calor y gráficos de dispersión, se evaluó la correlación entre las variables numéricas. Se identificó una fuerte relación de 0.66 entre la potencia y el precio, y una relación lineal de 0.89 entre el rendimiento en ciudad y autopista, lo que a su vez permitió clasificar visualmente a los carros 100% eléctricos de la muestra.

- Durante el análisis del grafico dispersión, se logró detectar una anomalía en una observación, revisando el registro físicamente imposible, pudimos verificar que es un carro con 354 MPG en autopista, esto probablemente sea un error de tipeo, gracias a esta identificación podemos preparnos mejor para futuras etapas de limpieza.