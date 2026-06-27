# Capítulo 7: Teoría de los Números

> *Basado en el libro de Donald D. Spencer, Editorial Limusa, 1985*

## Introducción

La teoría de números es una rama de las Matemáticas que trata con los números naturales 1, 2, 3, 4, ... llamados a menudo enteros positivos. La arqueología y la historia nos enseñan que el hombre comenzó a contar tempranamente. Aprendió a contar números y mucho tiempo después a multiplicarlos y restarlos. La división por números fue necesaria para partir igualmente un montón de peras o una cantidad de peces. Estas operaciones con los números se denominan cálculos. La palabra *cálculo* proviene del latín *calculus*, que significa piedrecilla. Los romanos acostumbraban usar guijarros para designar números en sus mesas de cálculo. Tan pronto como el hombre aprendió a calcular un poco, para muchos con mente especulativa resultó un pasatiempo agradable. Esas experiencias con números se acumularon por siglos con interés diverso, hasta que, por decirlo así, se dispuso de una estructura imponente en Matemáticas, llamada teoría de los números. Si es usted un entusiasta de los acertijos, recuerda probablemente algunos cuyo interés radica en las propiedades de los números; si ha resuelto algunos, usted está ya iniciado en algunos de los elementos de la teoría de números.

En la actualidad, la teoría de números tiene aplicaciones directas en la criptografía moderna: los algoritmos RSA —que protegen las comunicaciones HTTPS en internet— se basan en la dificultad de factorizar números primos muy grandes. Esto convierte los problemas de este capítulo en algo más que acertijos: son la base matemática de la seguridad digital.

## Problemas

**1.** Introducir un número y determinar si se trata de un primo.

**2.** Introducir un número $N$ y enlistar a continuación todos los números primos menores o iguales a él.

**3.** Imprimir los números primos del 1000 al 1500. El programa no deberá probar los números pares.

**4.** El año 1973 lo recordarán muchos aficionados a la Matemática, pues se trata de un número primo. Generar todos los números primos en el período 1972–2030 e imprimir cuáles años de ese rango son primos.

**5.** Calcular e imprimir todos los pares de primos gemelos (tales como 11 y 13, 17 y 19) menores que 1000. Dos primos gemelos son primos consecutivos que difieren en 2.

**6.** Calcular e imprimir una tabla que dé el número y el porcentaje de números primos en los intervalos 2–100, 101–200, 201–300, 301–400, 401–500, 501–600, 601–700, 701–800, 801–900 y 901–1000.

**7.** Enlistar todos los números compuestos entre 4 y 100. Un número compuesto es cualquier entero diferente de 1 que no sea primo.

**8.** Introducir dos números $A$ y $B$ y determinar si son primos relativamente. Dos números son primos relativamente si su máximo común divisor es 1. Por ejemplo, 4 y 15 son primos relativamente.

**9.** Introducir tres enteros $A$, $B$ y $C$ y determinar si son primos relativamente.

**10.** Determinar si un conjunto de $N$ enteros positivos son primos relativamente.

**11.** Usar la fórmula $3N^2 - 3N + 23$ para construir una tabla de números primos. Variar $N$ de 0 a 22.

**12.** Imprimir una tabla de números primos usando el polinomio de Euler:

$P = N^2 - N + 41$

para $N = 1, 2, 3, \ldots, 40$. Verificar que todos los valores generados son primos y determinar para qué valor de $N$ el polinomio falla por primera vez.

**13.** La fórmula $Y_N = N^2 - 79N + 1601$ puede usarse para generar primos dentro de un rango limitado. Determinar para cada valor $N = 1, 2, 3, \ldots, 100$ si $Y_N$ es un número primo o no lo es.

**14.** Un número primo palíndromo es uno que también es primo cuando se invierten sus dígitos. 17, 31, 37 y 113 son ejemplos de tales números. Encontrar todos los primos palíndromos menores que 400.

**15.** Es posible encontrar progresiones aritméticas de números primos no consecutivos. Por ejemplo, una progresión aritmética de tres primos es 11, 17, 23 (diferencia constante igual a 6). Examinar todos los primos menores que 1000 e imprimir cualquier progresión aritmética de tres o cuatro primos.

**16.** Los números primos de Mersenne son de la forma $2^p - 1$, donde $p$ es primo. Para cada primo de Mersenne existe un número perfecto correspondiente:

