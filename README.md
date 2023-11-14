# Tratamiento de Señales 3
## Mini-Proyecto 2: Modelos de Variable Latente para el Reconocimiento de Emociones

### Descripción

La emoción es un proceso psicofisiológico desencadenado por la percepción consciente y/o inconsciente de un objeto o situación y, a menudo, se asocia con el estado de ánimo, el temperamento, la personalidad, la disposición y la motivación. Las emociones juegan un papel importante en la comunicación humana y pueden expresarse verbalmente a través del vocabulario emocional o mediante la expresión de señales no verbales como la entonación de la voz, las expresiones faciales y los gestos. La mayoría de los sistemas contemporáneos de interacción humano-computadora (HCI) son deficientes en la interpretación de esta información y carecen de inteligencia emocional. En otras palabras, no pueden identificar los estados emocionales humanos y utilizar esta información para decidir las acciones adecuadas que ejecutar. El objetivo de la computación afectiva es llenar este vacío detectando señales emocionales que ocurren durante la interacción humano-computadora y sintetizando respuestas emocionales.

La evaluación de las emociones a menudo se lleva a cabo mediante el análisis de las expresiones emocionales y/o señales fisiológicas de los usuarios. Las expresiones emocionales se refieren a cualquier comportamiento verbal y no verbal observable que comunica emoción. Hasta ahora, la mayoría de los estudios sobre evaluación de emociones se han centrado en el análisis de las expresiones faciales y el habla para determinar el estado emocional de una persona. También se sabe que las señales fisiológicas incluyen información emocional que se puede utilizar para evaluar las emociones, pero han recibido menos atención. Estas comprenden las señales que se originan en el sistema nervioso central (SNC) y el sistema nervioso periférico (SNP).

### Actividad de aprendizaje

Se requiere construir un framework que permita procesar y caracterizar las señales fisiológicas para agruparlas en estados emocionales. Para ello, se trabajará con la base de datos DEAPdataset, la cual es un conjunto de datos para el análisis de emociones usando señales de EEG, fisiológicas y de video (ver figura 1).

![Figura 1. Ejemplo de la base de datos DEAP](https://github.com/DavidELP17/TS3_MiniProyecto1/assets/17619940/ce5004e5-296d-400a-b948-c6af9eca62fa)
![Figura 2. Ejemplo de la base de datos DEAP](https://github.com/DavidELP17/TS3_MiniProyecto1/assets/17619940/14193f64-aadd-49d8-966d-3466e1f62b56)

Para el sistema de Análisis Multivariado de Señales fisiológicas obtenido en el Primer Mini-Proyecto, se debe construir un módulo de variable latente utilizando el algoritmo de PCA (Análisis de Componentes Principales). La idea es proyectar la matriz característica obtenida, a un espacio latente de menor dimensión \(q << D\). Seleccione diferentes configuraciones del número de componentes \(q\) y evalúe el mejor desempeño arrojado por el modelo midiendo la precisión (accuracy) y la matriz de confusión.

Dado que PCA es un modelo lineal de variable latente en el cual las características son mapeadas de la forma \(z=Wx\), en muchas aplicaciones reales las relaciones entre los datos son no lineales. Es por esto que modelos como la reducción de la dimensionalidad a través del uso de funciones de mapeo (kernel) no lineales puede ayudarnos en la tarea. Aquí el mapeo se realiza utilizando (z=Φx), donde \(Φ\) es la matriz de mapeo no lineal conocida como función de kernel. Estas funciones de kernel pueden tener diferentes naturalezas como lineales, exponenciales, polinomiales, entre otras. Su objetivo aquí es realizar el procedimiento de mapeo del dataset de movimientos utilizando Kernel PCA (Kernel Principal Component Analysis).

<p align="center">Figura 1. Ejemplo de la base de datos DEAP.</p>
