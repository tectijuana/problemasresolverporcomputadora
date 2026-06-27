# Capítulo 2: Álgebra

> *Basado en el libro de Donald D. Spencer, Editorial Limusa, 1985*

## Introducción

Programar un problema estimula al estudiante a comprender lo que está haciendo, más que si solo confía en la lectura de problemas de muestra. Además, la computadora, al realizar los cálculos aritméticos, permite que el estudiante se concentre en el problema y en el método de solución, sin pérdida de tiempo. La computadora no domina ni decide el currículo; más bien sirve como auxiliar en la enseñanza para alcanzar las metas y objetivos propuestos, sobre los cuales se sustenta un programa de matemáticas moderno.

Se ha tratado, por lo tanto, de seleccionar problemas que se encuentran normalmente en cursos de Álgebra elementales e intermedios. En este capítulo se encontrarán problemas relacionados con desigualdades, oraciones verbales, potencias y raíces, funciones, gráficas, sistemas de ecuaciones lineales, polinomios, ecuaciones cuadráticas, números irracionales, exponentes, funciones circulares, números complejos, funciones exponenciales y logarítmicas, secuencias y series, programación lineal y otras áreas de los cursos de álgebra.

## Problemas

**1.** Dada una desigualdad $Ax + B > C$ (donde $A$, $B$, $C$ son números reales), resolver para $x$. Por ejemplo, si la desigualdad es $4x + 14 > 34$, imprimir $x > 5$.

**2.** Encontrar el conjunto de soluciones de cualquier desigualdad de la forma $ax^2 + bx + c < 0$ para valores cualesquiera de $a$, $b$ y $c$. Probar el programa con las siguientes desigualdades:

$$x^2 + 12x + 35 < 0$$

$$x^2 + x + 3 < 0$$

$$-x^2 + 3x + 2 < 0$$

**3.** Introducir un entero $N$ positivo e imprimir el producto $P$ de los cuatro enteros consecutivos $N$, $N+1$, $N+2$ y $N+3$. Verificar que $P + 1$ es un cuadrado perfecto.

**4.** Encontrar las raíces cuadradas de los enteros del 9 al 25. Imprimir el entero y su raíz cuadrada.

**5.** Introducir dos enteros y, sin multiplicarlos realmente, determinar si su producto es positivo, negativo o cero.

**6.** Imprimir un número real $N$, su inverso aditivo y su inverso multiplicativo (si lo tiene).

**7.** Calcular el cuadrado, cubo, raíz cuadrada y raíz cúbica de los enteros del 1 al 1,000. Imprimir los resultados en forma tabular.

**8.** Imprimir una tabla de valores para $y = a^x$, donde el usuario introduce la base $a$ y los valores enteros de $x$ van de 1 a 10.

**9.** Imprimir una tabla de cuadrados, cubos y raíces cuartas de los veinte primeros enteros.

**10.** Encontrar la solución para la ecuación exponencial $A^x = B$, donde $A = 3$ y $B = 81$.

**11.** Dados los valores de las constantes $a$, $b$, $c$ y $d$, y de la variable $x$ (introducidos por el usuario), calcular la función definida por:

$$f(x) = ax^2 + bx + c \quad \text{si } x < d$$

$$f(x) = 0 \quad \text{si } x = d$$

$$f(x) = -ax^2 + bx - c \quad \text{si } x > d$$

**12.** Para cada una de las siguientes parejas de números, encontrar el máximo común divisor: (60, 12); (35, 10); (28, 32); (65, 179); (210, 1036).

**13.** Hacer que la computadora genere parejas de enteros al azar. Encontrar el máximo común divisor de cada pareja.

**14.** Encontrar el máximo común divisor de un conjunto de tres números.

**15.** Hacer que la computadora genere conjuntos de tres enteros al azar y encontrar el máximo común divisor de cada conjunto.

**16.** Para cada una de las siguientes parejas de enteros, encontrar el mínimo común múltiplo: (25, 645); (132, 360); (192, 24).

**17.** Generar parejas de enteros y encontrar el mínimo común múltiplo.

**18.** Encontrar el mínimo común múltiplo de cinco números.