$2^{p-1}(2^p - 1)$

Encontrar varios primos de Mersenne y los números perfectos correspondientes.

**17.** Fermat, probablemente el más grande matemático francés del siglo XVII, propuso que todos los números de la forma $2^{2^n} + 1$, donde $n = 0, 1, 2, \ldots$, son primos. Demostrar que esto es cierto para $n = 1, 2, 3, 4$, pero no para $n = 5$.

**18.** Se ha conjeturado que existe una gran cantidad de números primos de la forma $n^n + 1$. Por ejemplo, $1^1 + 1 = 2$ (un primo) y $2^2 + 1 = 5$ (un primo). Determinar para cada valor $n = 1, 2, \ldots, 7$ si $n^n + 1$ es o no primo.

**19.** Si $p$ es un primo y $p^2 + 2$ también lo es, encontrar un caso en que $p^2 + 4$ lo sea también.

**20.** Algunos números primos pueden expresarse en la forma $n! + 1$. De hecho, se ha conjeturado que existe un número infinito de primos de esa forma. Determinar qué números primos (menores que 2000) pueden expresarse como $n! + 1$.

**21.** En el siglo XIII, Leonardo Fibonacci, un próspero mercader de Italia a quien le fascinaban los números, descubrió lo que se conoce ahora como la serie numérica de Fibonacci. Cada número de esta serie es la suma de los dos números que lo preceden inmediatamente. Los primeros términos de la secuencia son:

$1,\; 1,\; 2,\; 3,\; 5,\; 8,\; 13,\; 21,\; 34,\; 55,\; 89,\; 144,\; \ldots$

Encontrar los primeros treinta números en esta secuencia. Calcular también la razón $F_{n+1}/F_n$ entre términos consecutivos e imprimir cómo converge al número áureo $\varphi \approx 1.618033\ldots$

**22.** Supóngase que se juntan dos conejos, macho y hembra, para cruzarse. Supóngase que una pareja de conejos procrea otra cada mes, comenzando dos meses después de su propio nacimiento, y que cada pareja producida así consiste en un macho y una hembra. ¿Cuántos conejos habrá al cabo de 24 meses?

**23.** Encontrar el primer término de la serie de Fibonacci mayor que 10000. Solo este término se imprimirá con el programa.

**24.** Imprimir los primeros cincuenta números de Lucas. Los números de Lucas son similares a los de Fibonacci, aunque la secuencia principia diferentemente: 1, 3, 4, 7, 11, 18, 29, 47, 76, ...

**25.** Un número perfecto es un entero tal que la suma de sus divisores propios es igual a él mismo. Por ejemplo, 6 es un número perfecto, pues $1 + 2 + 3 = 6$. Ver cuántos números perfectos pueden encontrarse.

**26.** Determinar si un número dado es perfecto, abundante o deficiente. Un número es perfecto cuando la suma de sus divisores propios es igual a él; es abundante cuando esa suma lo excede, y es deficiente cuando es menor que él.

**27.** Algunas parejas de números se llaman "números amigables" si la suma de los factores propios de uno de ellos es igual al otro. Por ejemplo, 220 y 284 son números amigables, pues la suma de los factores propios de 220 es 284 y la de los factores propios de 284 es 220. Los factores propios de 220 son: 1, 2, 4, 5, 10, 11, 20, 22, 44, 55, 110 (suma = 284). Los factores propios de 284 son: 1, 2, 4, 71, 142 (suma = 220). Encontrar todas las parejas de números amigables menores que 10000.

**28.** Un número con $N$ dígitos es un número de Armstrong si la suma de las potencias $N$-ésimas de los dígitos que lo forman es igual al propio número. Por ejemplo, 407 es un número de Armstrong, pues tiene tres dígitos tales que:

$4^3 + 0^3 + 7^3 = 407$

Determinar todos los números de Armstrong con tres dígitos.

**29.** El antiguo matemático griego Diofante se considera uno de los genios precursores de la teoría de los números. Una ecuación encontrada en sus escritos establece: "Encontrar tres números tales que su suma sea un cuadrado perfecto y que la suma de dos cualesquiera de ellos también lo sea". Determinar tres números así.

**30.** Generar e imprimir las primeras quince filas del triángulo de Pascal, en distribución tabular centrada.

**31.** Sea la tabla:

```
1    1    1
1    2    3    2    1
1    3    6    7    6    3    1
1    4   10   16   19   16   10    4    1
```

Cada elemento (excepto los de la primera fila y los extremos de cada fila) es la suma del elemento directamente arriba y sus dos vecinos inmediatos en esa misma fila superior. Utilizar esta regla para calcular las siguientes diez líneas de la tabla.

**32.** Un cuadrado latino es una distribución tabular de $N \times N$ números, de tal manera que cada número aparezca exactamente una vez en cada fila y en cada columna. Imprimir todos los cuadrados latinos de orden $N$ para $N = 2, 3, \ldots, 9$. Ejemplo para $N = 5$:

```
1 2 3 4 5
2 3 4 5 1
3 4 5 1 2
4 5 1 2 3
5 1 2 3 4
```

**33.** Existen tres enteros menores que 10000 que son iguales a la suma de sus dígitos elevados a la cuarta potencia. Un ejemplo es el número 1634:

$1634 = 1^4 + 6^4 + 3^4 + 4^4$

Encontrar los otros dos enteros.

**34.** Encontrar el máximo común divisor (MCD) de tres números. El MCD es el número más grande que divide a los tres números. Por ejemplo, el MCD de 3, 12 y 30 es 3.

**35.** Utilizar el algoritmo de Euclides para determinar el MCD de dos enteros positivos.

**36.** De las $N^2$ posibles parejas de enteros entre 1 y $N$, contar el número de parejas cuyo MCD sea 1.

**37.** Encontrar el mínimo común múltiplo (MCM) de tres números.

**38.** Encontrar el mínimo común múltiplo de cinco números.

**39.** Determinar el MCD y el MCM de los siguientes conjuntos de números: 324 y 610; 200 y 316; 84 y 1003.

**40.** Determinar todas las diferentes parejas de factores del siguiente conjunto de enteros: 1009, −854, 453, −991, 771, 991.

**41.** Introducir el número $N$ y enlistar sus factores primos. Por ejemplo, los factores primos de 12 son 2, 2 y 3.

**42.** Determinar el número menor que 2000 que tenga el mayor número de factores.

**43.** Determinar el entero menor que tenga exactamente 32 factores.

**44.** Encontrar la suma y el número de factores de 1134, 1135, 1136, ..., 1174.

**45.** Dividir 1000 en dos partes de tal manera que una sea múltiplo de 19 y la otra sea múltiplo de 47.

**46.** Redactar un programa para un juego en que cada jugador introduce un número de 7 dígitos. El programa extrae automáticamente el factor primo mayor de cada número, muestra ambos factores e indica el ganador. Jugar 3 rondas y mostrar la puntuación final.

**47.** Encontrar todos los valores de $N$ menores que 100 para los cuales el número triangular:

$T_N = \frac{N(N+1)}{2}$

sea un cuadrado perfecto.

**48.** La suma de los primeros cinco enteros es igual a 15: $1 + 2 + 3 + 4 + 5 = 15$. ¿Cuántos enteros, comenzando con $1 + 2 + 3 + 4 + \cdots$, tendrían que agregarse para alcanzar una suma de 820?

**49.** Determinar el valor del dígito $X$ (del 0 al 9) de tal manera que el número de cinco dígitos $X30X8$ sea divisible entre 23.

**50.** Platón, maestro ateniense y discípulo de Sócrates, recomendó que una ciudad se dividiera en lotes cuyo número tuviera tantos divisores propios como fuera posible. Sugirió 5040, pues este número posee 59 divisores propios. Sin embargo, existen dos números menores que 10000 que tienen 63 divisores propios. Uno de ellos es 9240. ¿Cuál es el otro?

**51.** Dada la secuencia 1, 2, 4, 5, 7, 8, 10, 11, 13, 14, ... donde falta cada tercer entero, imprimir sus primeros cien términos y la suma acumulada.

**52.** Los números 12 y 13 tienen la siguiente característica: $12^2 = 144$ y $21^2 = 441$ (que es el inverso de 144); $13^2 = 169$ y $31^2 = 961$ (que es el inverso de 169). Encontrar un número de tres dígitos, si existe, para el cual sea también válido este tipo de relación.

**53.** Aquí se tiene una curiosidad matemática en base 10: $98765432 \times 9 = 888888888$. Encontrar curiosidades semejantes en bases menores que 10.

