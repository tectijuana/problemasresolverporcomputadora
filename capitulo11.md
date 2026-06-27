# Capítulo 11: Miscelánea de Problemas

> *Basado en el libro de Donald D. Spencer, Editorial Limusa, 1985*

## Introducción

Este capítulo presenta problemas que cubren áreas diversas: dibujo por computadora, reconocimiento de patrones, matemáticas, conversiones de sistemas numéricos, generación de palabras y oraciones, estadística, procesamiento de texto, criptografía básica y algoritmos combinatorios. La variedad de temas refleja la versatilidad de la programación como herramienta universal para resolver problemas de cualquier disciplina.

## Problemas

**1.** La computadora puede servir como herramienta para trazar figuras mediante caracteres ASCII. Redactar un programa para dibujar un árbol de Navidad:

```
         *
        ***
       *****
      *******
     *********
    ***********
         *
         *
```

**2.** Generar una figura imprimiendo X's en la pantalla de salida. Deben definirse reglas respecto a la manera en que se imprimirán las X's para que la figura tenga alguna forma reconocible.

**3.** Trazar la carátula de un reloj, incluyendo los doce números y las manecillas. Como entrada, el programa deberá aceptar dos números que representarán la hora. Así, los números 7 y 30 significarían las 7:30.

**4.** Redactar un programa que trace la bandera de México usando caracteres ASCII. Usar G para la franja verde, W para la franja blanca con un asterisco central que represente el escudo, y R para la franja roja. Repetir cada franja por varias líneas.

**5.** Redactar un programa que trace una figura de algún personaje de historieta usando X's.

**6.** Trazar todos los registros posibles con cuatro dardos lanzados a un blanco circular con zonas de puntuación 1, 2, 3, 4 y 5.

**7.** Escribir un programa que genere poesía aleatoria combinando palabras de listas predefinidas de verbos, sustantivos, adjetivos y artículos.

**8.** De un archivo de datos de adjetivos y nombres, generar símiles aleatorios de la forma *(adjetivo)* COMO UN *(nombre)*. Por ejemplo: RÁPIDO COMO UN CONEJO, RICO COMO UN MILLONARIO.

**9.** Hacer un programa que genere oraciones de cuatro palabras: artículo + sustantivo + verbo + complemento.

**10.** Generar un programa para producir música aleatoria. El programa deberá elegir aleatoriamente notas (Do, Re, Mi, Fa, Sol, La, Si) y duraciones (redonda, blanca, negra, corchea) e imprimir la secuencia generada.

**11.** Calcular los honorarios de una niñera para un cierto tiempo de entrada y salida. Su sueldo es de \$120/h hasta las 11 PM y de \$180/h a partir de esa hora.

**12.** Preparar un programa para convertir unidades de cocina. Las relaciones son: 3 cucharaditas = 1 cucharada; 4 cucharadas = un cuarto de taza; 4 cuartos de taza = 1 taza; 2 tazas = 500 mL. Con los códigos 1 (cucharadita), 2 (cucharada), 3 (cuarto de taza), 4 (taza) y 5 (mililitros), introducir la cantidad, unidades actuales y las nuevas unidades requeridas.

**13.** Generar un programa que calcule la correlación entre calificaciones escolares y promedios de puntos por grado para un grupo de estudiantes.

**14.** La ciudad de Futura tenía 125,000 residentes en el año 2020. Cada año nace un nuevo niño por cada 210 residentes y hay un deceso por cada 263 residentes. Cada año llegan a Futura 610 nuevos residentes y la abandonan 840. Determinar la población en el año 2050.

**15.** Escribir un programa para convertir cualquier número del 1 al 3000 a su equivalente romano. Los siete símbolos romanos son: M (1000), D (500), C (100), L (50), X (10), V (5), I (1). Las reglas de formación son: a) si un símbolo precede a uno de valor menor, se agrega su valor; b) si un símbolo precede a uno de valor mayor, su valor se resta; c) los números se escriben lo más sencillamente posible, usando solo C, X e I como sustraendos. Ejemplos: MCMLXIV (1964) y DXLIX (549). Convertir: 1, 14, 400, 549, 999, 1964, 1984, 2500, 2994, 3000.

