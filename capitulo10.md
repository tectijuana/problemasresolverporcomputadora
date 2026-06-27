# Capítulo 10: Diversión con la Computadora

> *Basado en el libro de Donald D. Spencer, Editorial Limusa, 1985*

## Introducción

Hasta que se inventó la computadora, jugar estuvo restringido primordialmente a los humanos o a ciertas máquinas de propósitos lúdicos. Hoy, en 2026, los videojuegos son una industria global que supera al cine y a la música juntos, y millones de programadores comenzaron su carrera escribiendo juegos simples en casa. Los juegos son excelentes vehículos para aprender a programar: el problema a resolver es inmediatamente comprensible, la retroalimentación es instantánea y la motivación natural. Desde los juegos de dados y cartas hasta los autómatas celulares y laberintos, cada programa de juego enseña conceptos fundamentales: números aleatorios, estructuras de datos, búsqueda exhaustiva, recursividad e inteligencia artificial básica. En este capítulo se encontrarán juegos, rompecabezas y entretenimientos matemáticos que pueden programarse para jugar con una computadora, y que sirven de trampolín hacia el desarrollo de videojuegos más ambiciosos.

## Problemas

**1.** Escribir un programa que simule el lanzamiento de dos dados.

**2.** Sacar al azar cinco cartas de una baraja de 52 e imprimir el valor y palo de cada carta.

**3.** Distribuir y analizar una mano de póquer.

**4.** Programar la computadora para que "dibuje" un cuadro o figura geométrica en la pantalla usando caracteres ASCII. Probar con al menos tres figuras: un triángulo, un rombo y una figura libre.

**5.** La computadora trata de adivinar un número que tiene usted en mente. Primero, ella propone un número y usted le dice si es demasiado alto, demasiado bajo o correcto. En base a la información que se le proporcione, la computadora ensaya de nuevo. El proceso continúa hasta que la computadora acierta el número. Generar un programa que desarrolle este juego de tanteos.

**6.** Correr un programa que pida a dos jugadores que adivinen un número que la computadora saque al azar entre 1 y 75. El programa dará 15 puntos al jugador que dé la respuesta más próxima.

**7.** Colocar cinco monedas en cinco cuadros, de tal suerte que no haya ningún par en la misma fila, columna o a lo largo de una diagonal.

**8.** Simular 100 veces un juego entre Tomás y Laura, teniendo ambos \$10 cada uno. Se lanza una moneda. Si cae águila, Tomás gana \$1 de Laura; si cae sol, Laura gana \$1 de Tomás. En promedio, ¿cuántas veces habrá que arrojar la moneda antes de que Tomás (o Laura) pierda todo su dinero?

**9.** Introducir el número de paradas que Juan López hace con cada balón en cada marco y calcular su registro de juego de boliche.

**10.** Resolver el siguiente problema de criptaritmética: sustituir cada letra por un dígito único (0–9) de manera que la suma sea correcta:

```
  MEDIO
+ MEDIO
-------
  TOTAL
```

**11.** Santiago va a la feria con su mascota que es una zorra, un costal de maíz y un ganso de engorda. Llega a un puente peatonal que permite solo que pase con una de sus pertenencias a la vez. Si dejara solo al ganso con el maíz, el animal se lo comería; si dejara sola a la zorra con el ganso, se lo comería. ¿Cómo debe proceder para pasarlos sin problemas al otro lado del río?

**12.** ¿Cree usted que pueda usarse una computadora para resolver un problema de lógica recreativa como el que sigue? Si así lo considera, escriba el programa correspondiente.

> Mientras el censador entrevistaba a un habitante de una pequeña comunidad, este señaló a una persona que descansaba cerca y dijo: "No tengo ni hermanas ni hermanos, pero el padre de esa persona es el hijo de mi padre". El objetivo del acertijo es determinar quién era la persona señalada.

**13.** Tres marineros náufragos en una isla desierta con un mono, reunieron en un día un montón de cocos para repartirlos al día siguiente. En la noche, uno de los marineros se levantó, dividió el montón en tres partes iguales y vio que sobraba un coco que le dio al mono, escondiendo enseguida su parte. Un poco después, otro marinero hizo lo mismo y luego el último repitió la operación fraudulenta. Por la mañana, los marineros partieron la pila restante y encontraron que sobraba un coco que le dieron al mono. Calcular cuántos cocos había en la pila original. Como hay más de una respuesta correcta, el programa considerará pilas de cocos solo en el rango de 1 a 1000. Una de las respuestas es 79 y puede usarse para verificar el programa.