**54.** ¿Qué entero multiplicado por 52631578947368421 dará solo nueves?

**55.** Encontrar un número de cinco dígitos que al multiplicarse por 4 le inviertan sus dígitos. En otras palabras, encontrar un número $ABCDE$ tal que $4 \times ABCDE = EDCBA$.

**56.** A los números que puedan representar un patrón triangular de puntos se les llama números triangulares:

$T_n = \frac{n(n+1)}{2}$

A los que puedan representar un patrón cuadrado de puntos se les denomina números cuadrados:

$Q_n = n^2$

Encontrar si existen números que sean a la vez triangulares y cuadrados.

**57.** Encontrar enteros positivos distintos $W$, $X$, $Y$ y $Z$, cada uno menor que 15, tales que:

$W^3 + X^3 = Y^3 + Z^3$

**58.** Dado un número de tres dígitos, restarle el número de tres dígitos "invertido" e imprimir el resultado. Por ejemplo, 632 daría el resultado $632 - 236 = 396$.

**59.** Encontrar aquellos enteros $C$, de 1 a 50, que puedan escribirse en la forma:

$C^2 = A^2 + B^2$

con enteros positivos $A$ y $B$.

**60.** El cuadrado de 5 es 25 y 5 es el último dígito de 25. El cuadrado de 90625 es 8212890625 y 90625 son los cinco últimos dígitos de 8212890625. Encontrar más números, menores que 1000, que sean el último dígito o los últimos dígitos de su cuadrado.

**61.** La suma de los primeros dos dígitos del entero 3025 y los dos últimos dígitos es 55. Si se eleva al cuadrado 55 se obtiene el número original:

$30 + 25 = 55$

$55^2 = 3025$

Determinar todos los números menores que 10000 con esta propiedad.

**62.** Los tres números consecutivos 72, 73 y 74 son únicos, pues cada uno es igual a la suma de dos cuadrados:

$72 = 6^2 + 6^2$

$73 = 3^2 + 8^2$

$74 = 5^2 + 7^2$

Determinar todos los conjuntos similares de tres números consecutivos menores que 1000.

**63.** El número 20 puede escribirse como la suma de dos cuadrados: $20 = 2^2 + 4^2$. Determinar todos los números menores que 100 que puedan escribirse como la suma de dos cuadrados.

**64.** Encontrar todos los enteros de dos dígitos iguales a la suma de los cuadrados de sus dígitos.

**65.** Cuatro y nueve se llaman números cuadrados, pues $2^2 = 4$ y $3^2 = 9$. Ciertas parejas de números, cuando se suman o se restan, dan un número cuadrado. Por ejemplo, 12 y 37: $12 + 37 = 49$ y $37 - 12 = 25$. Determinar todas las parejas de números menores que 80 que den un número cuadrado cuando se sumen y cuando se resten.

**66.** El matemático inglés G. H. Hardy abordó en una ocasión un taxi para visitar a su amigo el matemático hindú Srinivasa Ramanujan. El número del taxi le parecía insulso, pero Ramanujan señaló que "se trata del número más pequeño expresable como la suma de dos cubos en dos maneras diferentes":

$A^3 + B^3 = X^3 + Y^3$

Determinar el número del taxi.

**67.** Para cada una de las siguientes parejas de números, encontrar dos números cuya suma sea el primero y cuyo producto sea el segundo: 42 y 392; 75 y 756; 94 y 840; 296 y 17679.

**68.** Con los enteros del uno al nueve, tomados de tres en tres, ¿de cuántas formas puede obtenerse una suma de 15?

**69.** Demostrar que la suma de los cuadrados de cinco enteros consecutivos es siempre divisible entre 5.

**70.** Introducir un entero $N$ y determinar si se trata de un cuadrado perfecto.

**71.** La suma de los cuadrados de los $N$ primeros números está dada por la fórmula:

$S = \frac{N(N+1)(2N+1)}{6}$

Con esta fórmula, calcular la suma de los cuadrados de los primeros 150 enteros.

**72.** Encontrar todos los números naturales pares entre 100 y 150 que sean iguales a la mitad de la suma de sus divisores propios.

**73.** Encontrar los tres primeros números impares positivos que puedan expresarse como la suma de dos cuadrados perfectos de enteros positivos en dos formas distintas.