**19.** Factorizar los siguientes trinomios:

$$\text{(a)}\ 6x^2 + 11x + 3 \qquad \text{(b)}\ 5x^2 + 31x + 6$$

$$\text{(c)}\ 10x^2 + 6x - 24 \qquad \text{(d)}\ 2x^2 - 41x - 336$$

**20.** Factorizar el trinomio $3x^2 + 4x - 48$ en factores primos.

**21.** Dado el número de victorias, empates y derrotas de un equipo de fútbol, calcular su puntaje total y su porcentaje de rendimiento. Usar el sistema de puntuación oficial: victoria = 3 puntos, empate = 1 punto, derrota = 0 puntos. El porcentaje de rendimiento se calcula como puntos obtenidos entre puntos posibles (si hubiera ganado todos los partidos).

**22.** Un artesano de la Zona Libre de la Frontera Norte trabaja a razón de \$130 por hora hasta las 10 p.m. y de esa hora en adelante a razón de \$195 por hora (tarifa nocturna, 1.5×). Conocidas las horas en que comienza y termina de trabajar, calcular el costo total de una noche de trabajo. (Referencia: salario mínimo frontera norte 2026 = \$440.87/día).

**23.** La plataforma de streaming de una ciudad patrocina un sorteo con boletos numerados del 1 al 1,500. Introducir un número de boleto y verificar la lista de 12 números premiados (generados al azar) para ver si el número introducido está entre ellos.

**24.** Esteban tiene algunos libros de historietas: exactamente tres veces más que Miguel y cuatro más que Laura. Entre los tres tienen menos de 200 libros. ¿Cuántos tendrá cada uno? Mostrar todas las posibilidades.

**25.** Los jitomates cuestan \$2.50 por kg más que las papas. Si éstas cuestan $x$ pesos por kg, expresar el costo de 3 kg de papas y 1.5 kg de jitomates.

**26.** Una empresa de desarrollo de software tiene un presupuesto de \$10,000 para comprar exactamente 100 licencias. Las opciones son: licencia premium a \$500 c/u, estándar a \$150 c/u y básica a \$50 c/u. Debe adquirir al menos una de cada tipo y gastar exactamente \$10,000. ¿Cuántas combinaciones posibles existen? Imprimir todas las soluciones.

**27.** Encontrar la velocidad a la que debe viajar una persona para alcanzar a otra que salió del mismo lugar cierto tiempo antes.

**28.** Encontrar el tiempo que requiere una persona para alcanzar a otra si ambas parten en tiempos diferentes con velocidades distintas pero viajan en la misma dirección.

**29.** Una piscina rectangular mide $40 \times 13$ m. Una persona que está en la esquina $A$ quiere ir a la esquina $C$ en el menor tiempo posible. Tiene las opciones de rodear la piscina, nadar en diagonal o combinar caminata con nado. Su rapidez en carrera es de 1 m/s y nadando de 0.5 m/s. Encontrar la distancia nadada y la distancia caminada para ir de $A$ a $C$ en el menor tiempo.

**30.** Un bote navega a razón de 10 km/h en aguas tranquilas. Si necesita 4 h para recorrer 20 km contra la corriente, determinar la rapidez de la corriente del río.

**31.** Encontrar la distancia entre dos personas que parten del mismo punto al mismo tiempo, pero viajan en direcciones opuestas y con velocidades diferentes.

**32.** Si cinco parejas de pájaros empollan 3 huevecillos hasta la madurez y mueren enseguida, dejando 15 pájaros para acoplarse y empollar también 3 huevos por pareja hasta la madurez, para morir luego, etc., ¿cuántos pájaros habrá al término de 5 años?

**33.** Roberto hace 50% más trabajo que Guillermo y 25% más que Samuel. Trabajando juntos requieren 15 días para construir una piscina. Encontrar el tiempo que requeriría cada uno si trabajara solo.

**34.** El propietario de una tienda acuerda el siguiente plan con un empleado: "trabajaré de lunes a sábado durante tres semanas. El primer día me paga un centavo, el segundo dos centavos y el tercero cuatro centavos; cada día me paga el doble del anterior". Encontrar la cantidad total que gana el empleado durante las tres semanas.

