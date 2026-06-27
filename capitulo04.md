# Capítulo 4: Trigonometría

> *Basado en el libro de Donald D. Spencer, Editorial Limusa, 1985*

## Introducción

En este capítulo hay problemas adecuados para estudiantes que lleven un curso común en Trigonometría o en otros que la incluyan como parte del curso. Las computadoras resultan especialmente útiles en trigonometría porque permiten evaluar funciones trigonométricas, verificar identidades y resolver triángulos de manera rápida y precisa, lo que facilita la comprensión de los conceptos fundamentales.

## Problemas

**1.** Pasar de grados a radianes, usando múltiplos de 10°, desde 0° hasta 360°.

**2.** Hacer un conversor bidireccional de ángulos. El usuario elige mediante un menú: (1) grados → radianes o (2) radianes → grados. El programa convierte el ángulo introducido y muestra el resultado con 6 decimales. Repetir hasta que el usuario elija salir.

**3.** Encontrar los ángulos de un triángulo rectángulo de lados 3, 4 y 5, llegando hasta el minuto más cercano.

**4.** Dados los tres lados de un triángulo cualquiera (no necesariamente rectángulo), usar la ley de los cosenos para encontrar los tres ángulos interiores hasta el minuto más cercano. Probar con los lados $a = 5$ m, $b = 12$ m y $c = 13$ m, y verificar que el resultado del triángulo 5-12-13 es rectángulo.

**5.** Cualquier ángulo cuya medida en grados sea mayor que 90° o menor que 0° tiene un ángulo de referencia entre 0° y 90°, inclusive. Introducir la medida en grados de un ángulo entre −360° y 360°, inclusive, e imprimir la medida de su ángulo de referencia.

**6.** Convertir de coordenadas polares $(r,\,\theta)$ a rectangulares $(x,\,y)$ usando $x = r\cos\theta$ y $y = r\sin\theta$. Evaluar las siguientes curvas para $\theta = 0°, 5°, 10°, \ldots, 360°$:

$$r = \cos 3\theta$$

$$r = \sin 3\theta$$

$$r = \sin\theta + \cos\theta$$

**7.** Dado un ángulo $\theta$ en grados, calcular el punto $(\cos\theta,\,\sin\theta)$ sobre el círculo unitario. Mostrar en pantalla: el ángulo en grados y en radianes, los valores de sin, cos y tan, y la posición aproximada del punto en un diagrama ASCII de $21 \times 21$ caracteres. Probar con $\theta = 0°, 30°, 45°, 60°, 90°, 120°, 150°, 180°, 270°$.

**8.** Sin usar las funciones ya programadas para senos y cosenos, generar una tabla para estas funciones con todos los ángulos desde 0° a 90°, usando las series de Taylor (ver problemas 28 y 29).

**9.** Imprimir en forma de columna el seno, coseno y tangente de $x$ en grados. Introducir el ángulo inicial $A$, el incremento $I$ y el ángulo final $B$.

**10.** Dado cualquier triángulo con lados $a$, $b$ y $c$ introducidos por el usuario: (a) determinar si es agudo, rectángulo u obtuso comparando $a^2 + b^2$ con $c^2$ para el lado mayor; (b) calcular los tres ángulos interiores con la ley de los cosenos; (c) clasificarlo como escaleno, isósceles o equilátero. Probar con: $(5, 5, 8)$, $(3, 4, 5)$, $(6, 7, 8)$, $(10, 10, 10)$.

**11.** Un triángulo rectángulo tiene un ángulo de 42°25' y el lado opuesto a este ángulo mide 25.4 cm. Encontrar los otros dos lados del triángulo.

**12.** Determinar el área de un triángulo usando la fórmula:

$$\text{Área} = \frac{1}{2}\,a\,b\,\sin C$$

donde $a$ y $b$ son dos lados conocidos y $C$ es el ángulo comprendido entre ellos.

**13.** Introducir las longitudes de la hipotenusa y un cateto de un triángulo rectángulo. Determinar el seno, coseno y tangente de cada uno de los ángulos agudos del triángulo.

**14.** Leer las longitudes de los catetos de un triángulo rectángulo. Calcular e imprimir los valores de las seis funciones trigonométricas de cada ángulo agudo del triángulo.

**15.** Imprimir $\sin^2 x + \cos^2 x$ para $x = 5°, 10°, 15°, \ldots, 85°$. Examinar la salida. ¿Qué conclusiones puede sacar?