**14.** ¿Cuántas reinas de ajedrez se requieren para cubrir un tablero? (Se dice que un tablero está cubierto cuando cada cuadrado se encuentra ocupado o amenazado.) Está demostrado que cuatro reinas cubren un tablero de 6 × 6. Determinar mediante una búsqueda exhaustiva si tres reinas lo cubren o no.

**15.** Se desarrolla un juego tirando un dado. Si sale un número par (2, 4, 6) el jugador recibe una cantidad igual al número que salió. Si el número es impar, pierde una cantidad igual al número que salió. Simular este juego en una computadora.

**16.** Generar un programa que distribuya una mano de *bridge* y haga enseguida una apuesta de apertura.

**17.** Pueden distribuirse diez manos de póquer de cinco cartas, cada una tomada de una baraja de 52 cartas. Simular este proceso algunas centenas de veces; encontrar y sacar el mínimo de manos de póquer que aparecen con cuatro de una clase, casa llena, una tercia, dos pares y un solo par.

**18.** Simular 10 manos de un juego de dos personas llamado "cinco cartas tapadas". El juego se realiza con una baraja común de 52 cartas. Los ases son altos y los doses bajos. Las combinaciones ganadoras son: pares, tercias y cuatro de una clase. Si ningún jugador tiene un par o algo mejor, gana la carta más alta. Si hay empate, se regresa la apuesta. Cada jugador pone \$50 de apuesta. El programa distribuirá 5 cartas a cada jugador, comparará las manos y tabulará lo ganado o perdido por cada jugador.

**19.** El juego de los dados de póquer utiliza cinco dados, cada uno marcado del as al nueve. El objeto del juego es tirar los dados y hacer la mejor mano de póquer, en una, dos o tres tiradas. El jugador arroja los cinco dados, puede separar los que desea conservar y volver a lanzar los restantes hasta un máximo de tres tiradas. Se registra la mejor mano y gana el jugador con la mano más alta. Simular este juego en una computadora.

**20.** El juego "Arriba y abajo del 7" se juega con dos dados. Los jugadores apuestan a que el total quede arriba, abajo o sea exactamente igual a siete. Una apuesta *arriba de 7* gana cuando la suma de los dados es 8, 9, 10, 11 o 12; una apuesta *abajo de 7* gana si el total es 2, 3, 4, 5 o 6; ambas se pagan a razón igual (1 a 1). Si el total es exactamente 7, el jugador que apostó al centro gana 3 a 1. Simular este juego en la computadora.

**21.** El *Dara* es un juego de mesa del pueblo dakarkari de Nigeria que se juega en un tablero de 5 × 6 depresiones. Cada jugador tiene doce piedras, que coloca en los hoyos en turnos alternos hasta que ambos jugadores tienen todas sus piedras en la mesa. Luego se mueven alternativamente una piedra a lo largo de una fila o columna hasta el hoyo siguiente. El objeto del juego es colocar tres piedras en línea en hoyos consecutivos de una misma fila o columna (no diagonal). Siempre que un jugador logra tres en línea, puede quitar una de las piedras de su oponente. El juego termina cuando uno de los jugadores ya no puede obtener una línea de tres piedras. Escribir un programa que simule este juego.

**22.** El juego del "cuadrado marcado" se juega en una mesa con 9 filas y 9 columnas. Los jugadores se alternan marcando un cuadrado por vez, cada uno con su marca distintiva. Siempre que un jugador marca el último cuadro en una línea horizontal, vertical o diagonal, se le acreditan todos los cuadrados de esa línea. Cada cuadrado vale un punto. El jugador con la cuenta más alta gana el juego. Simular este juego en la computadora.

**23.** El poder de movimiento del rey en el ajedrez está muy limitado: solo puede desplazarse un cuadro por vez hacia cualquiera de las ocho direcciones adyacentes. Para completar una gira del rey, debe moverse sucesivamente sobre cada celda del tablero exactamente una vez. Escribir un programa para generar una gira del rey en el tablero de ajedrez.