**74.** Encontrar los números $A$, $B$ y $C$ cuya suma sea 43 y la suma de sus cubos sea 17299.

**75.** Encontrar los enteros positivos cuya suma sea 20 y cuyo producto sea máximo.

**76.** Paradójicamente, pueden reducirse ciertas fracciones eliminando un dígito común en el numerador y en el denominador. Por ejemplo: $16/64 = 1/4$ (cancelando el 6) y $154/253 = 14/23$ (cancelando el 5). Encontrar todas las fracciones con esta propiedad hasta 998/999.

**77.** Para cada entero del 1 al 40, encontrar el cuadrado mínimo que principie con los dígitos de ese entero.

**78.** Un entero $X$, al dividirse entre los números del 2 al 12, deja siempre un residuo de 1, y además es divisible entre 13. Determinar el entero menor que se ajuste a esta descripción.

**79.** Un cierto número, menos la suma de sus dígitos, es igual a 36. Además, la suma de sus dígitos más el producto de ellos es igual al número menos 8. Determinar ese número.

**80.** Encontrar una secuencia de siete enteros consecutivos en la que ninguno sea primo.

**81.** Encontrar los cuadrados de todos los enteros hasta el 100 cuyos dígitos de las decenas sean impares.

**82.** Determinar la suma de todos los enteros entre 100 y 1000 que sean divisibles entre 14.

**83.** Imprimir todos los números hasta el 1000 que no sean divisibles entre ningún entero del 2 al 9.

---

## Problemas adicionales

> *Problemas de elaboración propia, inspirados en el capítulo.*

**84.** La conjetura de Goldbach afirma que todo número par mayor que 2 puede expresarse como la suma de dos números primos. Verificar esta conjetura para todos los números pares entre 4 y 200, e imprimir para cada uno al menos un par de primos que sumen el número dado.

**85.** La conjetura de Collatz: dado un entero positivo $n$, si $n$ es par se divide entre 2; si es impar se multiplica por 3 y se suma 1; se repite el proceso con el resultado. La conjetura afirma que el proceso siempre termina en 1. Aplicar el proceso para $n = 1, 2, \ldots, 50$ e imprimir la longitud de cada secuencia.

**86.** La función totiente de Euler $\varphi(n)$ cuenta los enteros positivos hasta $n$ que son coprimos con $n$. Por ejemplo, $\varphi(6) = 2$ porque solo 1 y 5 son coprimos con 6. Calcular $\varphi(n)$ para $n = 1, 2, \ldots, 50$.

**87.** Los números de Catalan aparecen en numerosos problemas combinatorios. El $n$-ésimo número de Catalan es:

$C_n = \frac{(2n)!}{(n+1)!\; n!}$

Imprimir los primeros 15 números de Catalan.

**88.** El proceso de Kaprekar: tomar cualquier número de 4 dígitos (no todos iguales), formar el mayor número posible con sus dígitos y también el menor, y restar el menor del mayor. Repetir con el resultado. Demostrar que el proceso siempre llega al número 6174 (constante de Kaprekar). Aplicar el proceso a los números 1234, 5678 y 9981 e imprimir cada secuencia.

**89.** Un número feliz se define así: tomar la suma de los cuadrados de sus dígitos y repetir el proceso con el resultado; si se llega a 1, el número es feliz. Si el proceso cae en el ciclo $4 \to 16 \to 37 \to 58 \to 89 \to 145 \to 42 \to 20 \to 4$, el número es triste. Encontrar todos los números felices del 1 al 100.

**90.** Un número de $N$ dígitos es un número de Keith si aparece en la secuencia de recurrencia que comienza con sus propios dígitos y donde cada término es la suma de los $N$ anteriores. Por ejemplo, 14 es un número de Keith pues la secuencia $1, 4, 5, 9, 14$ lo contiene. Encontrar todos los números de Keith de dos dígitos.

**91.** Generar todos los números de 6 dígitos que usen cada uno de los dígitos del 1 al 6 exactamente una vez y sean divisibles entre 6. ¿Cuántos existen en total?

**92.** El proceso "sumar y voltear" consiste en sumar un número con el número formado por sus dígitos en orden inverso; repetir el proceso hasta obtener un palíndromo. Aplicar este proceso a todos los enteros del 1 al 100 e imprimir cuántos pasos necesita cada uno para llegar a un palíndromo.