**35.** Ordenar los dígitos del 1 al 9, usando solo adición y sustracción, hasta completar 100. Por ejemplo:

```
 1 + 23 -  4 + 56 +  7 +  8 +  9 = 100
12 +  3 +  4 +  5 -  6 -  7 + 89 = 100
```

Imprimir todas las combinaciones posibles.

**36.** Un camión carguero completamente cargado lleva suficiente gasolina para recorrer medio desierto. Si el camión puede regresar al punto de partida cuando sea necesario, y puede dejar combustible oculto en cualquier punto del desierto, determinar la cantidad mínima de combustible requerida para cruzar todo el desierto.

**37.** Calcular la presión sanguínea sistólica de personas con edades 25, 35, 47, 51.5 y 60 años. Usar la fórmula:

$$P = 100 + \frac{A}{2}$$

donde $A$ representa la edad.

**38.** Calcular la altura $h$ (en metros) para $t$ segundos de un cuerpo lanzado verticalmente hacia arriba con velocidad inicial $r$ (en m/s):

$$h = rt - 4.9t^2$$

Usar $r = 10$ m/s y calcular $h$ para $t = 0$, $0.5$, $1.0$, $1.5$ y $2.0$ s.

**39.** Si dos ciudades están a 80 km una de otra y se conduce a 90 km/h, ¿cuántos minutos se necesitan para ir de una ciudad a la otra?

**40.** Una startup tecnológica en Tijuana proyecta su utilidad neta para los 8 años próximos mediante la fórmula:

$$p = t^3 - 5t^2 + 10t - 51$$

donde $p$ representa la utilidad (en miles de pesos mexicanos) y $t$ el tiempo en años. En $t = 0$, al momento de la inversión inicial, $p = -51$, es decir, el costo inicial es de \$51,000 MXN. Determinar la utilidad o pérdida acumulada año por año durante los 8 años, e indicar a partir de qué año la empresa comienza a ser rentable.

**41.** Un atleta lanza una pelota de fútbol, una de béisbol y una medicinal hacia arriba. La altura en metros respecto al tiempo en segundos se describe con las siguientes funciones cuadráticas ($g/2 \approx 4.9$ m/s²):

$$f(t) = -4.9t^2 + 13t + 2.5 \quad \text{(fútbol)}$$

$$b(t) = -4.9t^2 + 30t + 4.0 \quad \text{(béisbol)}$$

$$m(t) = -4.9t^2 + 0.5t + 0.6 \quad \text{(medicinal)}$$

Imprimir el tiempo $t$ (de 0 a 10 s, cada 0.5 s) y la altura de cada pelota. Detener la impresión cuando la pelota toque el suelo ($h \leq 0$).

**42.** Convertir un decimal periódico a fracción racional de la forma $M/N$, donde $M$ y $N$ sean enteros.

**43.** Probar un número para determinar si es primo. Imprimir `PRIMO` cuando lo sea y `NO PRIMO` cuando no lo sea.

**44.** Dados dos puntos $(x_1, y_1)$ y $(x_2, y_2)$ y un valor $x$ con $x_1 \leq x \leq x_2$, calcular el valor interpolado $y$ usando interpolación lineal:

$$y = y_1 + \frac{(x - x_1)(y_2 - y_1)}{x_2 - x_1}$$

Probar con los puntos $(2, 4)$ y $(8, 16)$ para $x = 3, 4, 5, 6, 7$. Verificar que los resultados caen sobre la recta que une ambos puntos.

**45.** Introducir varios valores de $A$ y $B$ para verificar la desigualdad triangular:

$$|A + B| \leq |A| + |B|$$

**46.** Resolver una ecuación de valor absoluto de la forma $|X - A| = B$, donde $A$ y $B$ son números reales.

**47.** Imprimir los elementos de la función $f(x) = |x|$ para $x = -8, -7, -6, \ldots, 7, 8$.

**48.** Evaluar la función $y = \dfrac{x^2 - 1}{x - 1}$ cuando $x$ toma valores enteros del 2 al 10 inclusive. ¿Qué observa? ¿Puede simplificarse la expresión?