**24.** En un juego de Bingo, se numeran 75 fichas del 1 al 75 y se mezclan en un recipiente. El que canta el bingo saca una ficha por vez y dice su número. Los números del 1 al 15 corresponden a la letra B; del 16 al 30 a la I; del 31 al 45 a la N; del 46 al 60 a la G; y del 61 al 75 a la O. Una carta de Bingo tiene 25 cuadros (5 × 5): el cuadro central es juego libre y los demás contienen números en el rango 1–75. El objeto es conseguir 5 números en una fila, columna o diagonal. Generar un programa para desarrollar el juego de Bingo.

**25.** La Rueda de la Fortuna es un volante giratorio similar al que aparece en programas de televisión. El aro del volante se divide en 60 secciones: 22 billetes de \$10, 14 de \$20, 7 de \$50, 3 de \$100, 2 de \$200, un comodín y una bandera. Los jugadores apuestan a que la flecha se detendrá en una denominación específica. El que acierta recibe el valor de la denominación (1:1). El comodín y la bandera pagan 40 a 1. Generar un programa que simule jugar en la Rueda de la Fortuna.

**26.** "Chuck-a-Luck" es un juego que se desarrolla a menudo en los casinos. Un jugador puede apostar a cualquiera de los números 1, 2, 3, 4, 5 o 6. Se lanzan tres dados. Si el número del jugador aparece en uno, dos o tres de los dados, recibe respectivamente una, dos o tres veces su apuesta original (más la devolución de su apuesta); si no aparece, pierde su apuesta. Simular este juego en una computadora.

**27.** Este problema simula una máquina tragamonedas: el usuario presiona ENTER como si jalara la manija. La máquina genera al azar tres símbolos de los siguientes: Cereza, Limón, Lima, Naranja, Barra, Estrella. La apuesta por juego es \$5. La tabla de pagos es:

| Combinación | Pago |
|---|---|
| 1 Cereza | \$10 |
| 2 Cerezas | \$25 |
| 3 Limones | \$40 |
| 2 Limas | \$25 |
| 3 Limas | \$50 |
| 2 Naranjas | \$25 |
| 3 Naranjas | \$50 |
| 3 Barras | \$40 |
| 3 Estrellas | \$500 |

Imprimir el dinero ganado o perdido por el apostador después de cada tiro simulado.

**28.** El juego de "craps" (siete u once), jugado con dos dados, es uno de los juegos de apuesta más populares. El jugador lanza los dados y gana de inmediato si el total del primer lanzamiento es 7 u 11, y pierde si es 2, 3 o 12. Cualquier otro total se llama su "punto". Si el primer lanzamiento da un punto, el jugador repite la tirada hasta que gane sacando su punto otra vez, o pierda sacando 7. Simular el juego de "craps" en la computadora.

**29.** Programar la computadora para jugar *blackjack* (o 21) contra jugadores humanos, siendo la computadora el distribuidor.

**30.** Un jugador con \$250 necesita llegar a \$500 y considera dos estrategias en la ruleta: apostar los \$250 al "rojo" de una sola vez y retirarse si gana o pierde, o bien apostar al "rojo" \$10 por vez hasta ganar o perder los \$250. Comparar los méritos de ambas estrategias mediante simulación.

**31.** El juego de NIM principia con tres pilas de fichas. Los jugadores, uno de los cuales puede ser la computadora, toman turnos eliminando fichas. El jugador que quite la última ficha pierde. En cada turno, puede sacarse cualquier número de fichas siempre que al menos una se saque y todas provengan de la misma pila. Redactar un programa para jugar NIM.

**32.** El juego de los marcadores principia con 15 marcadores en una línea. Hay dos jugadores que toman turnos alternos. En cada turno, un jugador puede quitar 1, 2 o 3 marcadores. El que tome el último marcador gana. Generar un programa que permita a una persona jugar a los marcadores contra la computadora.

**33.** Escribir un programa para simular a un ratón que trata de encontrar su camino en un laberinto hacia cierto queso. El laberinto será una cuadrícula de 20 × 20. El ratón partirá de la esquina noreste y el queso estará en la esquina suroeste. El ratón puede moverse un cuadro a la vez hacia el norte, sur, este u oeste, sin salirse de la cuadrícula ni regresar a un cuadro donde ya haya estado. Sus movimientos serán determinados al azar generando enteros aleatorios en el rango 1 a 4. El programa imprimirá las posiciones del ratón mientras se mueve a través del laberinto.