**16.** Verificar la identidad trigonométrica $\sin 2\theta = 2\sin\theta\cos\theta$ para diez valores de $\theta$ elegidos entre 0° y 360°.

**17.** Si se conocen las longitudes de dos lados de un triángulo y la medida del ángulo comprendido, se puede usar la ley de los cosenos para determinar el tercer lado. Para cualquier triángulo $ABC$:

$$a^2 = b^2 + c^2 - 2bc\cos A$$

$$b^2 = a^2 + c^2 - 2ac\cos B$$

$$c^2 = a^2 + b^2 - 2ab\cos C$$

Usar la ley de los cosenos para encontrar el lado desconocido de un triángulo con $b = 6$ cm, $c = 8$ cm y ángulo comprendido $A = 22°$.

**18.** La ley de los senos establece que para cualquier triángulo $ABC$:

$$\frac{a}{\sin A} = \frac{b}{\sin B} = \frac{c}{\sin C}$$

Dadas las longitudes de los lados $a$ y $b$ y el ángulo $C$, usar la ley de los cosenos para determinar el lado $c$ y luego la ley de los senos para encontrar los ángulos $A$ y $B$.

**19.** Dos botes deportivos abandonan un muelle al mismo tiempo. Uno va hacia el norte a razón de 57 km/h y el otro a 63 km/h en una dirección de 40° al oeste respecto al norte. Después de 2 h, ¿a qué distancia se encuentran entre sí los botes?

**20.** Un estudiante desea conocer la altura de la torre de telecomunicaciones de su ciudad. Desde un punto a 450 m de la base de la torre, mide un ángulo de elevación de 20°. Escribir un programa para calcular la altura de la torre. Generalizar el programa para que acepte cualquier distancia y ángulo de elevación como entrada.

**21.** Calcular el área de un polígono regular de $N$ lados, cada uno de longitud $L$ metros:

$$\text{Área} = \frac{NL^2}{4}\cot\!\left(\frac{180°}{N}\right)$$

El programa debe introducir los valores de $N$ y $L$.

**22.** Dos fuerzas actúan sobre un punto $P$. La primera, de magnitud $F_1 = 45$ N, forma un ángulo de 41° con la horizontal; la segunda, de magnitud $F_2 = 60$ N, forma un ángulo de 72° con la horizontal. Calcular la magnitud y dirección de la fuerza resultante.

**23.** A 274 m de la base de un faro, a nivel del suelo, el ángulo de elevación de la linterna es de 8°15'. Encontrar la altura del faro.

**24.** Una empresa de ingeniería civil está construyendo un puente a través de un río, desde el punto $A$ al punto $B$. Para encontrar la longitud del puente, un ingeniero localiza un punto $C$ a 30 m de $A$ tal que el triángulo $BAC$ sea rectángulo en $C$. El ángulo $BCA$ mide 55°. ¿Qué longitud debe tener el puente?

**25.** En los videojuegos de estrategia y en mapas digitales se usan cuadrículas hexagonales. El área de un hexágono regular de lado $L$ es:

$$A_{hex} = \frac{3\sqrt{3}}{2}L^2$$

y su perímetro es $P = 6L$. Dado el lado $L$ de cada celda hexagonal y el número de celdas del mapa $N$, calcular el área total cubierta. Probar con $L = 1$ m y $N = 7,\,19,\,37$ (los primeros anillos concéntricos de un mapa hex).

**26.** Un topógrafo desea medir la longitud de un lago. Para encontrar la distancia $AB$ entre dos puntos en orillas opuestas, localiza un punto $C$ a 95 m de $A$ y a 122 m de $B$, y mide que el ángulo $ACB$ es de 47.5°. ¿Cuál es la longitud del lago?

**27.** En un parque hay un sendero peatonal entre los puntos $X$ e $Y$, con una distancia de 85 m. Los administradores desean construir senderos adicionales de $X$ a $Z$ y de $Y$ a $Z$. El ángulo $YXZ$ es de 38° y el ángulo $XYZ$ es de 54°. Determinar las longitudes $XZ$ e $YZ$.

**28.** Calcular $\sin x$ mediante la serie de Taylor:

$$\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots$$

donde $x$ está en radianes. Continuar la serie hasta que el término siguiente sea menor que $10^{-8}$.

**29.** Calcular $\cos x$ con la serie de Taylor:

$$\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots$$

donde $x$ está en radianes. Continuar la serie hasta que el término siguiente sea menor que $10^{-8}$.