**49.** Encontrar la forma general de la ecuación lineal dada por las coordenadas de dos puntos $(9, 7)$ y $(5, 4)$ sobre la línea.

**50.** Introducir la raíz real $R$. Determinar por sustitución si $R$ es una raíz de la ecuación cuadrática $Ax^2 + Bx + C = 0$.

**51.** Introducir un número real $x$. Si no es negativo, imprimir la raíz cuarta principal de $x$. Si es negativo, imprimir el mensaje `NINGUNA RAÍZ CUARTA REAL`.

**52.** Introducir $A$, $B$ y $C$ (números reales), coeficientes de la ecuación cuadrática $Ax^2 + Bx + C = 0$. Determinar si la ecuación tiene raíces reales. Imprimir uno de los mensajes: `RAÍCES REALES` o `NINGUNA RAÍZ REAL`.

**53.** Introducir los números reales $A$, $B$ y $C$, coeficientes de la ecuación cuadrática $Ax^2 + Bx + C = 0$. Determinar si la ecuación tiene una o más raíces reales. Si es así, calcularlas e imprimirlas.

**54.** Dado un punto $P(x, y)$, determinar la pareja ordenada del punto simétrico a $P$ respecto al eje $x$.

**55.** Encontrar dónde cruza al eje de las $x$ la recta representada por la ecuación $y = 4x + 3$.

**56.** Trazar la curva $y = x^2$ desde $x = -6$ hasta $x = 6$. Rotular las escalas horizontal y vertical.

**57.** Trazar la curva $y = 4x^2 - 5x + 2$, desde $x = -3$ hasta $x = 5$. Rotular las escalas horizontal y vertical.

**58.** Encontrar los ceros de la función cuadrática $f(x) = x^2 - 4x - 165$.

**59.** Encontrar el vértice de la función cuadrática $f(x) = 3x^2 + 18x + 7$.

**60.** Evaluar el polinomio $f(x) = 12x^2 + 6x + 8$ cuando $x$ toma valores desde 1 a 10, en saltos de 0.1.

**61.** Dada la ecuación lineal $AX + B = C$ ($A$, $B$ y $C$ son números reales), resolver para $X$. Por ejemplo, si la ecuación es $6X + 12 = 30$, imprimir $X = 3$.

**62.** Evaluar la función $y = 3x^2 + 4x - 1$ para $x$ entero en el dominio $-10 \leq x \leq 2$.

**63.** Encontrar todas las soluciones de $12x - 18y + 14 = 0$ para $x = 5, 10, 15, \ldots, 40$.

**64.** Encontrar todas las soluciones de $5x + y + 17 = 0$ para $x = -8, -2, -1.5, 2, 5, 6, 12, 15$.

**65.** Encontrar el vértice, eje de simetría y los ceros de la función cuadrática $f(x) = 3x^2 + 5x - 2$.

**66.** Factorizar un polinomio de la forma $x^2 + bx + c$.

**67.** Encontrar los ceros de la función $y = x - \sqrt{x}$.

**68.** Usar la fórmula cuadrática para resolver la ecuación $15x^2 - 23x - 4 = 0$.

**69.** Resolver la siguiente ecuación: $6x^2 - 17x + 5 = 0$.

**70.** Las dos raíces de una ecuación cuadrática $ax^2 + bx + c = 0$ pueden encontrarse con la fórmula:

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

Escribir un programa para encontrar e imprimir las raíces para coeficientes cualesquiera. Si $b^2 - 4ac < 0$, imprimir `DISCRIMINANTE NEGATIVO`.

**71.** Determinar si los enteros de $-10$ a $10$ son soluciones de $x^3 + 2x^2 + 75 = 0$.

**72.** Cada una de las siguientes ecuaciones tiene dos soluciones reales. Imprimir una tabla con los valores de $a$, $b$ y $c$; las dos soluciones; la suma de las soluciones y el producto de ellas:

$$\text{(a)}\ x^2 - 3x - 54 = 0 \qquad \text{(c)}\ 9x^2 + 45x - 18 = 0$$

