Estadística inferencial
==============================

## Diferencia entre estadística descriptiva e inferencial### Descriptiva
Parte de las estadísticas que nos ayuda a describir y comprender los datos, para explicar cómo se comportan los datos en el pasado y en el presente.
También nos ayuda a determinar:

- Tendencia central de variables (Media, Mediana, Moda)
- Variabilidad
- Distribución de variables (Unimodal, Bimodal, Multimodal)

### Inferencial
Parte de la estadística que nos ayuda a predecir o deducir características o resultados esperados en una población y así validar teorías. En esta parte vemos una abstracción de una muestra para determinar:

- Muestreo
- intervalos de confianza
- Validación de hipótesis
- Evitar sesgos

La inferencia estadística nos permite obtener conclusiones sobre los parámetros de una población de datos, además, estudiamos el grado de fiabilidad que tenemos de nuestros modelos.
## Estadística inferencial en data science y machine learning
La estadística inferencial la usamos tanto en el análisis como en los modelos predictivos, ya que esta os servirá para:

- Entender la distribución de nuestra información.
- Creación y validación de hipótesis.
- Experimentos.
- Elección adecuada de los modelos predictivos sugún los datos.

## Principales estadisticos
### Experimentos
Proceso en el que un fenómeno se puede realizar infinitamente y tiene un conjunto bien definido de posibles resultados, también conocido como "espacio muestral", estos experimentos pueden tener diferentes resultados:

- Random: si tiene más de un resultado posible.
- Determinista: si solo hay un valor posible.

### Población y muestra
La población es el conjunto de todos los datos sin importar sus condiciones, mientras que la muestra es un subconjunto de datos que pertenece a la población, y esta tiene algunas condiciones:

- Número suficiente de registros para ser estadísticamente significativo.
- Representación imparcial de la información total.

### Eventos
Son cada uno de los posibles resultados derivados de un experimento.
### Variable
Son cada uno de los atributos o características que tenemos de las muestras, existen diferentes tipos:

- Cualitativos: atributos no medibles.
-Cuantitativos: atributos medibles, estos se representan mediante números y existen dos tipos:
    
       - Discretos (son enteros o son aquillos que tienen valores finitos entre dos datos)
       - Continuos (son números decimales o pueden tomar cualquier valor entre dos datos)
### Probabilidad

Mide que tan posible es prevenir un determinado evento bajo ciertas condiciones, el análisis de eventos probabilísticos se llama estadística. Dentro de la probabilidad existe una logia llamada probabilidad condicional, esto es; La posibilidad de que un evento ocurra como consecuencia de otro evento pasado se define como:

![1](./reports/figures/1.png)
![2](./reports/figures/2.png)

### Distribución normal
La mayoría de los factores en el mundo se rigen por una `distribución normal`, esta tiene algunas características especiales:

- Distribución normal = Distribución gaussiana
- Moda = media = mediana
- es simétrico
- tiene forma de campana

La mayor parte de los datos se concentran en el centro, y a los lados están los datos atípicos y estarían representados por un gráfico como el siguiente.

![3](./reports/figures/3.png)

## Teorema del límite central
Las estadísticas establecen que, dada una muestra aleatoria suficientemente grande de la población, la distribución de medias seguirá una distribución normal.

## Muestreo
Es una técnica que nos ayuda a seleccionar una muestra, la cual se obtiene de una población estadística, y esta selección debe ser aleatoria y se espera que sus propiedades sean extrapolables a la población. Existen algunos tipos de fotografías, aquí vamos a ver las principales:

- Aleatorio Simple: Método de selección de determinadas unidades extraídas de una población de forma que cada una de las muestras tenga la misma probabilidad de ser elegida.
- Sistemático: Este método selecciona ciertas unidades al azar y luego el resto de las muestras se eligen siguiendo intervalos regulares.
-Estratificado: Este método selecciona ciertas unidades por segmentos exclusivos y homogéneos y luego se elige una muestra aleatoria simple de cada segmento.
## Media muestral

Debemos recordar algunos conceptos básicos como media, moda y mediana:

- Medias: Suma de los datos dividida por la cantidad de datos.
- Moda: Los datos que más se repiten.
- Mediana: Es el dato que está en el centro de todos.

La media muestral es la conocida media aritmética y se obtiene sumando un conjunto de valores cuantitativos y dividiéndolo por el número total de elementos sumados. La media muestral es diferente de la media poblacional.

## Varianza y desviación estándar muestral y poblacional

La varianza y la desviación estándar nos ayudan a calcular qué tan dispersa está una población o muestra, es decir, qué tan lejos están de la media, recuerda que la desviación estándar es la raíz cuadrada de la varianza. Para calcular estas propiedades estadísticas, tanto poblacionales como muestrales, podemos hacerlo con las siguientes ecuaciones.

![4](./reports/figures/4.png)

## Intervalos de confianza

Este es un par o pares de números entre los cuales se estima que existirá un valor desconocido respecto a un parámetro poblacional con cierto nivel de confianza, y estos son simétricos respecto a las medias.

### Nivel de significación

Este nivel de significación o alfa es el nivel límite para juzgar si un resultado es o no estadísticamente significativo. Si el valor de significancia es menor que el nivel de significación, el resultado será estadísticamente significativo.
## Prueba de hipótesis
Hypothesis or significance tests help us judge if there is any significant difference between the sample size and the overall parameter. To perform these tests we can follow some steps such as the ones shown below:

- Establish a null hypothesis (H0) and an alternative hypothesis (H1).
- Select the level of significance.
- Select the test statistic.
- Formulate the decision rule.
- interpret the results and make a decision.

## Tipos de pruebas de hipótesis

- Distribución t de Student: Se utiliza para estimar una media poblacional distribuida normalmente a partir de una pequeña muestra que sigue una distribución normal y cuya desviación estándar se desconoce.
- Coeficiente de Pearson: Se utiliza para medir la dependencia lineal (correlación) entre dos variables aleatorias cuantitativas.
- Análisis de varianza (ANOVA): Se utiliza para comparar varianzas entre las medias (o la media) de diferentes grupos.

## Tipos de errores
Las conclusiones a las que llegamos están basadas en una muestra, por lo que podemos cometer errores, para ello podemos separar las decisiones en correctas e incorrectas como en la siguiente tabla:

| |H0 Verdadera|H0 Falsa|
|-----------|----------|------------|
|Rechazar H0|Error tipo I P(Error tipo I)= $\alpha$| Decisión correcta|
|No rechazar H0|Decisión correcta| Error tipo II P(Error tipo II) = $\beta$|


## Bootstrapping

Este método se utiliza cuando queremos extraer una muestra de una población, pero la población es pequeña. Es decir, un método de remuestreo de datos de una muestra aleatoria. Se utiliza para encontrar una aproximación a la distribución de la variable analizada. Este método nos ayuda a no sesgar los resultados, esto se puede utilizar en el aprendizaje automático para evitar el sobreajuste.

## Validación cruzada
Es una técnica utilizada para evaluar los resultados de un análisis estadístico y así poder garantizar la independencia de las particiones de datos de entrenamiento y prueba.
Proceso:

- Dividir datos aleatoriamente en k grupos de tamaño similar.
- Los grupos k-1 se usan para entrenar el modelo y uno de ellos se usa para validarlo.
- El proceso se repite k veces usando un grupo diferente como validación para cada iteración.




Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