**34.** Determinar el número mínimo de movidas necesarias para hacer que los caballos blancos y negros cambien de lugar en un tablero de ajedrez simplificado. Un caballo se mueve en forma de "L": dos cuadros en una dirección y uno en dirección perpendicular. El caballo puede saltar cualquier pieza. (Nota: Este intercambio puede realizarse con 16 movidas individuales.)

**35.** En el juego denominado Yahtzee (Yatzi), se lanzan cinco dados a la vez. El juego consiste en que los dados caigan todos con el mismo número. Simular este juego e imprimir *YAHTZEE* cada vez que los cinco dados caigan iguales. ¿Cuántos lanzamientos se requieren en promedio para obtener un Yahtzee?

**36.** Conecta Cuatro se juega en un tablero de 6 filas y 7 columnas. Dos jugadores se alternan para dejar caer fichas de su color en la columna de su elección; las fichas caen a la posición más baja disponible en esa columna. El primero en colocar cuatro fichas consecutivas en línea (horizontal, vertical o diagonal) gana. Si el tablero se llena sin ganador, hay empate. Escribir un programa para jugar Conecta Cuatro contra la computadora.

**37.** Los cuadrados mágicos son una de las más antiguas y fascinantes curiosidades matemáticas. Un cuadrado mágico es un arreglo de $N^2$ números distintos en una cuadrícula de $N \times N$, de tal manera que la suma de cada columna, cada fila y las dos diagonales principales sea idéntica. Escribir un programa para generar un cuadrado mágico de orden 5 (con los números del 1 al 25). El cuadrado mágico de referencia es:

```
17  24   1   8  15
23   5   7  14  16
 4   6  13  20  22
10  12  19  21   3
11  18  25   2   9
```

(La suma de cada fila, columna y diagonal es 65.)

**38.** Determinar si el siguiente arreglo representa un cuadrado mágico (verificar que la suma de cada fila, columna y las dos diagonales principales sea la misma):

```
64  2  3 61 60  6  7 57
 9 55 54 12 13 51 50 16
17 47 46 20 21 43 42 24
40 26 27 37 36 30 31 33
32 34 35 29 28 38 39 25
41 23 22 44 45 19 18 48
49 15 14 52 53 11 10 56
 8 58 59  5  4 62 63  1
```

**39.** Tac Tic, un juego para dos inventado por Piet Hein de Dinamarca, es una variación del NIM. Se disponen 16 monedas en una cuadrícula de 4 × 4. Los jugadores se alternan para quitar cualquier número de monedas de una sola fila o columna, pero solo pueden eliminarse monedas adyacentes (sin espacios entre ellas). El jugador obligado a sacar la última moneda es el perdedor. Escribir un programa que permita jugar Tac Tic contra la computadora.

**40.** En el juego de la Torre de Hanoi, se debe transferir un conjunto de $n$ discos de una estaca a otra, con la condición de que un disco más grande no quede jamás sobre uno más chico. El número mínimo de movimientos requeridos es:

$2^n - 1$

Una persona está sentenciada a permanecer en la cárcel hasta que logra transferir los discos de la Torre de Hanoi de una estaca a la otra de acuerdo con las reglas del juego. Correr un programa para determinar cuántas movidas separadas tendrá que hacer si hay 20 discos y tres estacas. ¿Cuántos años le llevará si puede realizar un movimiento por segundo? (Sugerencia: el algoritmo de solución es un ejemplo clásico de recursividad; implementarlo de forma recursiva antes de calcular el tiempo.)

**41.** Escribir un programa para jugar el *tic-tac-toe* (gato). Este juego se desarrolla con dos jugadores (uno es la computadora) seleccionando alternadamente cuadros de un arreglo de orden 3. Cuando un jugador obtiene 3 en línea (horizontalmente, verticalmente o en diagonal), imprimir el ganador. Imprimir también un mensaje apropiado si el juego termina en empate.

**42.** Un pentomino es una figura plana formada por cinco cuadros iguales contiguos. Hay doce pentominos distintos posibles. El rompecabezas del pentomino consiste en acomodar los doce pentominos dentro de una caja rectangular de 6 × 10 cuadros. Generar un programa para encontrar algunos de los patrones de acomodo posibles. (Existen más de 2,000 patrones diferentes.)