$$\text{(b)}\ 2x^2 + x - 3 = 0 \qquad \text{(d)}\ 21x^2 + 11x - 2 = 0$$

**73.** La gráfica de $4x - y - 6 = 0$ intersecta al eje $y$ en el punto $(0, -6)$; a este punto se le llama la *intersección y* de la línea. La intersección $x$ es el punto donde la línea corta al eje $x$, siendo $(1.5,\ 0)$. Hacer un programa para encontrar las intersecciones $(x,\ y)$ de la línea representada por $6x - y + 43 = 0$.

**74.** Determinar las intersecciones $x$ e $y$ para la ecuación $4x + 3y = 6$.

**75.** Introducir las coordenadas de un punto y determinar si se encuentra sobre, arriba o abajo de la línea $y = x$. Probar con los puntos: $(1,1)$; $(3,4)$; $(-3,-4)$; $(-6,7)$; $(-5,5)$; $(-1,3)$.

**76.** Leer las coordenadas de un punto en el plano $xy$. Identificar el cuadrante donde se halla el punto, o si se encuentra sobre un eje, identificarlo.

**77.** Imprimir las ecuaciones de las rectas paralela y perpendicular a la recta $6x - 18y = 36$, que pasan por el punto $(-6,\ -2)$.

**78.** Determinar la ecuación de la recta que pasa por los puntos $(0,\ -2)$ y $(-68,\ -15)$.

**79.** Determinar la ecuación de la recta que pasa por los puntos $(56,\ 16)$ y $(-40,\ 1)$.

**80.** Determinar la ecuación de la recta con pendiente 3 que pasa por el punto $(8,\ -4)$.

**81.** Imprimir la pendiente de la recta con intersección $y$ en $(0,\ 10)$ y punto $(-3,\ 0)$.

**82.** Encontrar la pendiente y las intersecciones $(x,\ y)$ de la gráfica de $2x + 3y + 8 = 0$.

**83.** Determinar la pendiente y la intersección $y$ para cada una de las siguientes líneas:

$$\text{(a)}\ 3x + y = 4 \qquad \text{(b)}\ x - y = 2 \qquad \text{(c)}\ 5x - 3y = 15$$

**84.** Calcular la pendiente de una línea que pasa por dos puntos. Usar las siguientes parejas como datos de prueba:

$$\text{(a)}\ (-3,\ -5)\ \text{y}\ (0,\ -2) \qquad \text{(b)}\ (-4,\ 6)\ \text{y}\ (8,\ -3) \qquad \text{(c)}\ (3,\ -5)\ \text{y}\ (3,\ 0)$$

**85.** Encontrar la pendiente de la línea que pasa por dos puntos dados. Incluir la posibilidad de que la pendiente sea indefinida (línea vertical).

**86.** Escribir un programa para introducir cuatro números; imprimir el inverso aditivo de cada uno, la suma de los cuatro y el inverso aditivo de la suma.

**87.** Un faro se localiza en las coordenadas $(7.64,\ 12.12)$. Un bote, localizado inicialmente en $(2.00,\ 0.35)$, se mueve en línea recta hacia el faro. Después de un minuto, la posición del bote es $(3.37,\ 1.87)$. Determinar las coordenadas $(x,\ y)$ sobre la trayectoria del bote cuando la distancia de éste al faro es mínima (con dos cifras decimales).

**88.** Introducir dos parejas de coordenadas. Encontrar la pendiente y la intersección $y$ de la recta que las contiene e imprimir los resultados como números racionales en su mínima expresión.

**89.** Introducir dos parejas ordenadas e imprimir la ecuación de la mediatriz perpendicular del segmento determinado por esos puntos.

**90.** Introducir $A$, $B$ y $C$ para la parábola $y = Ax^2 + Bx + C$ ($A \neq 0$). Calcular la ecuación de la directriz y las coordenadas del foco.

**91.** Escribir un programa que trace la gráfica de la ecuación de la recta $y = mx + b$.

**92.** Escribir un programa que calcule el rango para un dominio y grafique la función $y = x^2 + 14x - 1$.