**30.** Calcular $\arctan x$ con la serie de Taylor:

$$\arctan x = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots \quad (-1 < x < 1)$$

Usar el programa para calcular $\pi \approx 4\arctan(1)$ con la serie de Leibniz.

**31.** Una identidad fundamental de la trigonometría establece que para cualquier valor de $x$: $\sin^2 x + \cos^2 x = 1$. Diseñar un programa que verifique esta identidad para $x = 0°, 1°, 2°, \ldots, 360°$ e imprima los casos donde el resultado se aleje más de $10^{-10}$ de 1.

**32.** Calcular el área de un segmento de círculo con la fórmula:

$$\text{Área} = \frac{\pi r^2}{2} - \left[x\sqrt{r^2 - x^2} + r^2 \arcsin\!\left(\frac{x}{r}\right)\right]$$

donde $r$ es el radio del círculo y $x$ es la distancia perpendicular del centro a la cuerda.

**33.** Encontrar todos los ángulos $\theta \in [0°,\,360°)$ que satisfacen la ecuación trigonométrica:

$$2\cos^2\theta - \cos\theta - 1 = 0$$

Verificar cada solución sustituyendo en la ecuación original. Imprimir las soluciones en grados y en radianes.

---

## Problemas adicionales

> *Problemas de elaboración propia, inspirados en el capítulo.*

**34.** Verificar las identidades de la suma de ángulos para diez pares $(A,\,B)$ generados aleatoriamente entre 0° y 360°:

$$\cos(A + B) = \cos A \cos B - \sin A \sin B$$

$$\sin(A + B) = \sin A \cos B + \cos A \sin B$$

**35.** Una señal de corriente alterna tiene la forma:

$$v(t) = A\sin(2\pi f t + \phi)$$

Con $A = 127$ V (tensión residencial estándar en México), $f = 60$ Hz y $\phi = \pi/6$ rad, imprimir la tensión $v(t)$ para $t = 0, 1, 2, \ldots, 20$ ms. Calcular también el valor RMS teórico $V_{rms} = A/\sqrt{2}$ y compararlo con el promedio cuadrático de los valores simulados.

**36.** Un avión parte de la ciudad $A$ y vuela 450 km en dirección N45°E hasta $B$; luego vuela 320 km en dirección S30°E hasta $C$. Calcular la distancia directa $AC$ y el rumbo desde $A$ hacia $C$.

**37.** Calcular todos los ángulos $\theta \in [0°,\,360°)$ que satisfacen la ecuación:

$$2\sin^2\theta - 3\sin\theta + 1 = 0$$

**38.** El período de un péndulo simple de longitud $L$ es:

$$T = 2\pi\sqrt{\frac{L}{g}}$$

con $g = 9.81$ m/s². Crear una tabla con $L = 0.25,\,0.50,\,0.75,\,1.00,\,1.50,\,2.00$ m y el período correspondiente en segundos.

**39.** Convertir coordenadas esféricas $(\rho,\,\theta,\,\phi)$ a rectangulares $(x,\,y,\,z)$ usando:

$$x = \rho\sin\phi\cos\theta \qquad y = \rho\sin\phi\sin\theta \qquad z = \rho\cos\phi$$

Calcular para $\rho = 5$ m, $\theta = 30°$ y $\phi = 60°$.

**40.** Dado un triángulo con lados $a = 12$ m, $b = 17$ m y $c = 9$ m, usar la ley de los cosenos para encontrar los tres ángulos interiores.

**41.** Desde dos puntos $A$ y $B$ situados a 800 m de distancia en terreno plano se miden los ángulos de elevación de la cima de una montaña: 35° desde $A$ y 48° desde $B$, ambos del mismo lado. Calcular la altura de la montaña.

**42.** Calcular el módulo y argumento de los números complejos $z = a + bi$, expresándolos en forma trigonométrica $z = r(\cos\theta + i\sin\theta)$, para:

$$z_1 = 3 + 4i \qquad z_2 = -5 + 12i \qquad z_3 = 8 - 6i$$

**43.** La temperatura de una ciudad varía durante el día según:

$$T(h) = 22 + 8\sin\!\left(\frac{\pi(h - 6)}{12}\right)\ °\text{C}$$

donde $h$ es la hora del día ($0 \leq h < 24$). Calcular e imprimir la temperatura para cada hora. Determinar el momento del día en que se alcanzan la temperatura máxima y la mínima.