**16.** Redactar un programa que calcule el cambio mínimo en billetes y monedas para un pago dado. Las denominaciones disponibles son: billetes de \$500, \$200, \$100, \$50, \$20 y monedas de \$10, \$5, \$2, \$1 y \$0.50. Por ejemplo, para un cambio de \$253.50 el programa imprimirá: un billete de \$200, uno de \$50, uno de \$2, uno de \$1 y una moneda de \$0.50.

**17.** Calcular el promedio de bateo de los siguientes cinco jugadores e imprimir una tabla de información en orden de promedios decrecientes. El promedio de bateo = Hits / Veces al bat.

| Jugador | Veces al bat | Hits |
|---------|-------------|------|
| 1 | 107 | 31 |
| 2 | 98 | 40 |
| 3 | 114 | 26 |
| 4 | 101 | 42 |
| 5 | 118 | 37 |

**18.** Los porteros de diez equipos de la Liga MX tienen las siguientes cifras de la temporada. El rendimiento se calcula como: Goles en contra por partido = Goles en contra / Partidos jugados. Introducir las cifras, calcular los promedios e imprimir la tabla completa en orden ascendente (menor promedio = mejor desempeño). Incluir también el porcentaje de partidos invicto.

| Portero | Goles en contra | Partidos | Partidos invicto |
|---------|----------------|----------|-----------------|
| 1 | 18 | 17 | 5 |
| 2 | 24 | 14 | 3 |
| 3 | 15 | 14 | 6 |
| 4 | 28 | 16 | 2 |
| 5 | 12 | 12 | 4 |
| 6 | 8 | 10 | 5 |
| 7 | 11 | 9 | 3 |
| 8 | 19 | 8 | 1 |
| 9 | 7 | 7 | 3 |
| 10 | 5 | 5 | 2 |

**19.** Enseñar a una computadora a "leer" desarrollando un conjunto normal de caracteres y redactando un programa para que la computadora pueda reconocer patrones de ese tipo. Cada carácter se representa en una cuadrícula de 5 × 7 celdas que pueden estar encendidas (X) o apagadas (espacio). El programa deberá reconocer al menos los dígitos del 0 al 9. (Este principio de representar caracteres como matrices de bits y clasificarlos por similitud es la base de los sistemas modernos de reconocimiento óptico de caracteres y de las primeras capas de una red neuronal convolucional.)

**20.** Calcular el número promedio de veces que aparece la letra "a" en todas las palabras de un texto de entrada. El programa deberá leer línea por línea y calcular la frecuencia de "a" por palabra.

**21.** Se ha especulado acerca de que si se diera a un grupo de monos máquinas de escribir y se les permitiera teclear al azar durante un período, escribirían finalmente cada libro que jamás haya sido escrito, incluyendo este. Correr un programa que simule un mono escribiendo. Suponer que los eventos del mono son independientes y que teclea letras del alfabeto al azar. El procesamiento se detendrá cuando el mono escriba la palabra MONO.

**22.** Generar un programa que dé habilidad a un estudiante para ejecutar operaciones aritméticas simples de suma, resta, multiplicación y división. El programa deberá generar problemas aleatorios e indicar si la respuesta es correcta o incorrecta.

**23.** Una niña del cuarto grado requiere práctica para sumar fracciones. Diseñar un programa que le proporcione ejercicios de suma de fracciones, registre sus avances y le haga progresar hasta problemas más complicados en la medida que demuestre dominar el material.

**24.** Escribir un programa que facilite a un estudiante la suma de números racionales. El programa deberá aceptar dos fracciones como entrada y mostrar la suma en forma reducida.

**25.** Una escuela técnica usa letras A, B, C, D y F para especificar el aprovechamiento del estudiante, con las siguientes ponderaciones:

| Calificación | Extraordinario | Regular |
|---|---|---|
| A | 5 | 4 |
| B | 4 | 3 |
| C | 3 | 2 |
| D | 1 | 1 |
| F | 0 | 0 |

Escribir un programa que acepte el número de calificaciones en cursos regulares y extraordinarios recibidos, y calcule el promedio de puntuación por grado del estudiante.

**26.** La ciudad ficticia de Esperanza tiene 1,000 habitantes y es autosuficiente en alimentos (produce suficiente comida para 100,000 personas). Sin embargo, cada 10 años se duplica la población y en ese tiempo puede producirse suficiente comida para alimentar a 4,000 personas más que en los 10 años anteriores. Sacar una tabla en el siguiente formato:

```
Años después   Población   Suministro de alimento
      0          1,000          100,000
     10          2,000          104,000
     20          4,000          108,000
     30          8,000          112,000
```

El programa se detendrá cuando la población exceda al suministro de alimentos.

**27.** ¿De cuántas maneras se puede dar un cambio exacto de \$20 usando monedas de \$10, \$5, \$2, \$1 y \$0.50?

**28.** A un repartidor se le paga \$1 el primer día de trabajo, \$2 el segundo, \$4 el tercero y así sucesivamente, duplicando su percepción cada día durante 30 días. Calcular su ingreso al trigésimo día y su total por los 30 días.

**29.** En un curso de ecología en una escuela secundaria se practicaron cinco exámenes con las siguientes ponderaciones: examen 1 = 10%, examen 2 = 15%, examen 3 = 25%, examen 4 = 15%, examen 5 = 35%. Las puntuaciones de seis estudiantes son:

| Estudiante | Exam 1 | Exam 2 | Exam 3 | Exam 4 | Exam 5 |
|---|---|---|---|---|---|
| 1 | 63 | 68 | 72 | 89 | 93 |
| 2 | 99 | 100 | 76 | 83 | 94 |
| 3 | 53 | 68 | 63 | 75 | 78 |
| 4 | 93 | 97 | 100 | 89 | 91 |
| 5 | 75 | 72 | 81 | 78 | 84 |
| 6 | 78 | 81 | 69 | 75 | 79 |

Calcular la calificación final ponderada para cada estudiante.

**30.** Se dan las temperaturas promedio durante seis meses en una ciudad:

| Mes | Temperatura (°C) |
|---|---|
| Junio | 26 |
| Julio | 32 |
| Agosto | 34 |
| Diciembre | 5 |
| Enero | 2 |
| Febrero | −3 |

Calcular las temperaturas promedio de verano (junio–agosto) e invierno (diciembre–febrero).

**31.** Dado un caballo colocado en la columna 5, fila 4 de un tablero de ajedrez, imprimir las ocho posiciones a donde se le permite desplazarse, de acuerdo con las reglas del ajedrez.

**32.** Los grupos sanguíneos A, B, O humanos se determinan por un sistema de tres alelos A, B y O. Los genotipos AA y AO forman el grupo A; BB y BO el grupo B; AB es el grupo AB; y OO es el grupo O. Generar un programa para determinar si las siguientes proporciones son consistentes con la hipótesis de apareamiento aleatorio. Datos: A = 33.6%, B = 20.8%, AB = 8.4%, O = 29.3%.

**33.** En una escuela secundaria se realizó una encuesta para conocer al jugador de fútbol de la Liga MX más popular. Se usaron los números 1, 2, 3 y 4 para registrar votos: 1 = L. Ramírez (delantero), 2 = A. Flores (mediocampista), 3 = M. Torres (defensa), 4 = J. Soto (portero). Participaron 52 personas y arrojaron los siguientes votos: 4, 1, 1, 2, 4, 1, 2, 3, 4, 4, 4, 1, 3, 3, 2, 4, 1, 2, 1, 4, 3, 3, 4, 1, 2, 4, 3, 2, 4, 4, 3, 1, 2, 4, 4, 3, 1, 1, 3, 4, 4, 4, 2, 1, 2, 4, 2, 4, 2, 1, 3, 4. Encontrar el triunfador.

**34.** Una familia trata de determinar la posición nocturna del termostato que resulte más económica. La compañía de servicios calcula el costo en unidades por cada noche mediante:

$\text{costo} = \frac{(m - 1)^2}{10} + \frac{(22 - t)^2}{100}$

donde $m$ es la temperatura nocturna en °C y $t$ es la posición del termostato en °C. La temperatura nocturna media $m$ varía uniformemente entre −7°C y 21°C durante el año. Simular los valores de $m$ durante un año y calcular el costo de utilidad para un valor dado de $t$. Usar el programa con varios valores de $t$ para encontrar la posición más económica.