**93.** Escribir un programa para graficar una parte de la función $y = 0.1x^2 - 0.2x$.

**94.** Encontrar la ecuación de la mediatriz perpendicular del segmento de recta cuyos extremos son $(2,\ 3)$ y $(2,\ 9)$.

**95.** Encontrar la distancia desde la recta $x + 2y + 3 = 0$ al punto $(4,\ 5)$.

**96.** Encontrar las coordenadas $(X,\ Y)$ del punto que divide un segmento en una razón dada. Por ejemplo, encontrar el punto que divide al segmento con extremos $(0,\ -2)$ y $(3,\ 7)$ en la razón $1:2$.

**97.** La función entera máxima se denota $f(x) = \lfloor x \rfloor$. Asocia a cada número real $x$ con el entero más grande que no exceda a $x$. Encontrar el valor de $\lfloor x \rfloor$ dado un argumento positivo, negativo o cero.

**98.** Introducir los enteros positivos $A$ y $B$ y determinar el cociente y el residuo cuando $A$ se divide entre $B$.

**99.** Calcular e imprimir el determinante de una matriz $2 \times 2$.

**100.** Evaluar el determinante de segundo orden:

$$|A| = (7)(-73.3) - (5)(42)$$

**101.** Escribir un programa que utilice división sintética para encontrar el cociente y el residuo cuando un polinomio se divide entre un factor lineal de la forma $(x - a)$.

**102.** Escribir un programa general que realice división sintética para cualquier polinomio y cualquier factor lineal.

**103.** Se dan dos ecuaciones:

$$4x + 5y = 17 \qquad 3x + 6y = 22$$

Encontrar los valores de $x$ e $y$.

**104.** Introducir los coeficientes para el sistema de ecuaciones lineales $Ax + By = C$ y $Dx + Ey = F$. Determinar si las gráficas se intersecan. Si es así, ¿lo hacen en un punto o en infinitos puntos?

**105.** Leer los coeficientes para el sistema de ecuaciones lineales $Ax + By = C$ y $Dx + Ey = F$. Determinar si las gráficas de las ecuaciones son perpendiculares.

**106.** Introducir los coeficientes para el sistema $Ax + By = C$ y $Dx + Ey = F$. Determinar si las ecuaciones son consistentes o inconsistentes, y dependientes o independientes.

**107.** Imprimir si las siguientes ecuaciones lineales tienen la misma gráfica:

$$y = 7x + 9 \qquad 3y - 21x = 12$$

**108.** Imprimir si las líneas determinadas por:

$$y = 5x + 19 \qquad y = -4x - 19$$

son perpendiculares.

**109.** Imprimir si las gráficas de las dos ecuaciones siguientes representan la misma recta, rectas paralelas o rectas que se intersecan en un punto:

$$5x + y = 12 \qquad 2y = -10x + 24$$

**110.** Resolver el siguiente sistema de ecuaciones:

$$3x + 4y - 6 = 0 \qquad 2x + 3y = 0$$

**111.** Resolver el sistema de ecuaciones lineales:

$$109x + 71y - 260 = 0$$

$$-89x + 29y + 18 = 0$$

**112.** Resolver el siguiente sistema de ecuaciones:

$$3x - 5y - 2z - 5 = 0$$

$$-5x + 2y + 3z - 12 = 0$$

$$2x + y - 5 = 0$$

**113.** Resolver el siguiente sistema de ecuaciones lineales:

$$2x + 4y - 5z - 3 = 0$$

$$3x - 2y - 2z + 14 = 0$$

$$-4x + 5y + 3z + 10 = 0$$

**114.** Escribir un programa que resuelva el siguiente sistema y encuentre todos los pares $(x, y)$ que lo satisfacen para $x = 2, 4, 6, 8, \ldots, 50$:

$$x + 6y + 1 = 0$$

$$2x - y + 5 = 0$$

**115.** Encontrar el centro y radio de la circunferencia dada por la ecuación cónica $x^2 + y^2 - 144 = 0$.

**116.** Encontrar el centro y radio de la circunferencia dada por $x^2 + y^2 + 2x + 4y - 20 = 0$.