**43.** Un rompecabezas popular, llamado "Locura Instantánea" (*Instant Insanity*), consiste de 4 bloques cúbicos cuyas caras tienen diferentes colores: rojo (R), azul (A), blanco (B) y verde (V). Ninguno de los bloques tiene la misma distribución de colores en sus caras. El objeto es apilar los cuatro bloques en una columna de tal forma que ninguna de las cuatro caras laterales visibles (frente, atrás, izquierda, derecha) muestre el mismo color repetido. Escribir un programa de búsqueda exhaustiva que encuentre todas las soluciones posibles para una distribución de colores dada.

---

## Problemas adicionales

> *Problemas de elaboración propia, inspirados en el capítulo.*

**44.** Escribir un programa para jugar piedra, papel o tijeras (*Rock, Paper, Scissors*) contra la computadora. La computadora elige aleatoriamente y el jugador introduce su elección. El programa debe llevar el marcador acumulado de victorias, derrotas y empates, y preguntar al usuario si desea seguir jugando. ¿Puede la computadora aprender los patrones del jugador y vencerlo con más frecuencia?

**45.** El *Juego de la Vida* de John Conway es un autómata celular que evoluciona en una cuadrícula bidimensional. Cada celda puede estar viva (1) o muerta (0). Las reglas de evolución son: a) una celda viva con 2 o 3 vecinas vivas sobrevive; b) una celda muerta con exactamente 3 vecinas vivas nace; c) cualquier otro caso resulta en muerte o permanencia muerta. Programar el Juego de la Vida en una cuadrícula de 20 × 20 con un patrón inicial dado (por ejemplo, el "planeador" o *glider*) e imprimir el estado del tablero en cada generación durante 50 pasos.

**46.** *Mastermind* (también llamado Toros y Vacas): la computadora elige en secreto un número de 4 dígitos distintos (sin repetición). El jugador propone números de 4 dígitos y la computadora responde con el número de "toros" (dígito correcto en posición correcta) y "vacas" (dígito correcto en posición incorrecta). El juego termina cuando el jugador adivina el número (4 toros) o agota 10 intentos. Escribir el programa completo del juego.

**47.** El *problema del cumpleaños* pregunta: ¿cuántas personas deben estar en una habitación para que la probabilidad de que al menos dos compartan el mismo cumpleaños sea mayor al 50%? La respuesta analítica es 23. Verificar esto mediante simulación de Monte Carlo: repetir el experimento 10,000 veces para grupos de tamaño $n = 2, 3, \ldots, 50$ e imprimir la frecuencia relativa con que al menos dos personas comparten cumpleaños para cada tamaño de grupo.

**48.** Un verificador de Sudoku: introducir una cuadrícula de 9 × 9 con los números del 1 al 9 y verificar si constituye una solución válida de Sudoku. La solución es válida si: a) cada fila contiene los dígitos del 1 al 9 exactamente una vez; b) cada columna contiene los dígitos del 1 al 9 exactamente una vez; c) cada uno de los nueve subcuadros de 3 × 3 contiene los dígitos del 1 al 9 exactamente una vez.

**49.** Simular el *problema de Monty Hall* generalizado con $N$ puertas ($N \geq 3$). Hay un premio detrás de una puerta y cabras detrás de las demás. El concursante elige una puerta; el presentador abre una puerta con cabra (no la elegida); el concursante puede cambiar o quedarse con su elección. Ejecutar 100,000 simulaciones para $N = 3, 4, 5$ y comparar la probabilidad de ganar al cambiar versus quedarse.

**50.** Generar laberintos aleatorios usando el algoritmo de *recursive backtracking*: comenzar en una celda aleatoria de una cuadrícula de $M \times N$, marcarla como visitada y moverse aleatoriamente a una celda vecina no visitada, derribando la pared entre ellas. Si no hay vecinos sin visitar, retroceder. Repetir hasta haber visitado todas las celdas. El resultado es un laberinto perfecto (con solución única). Imprimir el laberinto de 10 × 10 con caracteres ASCII.

**51.** Generar cuadrados mágicos de orden $N$ impar usando el algoritmo de Siamese (*método del paso diagonal*): colocar el 1 en la celda superior central y cada número siguiente en la celda diagonal superior derecha; si esa posición está ocupada, descender una celda en su lugar; ajustar con aritmética modular para el borde del tablero. Generar e imprimir cuadrados mágicos para $N = 3, 5, 7$ y verificar que la suma de cada fila, columna y diagonal es $N(N^2+1)/2$.
