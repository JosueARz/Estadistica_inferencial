Información de atributos:

1) ID number : número de identificación

2) Diagnosis : Diagnóstico (M = maligno, B = benigno)
3-32)

Se calculan diez características de valor real para cada núcleo celular:

a) radius :media de las distancias del centro a los puntos del perímetro.

b) texture :desviación estándar de los valores de la escala de grises.

c) perimeter: perimetro.

d) area: área.

e) smoothness: variación local en longitudes de radio.

f) compactness: perímetro ^ 2 / área - 1.0

g) concavity: severidad de las porciones cóncavas del contorno.

h) concave points: número de porciones cóncavas del contorno.

i) symmetry: simetría

j) fractal dimension: "aproximación a la línea de costa" - 1"

La media, el error estándar y el "peor" o mayor (media de los tres
valores más grandes) de estas características se calcularon para cada imagen,
resultando en 30 características. Por ejemplo, el campo 3 es Radio medio, campo
13 es Radius SE, el campo 23 es Worst Radius.

Todos los valores de características se recodifican con cuatro dígitos significativos.

Faltan valores de atributo: ninguno

Distribución de clases: 357 benignos, 212 malignos