**35.** Tres grupos de ratas corren en una caja de Skinner en la que al presionar una barra obtienen alimento, bajo tres niveles de choque eléctrico. Redactar un programa para determinar si existe un efecto significativo del nivel de choque sobre la respuesta promedio de las ratas (número de presiones por hora).

**36.** El número 1729 puede expresarse de dos maneras diferentes como la suma de dos cubos. Correr un programa que encuentre los pares $(X, Y)$ tales que:

$X^3 + Y^3 = 1729$

**37.** Un pato y un palomo se encuentran entre las aves que vuelan al sur para pasar el invierno. El pato se encuentra a 100 km adelante del palomo y vuela a 95 km/h. El palomo vuela por la misma ruta a 105 km/h. ¿Cuánto tardará el palomo en alcanzar al pato y a qué distancia lo hará?

---

## Problemas adicionales

> *Problemas de elaboración propia, inspirados en el capítulo.*

**38.** Escribir un programa de conversión completa entre cuatro sistemas numéricos: binario (base 2), octal (base 8), decimal (base 10) y hexadecimal (base 16). El programa deberá aceptar un número en cualquiera de las cuatro bases e imprimirlo en las otras tres. Ejemplos de verificación: $255_{10} = 11111111_2 = 377_8 = \text{FF}_{16}$.

**39.** El cifrado de César desplaza cada letra del alfabeto en $k$ posiciones. Por ejemplo, con $k = 3$: A→D, B→E, ..., Z→C. Escribir un programa que: a) cifre un mensaje dado con una clave $k$ introducida por el usuario; b) descifre un mensaje cifrado dada la clave; c) rompa el cifrado por análisis de frecuencia de letras (la letra más frecuente en español es la E).

**40.** Análisis de frecuencia de caracteres en un texto: leer un párrafo de texto y calcular la frecuencia absoluta y relativa de cada letra del alfabeto (ignorando mayúsculas, acentos y signos). Imprimir una tabla ordenada de mayor a menor frecuencia y un histograma de barras ASCII horizontal.

**41.** El código Morse representa cada letra y dígito como una secuencia de puntos (·) y rayas (−). Escribir un programa que traduzca un texto en español a código Morse y viceversa. Por ejemplo: S = ··· , O = −−−, SOS = ··· −−− ···.

**42.** Un palíndromo es una palabra o frase que se lee igual de izquierda a derecha que de derecha a izquierda (ignorando espacios y signos). Ejemplos: "Anita lava la tina", "Yo soy". Escribir un programa que: a) determine si una palabra o frase es palíndromo; b) encuentre todas las palabras palíndromas en un texto dado.

**43.** La compresión por codificación de longitud de repetición (RLE, *Run-Length Encoding*) reemplaza secuencias de caracteres repetidos con el carácter y su conteo. Por ejemplo: "AAAAABBBCC" → "5A3B2C". Escribir un programa que: a) comprima un texto usando RLE; b) descomprima un texto codificado en RLE; c) calcule el porcentaje de compresión obtenido.

**44.** El índice de legibilidad de Flesch mide la facilidad de lectura de un texto:

$\text{Flesch} = 206.835 - 1.015 \cdot \frac{\text{palabras}}{\text{oraciones}} - 84.6 \cdot \frac{\text{sílabas}}{\text{palabras}}$

Un valor de 90–100 es muy fácil; 60–70 es estándar; 0–30 es muy difícil. Escribir un programa que lea un párrafo de texto, cuente palabras, oraciones y sílabas (aproximando las sílabas como el número de grupos vocálicos), y calcule e interprete el índice de Flesch.

**45.** El triángulo de Sierpinski es un fractal que puede generarse con caracteres ASCII usando el siguiente proceso: en una cuadrícula de 32 × 64, encender el píxel (fila $r$, columna $c$) si $(r\ \text{AND}\ c) = 0$ en aritmética de bits. Imprimir el triángulo resultante usando asteriscos (*) para las celdas encendidas y espacios para las apagadas.

**46.** El problema del viajante de comercio (TSP) simplificado: dado un conjunto de $N$ ciudades con sus coordenadas (en km), encontrar una ruta que visite todas las ciudades exactamente una vez y regrese al punto de partida, minimizando la distancia total. Implementar una solución por búsqueda exhaustiva para $N \leq 8$ ciudades y una heurística de "vecino más cercano" para $N$ mayor.