**117.** Encontrar el término enésimo y la suma de los $N$ primeros términos de una progresión aritmética. Usar:

$$L = A + (N-1)D \qquad S = \frac{N}{2}(A + L)$$

Probar con $A = 1$, $N = 20$ y $D = 3$.

**118.** Encontrar la suma de la serie aritmética:

$$A + (A+D) + (A+2D) + \cdots + (A+(N-1)D)$$

para valores dados de $A$, $D$ y $N$.

**119.** Determinar la suma de la serie $1 + 2 + 4 + 8 + 16 + \cdots + 2^n$ para cualquier valor entero positivo de $n$.

**120.** Encontrar la suma de la serie geométrica:

$$A + AR + AR^2 + \cdots + AR^{N-1}$$

para valores de $A$, $R$ y $N$.

**121.** Calcular la suma de los primeros 120 términos de la serie aritmética $1 + 2 + 3 + \cdots + n$ usando la fórmula:

$$S = \frac{n(n+1)}{2}$$

**122.** Introducir los 30 elementos de un arreglo $A$. Intercambiar las siguientes posiciones: $A[2]$ con $A[16]$; $A[5]$ con $A[25]$; $A[26]$ con $A[12]$. Imprimir el arreglo antes y después.

**123.** Calcular la suma, diferencia, producto y cociente de parejas de números complejos $a + bi$ y $c + di$ introducidos como datos. Recordar que:

$$(a+bi)(c+di) = (ac-bd) + (ad+bc)i$$

$$\frac{a+bi}{c+di} = \frac{ac+bd}{c^2+d^2} + \frac{bc-ad}{c^2+d^2}\,i$$

---

## Problemas adicionales

> *Problemas de elaboración propia, inspirados en el capítulo.*

**124.** Implementar el algoritmo de Euclides para calcular el MCD de dos enteros positivos $a$ y $b$:

$$\gcd(a, b) = \gcd(b,\ a \bmod b)$$

Verificar con los pares: (252, 105), (1071, 462), (100, 75).

**125.** Dado un polinomio $p(x) = a_n x^n + a_{n-1}x^{n-1} + \cdots + a_1 x + a_0$, evaluar $p(x)$ usando el método de Horner:

$$p(x) = (\cdots((a_n \cdot x + a_{n-1})\cdot x + a_{n-2})\cdots)\cdot x + a_0$$

Comparar el número de multiplicaciones con la evaluación directa.

**126.** Resolver un sistema $3 \times 3$ de ecuaciones lineales $Ax = b$ usando la regla de Cramer. Imprimir el determinante de la matriz $A$ y la solución $(x_1, x_2, x_3)$.

**127.** Generar la tabla de multiplicar para números complejos de la forma $a + bi$ donde $a, b \in \{-1, 0, 1\}$. Identificar las unidades imaginarias $i$, $-i$, $1$, $-1$.

**128.** Una función cuadrática $f(x) = ax^2 + bx + c$ define una parábola. Dado $a$, $b$ y $c$, imprimir:
- Coordenadas del vértice: $\left(-\dfrac{b}{2a},\ f\!\left(-\dfrac{b}{2a}\right)\right)$
- Ecuación del eje de simetría: $x = -\dfrac{b}{2a}$
- Ceros reales (si existen)
- Si la parábola abre hacia arriba o hacia abajo

**129.** Calcular la suma de la serie armónica hasta que el término $\dfrac{1}{n}$ sea menor que $10^{-6}$:

$$H_n = 1 + \frac{1}{2} + \frac{1}{3} + \cdots + \frac{1}{n}$$

¿Cuántos términos se necesitan?

**130.** Dado el coeficiente de correlación de Pearson entre dos conjuntos de datos $X$ e $Y$ de $N$ elementos:

$$r = \frac{N\sum x_i y_i - \sum x_i \sum y_i}{\sqrt{\left(N\sum x_i^2 - (\sum x_i)^2\right)\left(N\sum y_i^2 - (\sum y_i)^2\right)}}$$

Calcular $r$ para los datos: $X = \{2, 4, 6, 8, 10\}$, $Y = \{1, 3, 5, 7, 9\}$.
