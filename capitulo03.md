# Capítulo 3: Geometría

> *Basado en el libro de Donald D. Spencer, Editorial Limusa, 1985*

## Introducción

Este capítulo contiene problemas adecuados para usarse en un curso habitual de Geometría. Con la computadora, los estudiantes en la clase de Geometría pueden calcular áreas y volúmenes de figuras y cuerpos geométricos con gran exactitud; generar tripletas pitagóricas y explorar muchas áreas que eran inaccesibles antes.

## Problemas

**1.** Dados los tres lados $A$, $B$ y $C$ de un triángulo, encontrar los tres ángulos $a$, $b$ y $c$. Suponer que todos los ángulos son agudos.

**2.** Dada una medida angular mayor que 0° pero menor que 180°, clasificar el ángulo como obtuso, recto o agudo.

**3.** Introducir $D$, los grados de un ángulo agudo, y calcular la medida de su complemento y suplemento.

**4.** Determinar el ángulo entre dos líneas que se intersecan.

**5.** Introducir las medidas de dos ángulos interiores opuestos en un triángulo. Determinar la medida de uno de los ángulos externos.

**6.** Introducir la medida del ángulo del vértice de un triángulo isósceles $ABC$ con $AB = AC$ y determinar la medida del ángulo de la base.

**7.** La distancia entre dos puntos $A$ y $B$ se define como $|A - B|$. Escribir un programa para comparar $|A - B|$ y $|B - A|$. Usar las siguientes posiciones para $A$ y $B$ en los datos de prueba:

```
    A    12    −5    −2     9
    B    10     9    −3    13
```

**8.** Encontrar el área de cualquier rectángulo con la fórmula $\text{Área} = lw$, donde $l$ es la longitud y $w$ es el ancho.

**9.** Encontrar el tercer lado de un triángulo rectángulo mediante el teorema de Pitágoras.

**10.** Determinar la longitud de la hipotenusa en cada uno de estos triángulos rectángulos: ARB, BRC, CRD, DRE, ERF.

```
    F
     \
      E
       \
        D
         \
          C
           \
            B
             \
    R —————————A
```

*(Escalera de triángulos rectángulos con cateto vertical = 1. Las hipotenusas son $\sqrt{2}$, $\sqrt{3}$, $\sqrt{4}$, $\sqrt{5}$, $\sqrt{6}$.)*

**11.** Un patrón de vestido requiere 3.2 m de tela de 115 cm de ancho. ¿Cuántos metros se necesitarán de una tela de 90 cm de ancho para cubrir la misma área de tela?

**12.** La suma de los ángulos de un triángulo es 180°. Introducir dos ángulos $A$ y $B$ y calcular el valor del tercer ángulo $C$. El programa debe verificar que el tercer ángulo no sea cero ni negativo; si esto ocurre, imprimir el mensaje `NO ES UN TRIÁNGULO`.

**13.** Un teorema fundamental de Geometría se refiere a las medidas de los tres lados de un triángulo. El teorema establece que la suma de las medidas de dos cualesquiera de los lados debe ser mayor que la medida del tercero. Hacer un programa que determine si tres números cualesquiera pueden ser las medidas de los lados de un triángulo.

**14.** Introducir tres números positivos $X$, $Y$ y $Z$. Determinar si pueden ser las longitudes de los lados de un triángulo recto.

**15.** Hacer un programa que encuentre los tres ángulos de un triángulo, dados los tres lados.

**16.** Dados los tres lados de cualquier triángulo $ABC$, calcular e imprimir el área de ese triángulo.

**17.** Introducir las longitudes de los lados de un triángulo. Determinar si el triángulo es isósceles, equilátero o escaleno.

**18.** Introducir las longitudes de los catetos de un triángulo rectángulo y calcular el perímetro.

**19.** Introducir las longitudes de los lados de un triángulo. Encontrar el perímetro.

**20.** Introducir las longitudes de los tres lados de un triángulo y determinar el área.

**21.** Dados tres elementos cualesquiera de un triángulo, uno de los cuales debe ser un lado, calcular e imprimir el área.

**22.** Dados dos lados y el ángulo que forman en cualquier triángulo $ABC$, calcular e imprimir su área.

**23.** Determinar el perímetro de un triángulo rectángulo isósceles, dada la longitud de un cateto.

**24.** Introducir la longitud de la hipotenusa de un triángulo rectángulo isósceles y calcular la longitud de un cateto.

**25.** Introducir $B$, la base, y $H$, la altura de un triángulo, y determinar el área usando $\text{Área} = \frac{1}{2}BH$.

**26.** Snoopy, un gigante de otro planeta, ha decidido invadir la Tierra y regresar luego a su propio planeta. Durante su visita, prefiere ocultar su identidad portando una máscara que le cubra la nariz y la boca. La máscara debe tener una altura $h = 6.4$ m y una base $b = 14.3$ m. Con la ecuación $\text{Área} = \frac{1}{2}bh$, escribir un programa para determinar los metros cuadrados que necesitará el gigante.

**27.** El área de un triángulo rectángulo es igual a dos veces su perímetro:

$$\frac{1}{2}(A \times B) = 2(A + B + C)$$

Los lados del triángulo son enteros, cada uno menor que 100. Encontrar los lados del triángulo.

**28.** Introducir $X$, la longitud de un lado de un triángulo equilátero, y calcular su perímetro.

**29.** Determinar el perímetro de un triángulo rectángulo, dadas las longitudes de los catetos.

**30.** Determinar el perímetro de un triángulo rectángulo, dadas las longitudes de la hipotenusa y la de un cateto.

**31.** Introducir las longitudes de los lados de un triángulo y las longitudes de los tres lados correspondientes de un segundo triángulo. Determinar si los triángulos son semejantes.

**32.** Introducir las longitudes de los tres lados de un triángulo y las de los tres lados correspondientes de un segundo triángulo. Determinar si los triángulos son congruentes.

**33.** Se proporcionan como datos las coordenadas de los vértices de dos triángulos. Determinar si un triángulo está inscrito en el otro.

**34.** Encontrar el área de un triángulo dadas las coordenadas de los tres vértices.

**35.** La fórmula de Herón puede usarse para encontrar el área de cualquier triángulo, dadas las medidas de los tres lados. La fórmula es:

$$\text{Área} = \sqrt{s(s-a)(s-b)(s-c)}$$

donde $s = \frac{1}{2}(a + b + c)$. Encontrar el área de un triángulo cuyos lados sean 6, 8 y 10 m.

**36.** Con la fórmula de Herón, encontrar e imprimir los triángulos cuyas áreas sean enteras y cuyos lados sean enteros consecutivos menores que 1000.

**37.** Encontrar el área de cualquier cuadrado con la fórmula $A = S^2$.

**38.** Dada la longitud de un lado de un cuadrado, calcular el perímetro.

**39.** Calcular el área superficial $S$ de un prisma rectangular con dimensiones $l$, $h$ y $w$, usando $S = 2(lh + lw + hw)$. En este problema, $l = 10$, $h = 4$ y $w = 5.2$ m.

**40.** Una cocina tiene dos paredes que van a cubrirse con azulejos: la primera mide 2.20 m de ancho por 1.10 m de alto, y la segunda mide 1.65 m de ancho por 1.10 m de alto. Cada azulejo es un cuadrado de 11 cm por lado. ¿Cuál es el número mínimo de azulejos que se necesita en total?

**41.** Si una sala tiene dimensiones de 4 × 6 m, ¿cuánto costará alfombrarla si la alfombra cuesta \$380 el metro cuadrado?

**42.** ¿Habrá algún cambio en el área de un rectángulo si se duplica su longitud y su anchura se divide entre dos?

**43.** Va a empapelarse una habitación. Sus dimensiones son 4.25, 5.60 y 2.80 m de anchura, largo y altura, respectivamente. En la habitación hay dos puertas de 1 × 2.30 m y una ventana de 1.50 × 2 m. ¿Cuántos metros cuadrados de papel se requerirán? (Recuérdese que una habitación tiene cuatro paredes y que no se necesita papel para las puertas y la ventana.)

**44.** Marlene decidió plantar un vivero rectangular de melón. ¿Cuántos metros de cerca necesitará si el vivero tiene dimensiones de 6.5 y 4.70 m?

**45.** Una cantante de Monterrey habita en un departamento de 6 × 6 × 6 m. Desea pintar las paredes y el techo con pintura de interior que cubre aproximadamente 10 metros cuadrados por litro. Hacer un programa para determinar cuántos litros de pintura debe comprar.

**46.** El edificio de Artes Médicas consta de cuatro habitaciones con las siguientes dimensiones:

```
    1a.   3.5 × 4.0 m
    2a.   4.5 × 5.5 m
    3a.   4.0 × 6.0 m
    4a.   5.0 × 8.5 m
```

Calcular el espacio de piso en este edificio.

**47.** Una mesa mide 2.31 m. Si va a seccionarse en cuatro tramos de igual longitud, ¿cuántos centímetros tendrá cada uno? Si va a cortarse por la mitad, ¿cuántos centímetros habrá del centro a cada extremo?

**48.** Un rectángulo de 6 × 3 m tiene un área de 18 metros cuadrados y un perímetro de 18 m. Encontrar otro rectángulo que tenga el mismo área y el mismo perímetro.

**49.** Una piscina tiene dimensiones de 7 × 14 m y una profundidad promedio de 1.4 m. ¿Cuál es el peso del agua en la piscina en (a) kg y (b) toneladas métricas?

**50.** Calcular e imprimir el área y el perímetro de un paralelogramo con valores de entrada de $c = 8$, $d = 4.2$ y $h = 4$ m.

**51.** Si un paralelogramo tiene una base de 30 cm y una altura vertical de 15 cm, ¿cuál es su área?

**52.** Los lados de un paralelogramo son de 35 y 50 m y el ángulo menor es de 20°. ¿Cuál es la longitud de la mayor de las dos diagonales?

**53.** Introducir la altura y la longitud de las bases de un trapezoide y determinar su área.

**54.** Introducir el radio de una esfera y calcular su área superficial.

**55.** Introducir las longitudes de los cuatro lados de un cuadrilátero. Determinar si el cuadrilátero es equilátero.

**56.** Un papalote tiene la forma de un cuadrilátero con dos pares de lados adyacentes congruentes. Si la diagonal vertical es la bisectriz perpendicular de la diagonal horizontal, determinar el área del papalote.

**57.** Calcular e imprimir el volumen de un cilindro de radio $r$ y altura $h$. En este problema, $r = 10$ cm y $h = 32$ cm. Usar la fórmula $V = \pi r^2 h$.

**58.** Calcular el volumen de cualquier cilindro si se conocen el radio de la base y la altura del cilindro.

**59.** Calcular el área superficial total de un cilindro con la fórmula $S = 2\pi(r^2 + rh)$.

**60.** Calcular el área de la envoltura de papel de una lata cilíndrica de maíz que tiene 24 cm de altura y 12 cm de diámetro. La fórmula para el área lateral de un cilindro es:

$$\text{Área} = \text{altura} \times \text{diámetro} \times \pi$$

**61.** Introducir la longitud $L$ de la altura y el radio $R$ de la base de un cilindro circular recto. Determinar el volumen, el área superficial total y el área lateral del cilindro.

**62.** Encontrar la altura oblicua de una pirámide cuadrada regular, dadas la longitud de un lado de la base y la de una arista.

**63.** Calcular el área superficial de una pirámide regular, donde $b$ es la longitud de cada lado de la base y $h$ es la altura de cada cara triangular. En este problema, $b = 10$ y $h = 17$.

**64.** Introducir la longitud de un lado de la base y la de una arista de una pirámide cuadrada regular. Determinar el volumen, el área lateral, el área superficial y la altura oblicua de la pirámide.

**65.** Introducir $N$, el número de lados de un polígono regular. Determinar la medida de cada ángulo interior.

**66.** Leer $X$, un entero positivo que denota el número de lados de un polígono. Calcular la suma de los ángulos interiores del polígono.

**67.** Introducir las longitudes de los cinco lados de un pentágono. Determinar si es equilátero.

**68.** Calcular el área de un polígono. Suponer que el polígono tiene un número conocido pero variable de lados.

**69.** Calcular el área de un polígono regular, dados el número de lados y las medidas del apotema y de un lado.

**70.** Calcular e imprimir el área $A$ y la longitud del perímetro $P$ de un polígono con $n$ lados circunscrito en una circunferencia de radio $r$. Introducir valores para $r$ y $n$ y sacar los valores de $A$ y $P$.

**71.** Calcular el volumen y el área superficial de una esfera con las fórmulas $V = \frac{4\pi r^3}{3}$ y $A = 4\pi r^2$, donde $r$ es el radio. En este problema, $r = 10$ cm.

**72.** Introducir la longitud $L$, la anchura $W$ y la altura $H$ de un prisma rectangular. Calcular el volumen y el área superficial total del prisma.

**73.** Introducir las longitudes de las diagonales y determinar el área de un rombo.

**74.** Calcular el volumen de un "trompo" (sólido bicónico de revolución) para valores de entrada de $r$, $a$ y $b$, donde $r$ es el radio máximo y $a$, $b$ son las alturas de cada cono:

$$V = \frac{\pi r^2}{3}(a + b)$$

**75.** Introducir $A$, la altura, y $R$, el radio de la base de un cono circular recto. Determinar el volumen, el área lateral y el área superficial total.

**76.** Un ingeniero que construye presas de tierra necesita un programa para calcular el volumen de tierra requerido para una cierta presa. Todas las presas tienen la sección transversal trapezoidal que se muestra abajo y solo varían en dimensiones. ¿Puede usted ayudar al ingeniero haciendo un programa para calcular el volumen en metros cúbicos?

```
           |<—— a ——>|
       ____________________
      /                    \
     /                      \
    /                        \
   /                          \
  |<——H——>|<——— a ————>|<——H——>|
```

*(Datos de entrada: cresta $a$, talud $H$, altura y longitud de la presa.)*

**77.** Una tripleta pitagórica es un conjunto de números que satisface la relación $A^2 + B^2 = C^2$. Los números $(3, 4, 5)$ y $(5, 12, 13)$ son ejemplos de tripletas pitagóricas, pues $3^2 + 4^2 = 5^2$ y $5^2 + 12^2 = 13^2$. Encontrar 15 tripletas de este tipo.

**78.** Encontrar todas las tripletas pitagóricas con una hipotenusa menor o igual que 70.

**79.** Verificar que el producto de los tres números de una tripleta pitagórica es siempre divisible entre 60.

**80.** Aproximar $\pi$ tomando la suma de los primeros 25 términos en la fórmula de Leibniz:

$$\frac{\pi}{4} = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \frac{1}{9} - \cdots$$

multiplicando el resultado por cuatro.

**81.** La distancia $d$ entre dos puntos en el plano real puede determinarse con la fórmula:

$$d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$

donde $(x_1, y_1)$ y $(x_2, y_2)$ son los puntos. Imprimir la distancia entre los puntos $(14, 16)$ y $(38, 63)$.

**82.** Encontrar la distancia entre dos puntos cualesquiera $(a, b)$ y $(c, d)$. Usar los siguientes puntos como datos: $(2, 3)$ y $(4, 7)$; $(1, 8)$ y $(-2, 8)$; $(-3, 6)$ y $(12, -4)$; $(-7, 0)$ y $(0, 2)$.

**83.** Introducir las coordenadas de dos puntos $A$ y $B$ en el plano coordenado. Determinar la longitud del segmento $AB$.

**84.** Introducir las coordenadas de dos puntos $A$ y $B$ en el plano coordenado. Encontrar las coordenadas del punto medio del segmento $AB$.

**85.** Usar las coordenadas de dos puntos en el plano y calcular la distancia entre ellos, las coordenadas del punto medio y la pendiente del segmento de recta.

**86.** Dadas las coordenadas de cuatro puntos en el plano $XY$, decidir si el cuadrilátero formado por la unión ordenada de los puntos es un paralelogramo.

**87.** Dadas las coordenadas de tres puntos en el plano $XY$, determinar si son colineales.

**88.** Determinar la circunferencia de un círculo con cualquier diámetro dado. Probar el programa para los diámetros siguientes: 4, 100, 16.4 y 34,000.

**89.** El radio medio de la Tierra es de 6,371 km. Calcular la circunferencia de la Tierra.

**90.** ¿Cuál es el área de un círculo cuyo radio es de 8 cm?

**91.** Introducir el radio $R$ de un círculo. Determinar el área usando $\frac{22}{7}$ para $\pi$ y 3.14159 para $\pi$. Introducir varios valores de $R$ e imprimir los resultados del cálculo en forma tabular.

**92.** Dadas las coordenadas del centro y la longitud de su radio, determinar la ecuación de la circunferencia.

**93.** ¿Cómo se modificaría el área de un círculo si se duplica su radio? ¿Se reduciría a la mitad? ¿Se triplicaría? Hacer y correr un programa que le ayude en su respuesta.

**94.** Un cilindro tiene 1.1 m de largo y el radio de su base es de 7 cm. ¿Cuál es su volumen (a) en cm cúbicos y (b) en m cúbicos?

**95.** Un granjero planta sus cacahuates en un campo semicircular de 61 m de diámetro. Hacer un programa para determinar el área del campo.

**96.** Dada una circunferencia que pasa por $(2.3,\,-0.3)$, $(0.1,\,0.5)$ y $(1.02,\,-0.3)$, encontrar las coordenadas del centro y la medida de su radio.

**97.** Encontrar el área delimitada por la gráfica de cualquier circunferencia de la forma $X^2 + Y^2 = r^2$.

**98.** Tomás ordenó 36 m de cerca para una jaula rectangular para perro. Muchos rectángulos tienen 36 m de perímetro. Por ejemplo, 6 × 12, 8 × 10, 9 × 9. Determinar el rectángulo de mayor área para su perro.

**99.** Un granjero posee un terreno que limita con un río no sinuoso. Tiene 30 m de cerca y desea delimitar un área rectangular, utilizando al río como límite a lo largo de un lado del rectángulo y la cerca para los otros tres lados. Encontrar la forma del rectángulo con área máxima. ¿Cuál es la forma con área máxima si la cerca puede instalarse solo en tramos de 3 m?

**100.** Determinar la media geométrica de dos números reales positivos.

**101.** La serie $P(N) = 4\left[1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \cdots + \frac{(-1)^{N+1}}{2N-1}\right]$ converge a $\pi$. Calcular $P(N)$ hasta $P(1000)$, imprimiendo cada valor centésimo. El milésimo debe salir 3.140578, que ya no coincide en el tercer lugar decimal con $\pi$.

---

## Problemas adicionales

**102.** Calcular la distancia entre dos puntos en el espacio tridimensional $(x_1, y_1, z_1)$ y $(x_2, y_2, z_2)$ con la fórmula:

$$d = \sqrt{(x_2-x_1)^2 + (y_2-y_1)^2 + (z_2-z_1)^2}$$

Probar con los puntos $(1, 2, 3)$ y $(4, 6, 3)$.

**103.** Calcular el área de un polígono arbitrario de $N$ vértices usando la fórmula de Gauss (Shoelace):

$$A = \frac{1}{2}\left|\sum_{i=0}^{N-1}(x_i\, y_{i+1} - x_{i+1}\, y_i)\right|$$

donde los índices son módulo $N$. Probar con un pentágono cuyos vértices se introduzcan como datos.

**104.** Dado un conjunto de $N$ puntos en el plano, encontrar la caja envolvente mínima (*bounding box*): el rectángulo de lados paralelos a los ejes que contiene a todos los puntos. Imprimir $x_{\min}$, $x_{\max}$, $y_{\min}$, $y_{\max}$ y el área de la caja.

**105.** Determinar si un punto $P(px, py)$ está dentro de un triángulo con vértices $A$, $B$ y $C$ usando coordenadas baricéntricas. El programa debe imprimir `INTERIOR`, `FRONTERA` o `EXTERIOR` según corresponda.

**106.** La distancia entre dos puntos sobre la superficie terrestre puede calcularse con la fórmula de Haversine:

$$d = 2R \arcsin\!\left(\sqrt{\sin^2\!\frac{\Delta\phi}{2} + \cos\phi_1\cos\phi_2\,\sin^2\!\frac{\Delta\lambda}{2}}\right)$$

donde $R = 6{,}371$ km, $\phi$ son latitudes y $\lambda$ longitudes en radianes. Calcular la distancia entre Tijuana (32.52°N, 117.04°O) y la Ciudad de México (19.43°N, 99.13°O).

**107.** El copo de nieve de Koch se construye dividiendo cada lado de un triángulo equilátero en tres partes iguales y reemplazando el segmento central por dos lados de un triángulo equilátero menor. Después de $N$ iteraciones, el perímetro es $P_N = 3s\left(\dfrac{4}{3}\right)^N$. Dado el lado inicial $s$ y el número de iteraciones $N$, calcular el perímetro y el área acumulada del copo.

**108.** Calcular el área y el perímetro aproximado de una elipse con semiejes $a$ y $b$. El área es $A = \pi ab$. Para el perímetro, usar la aproximación de Ramanujan:

$$P \approx \pi\!\left[3(a+b) - \sqrt{(3a+b)(a+3b)}\right]$$

Probar con $a = 5$ cm y $b = 3$ cm.

**109.** Calcular el centroide, el incentro y el circuncentro de un triángulo dados sus tres vértices $(x_1,y_1)$, $(x_2,y_2)$, $(x_3,y_3)$. Verificar que para un triángulo equilátero los tres puntos coinciden.

**110.** Un toro tiene radio mayor $R$ (del centro del toro al centro del tubo) y radio menor $r$ (del tubo). Sus fórmulas son: volumen $V = 2\pi^2 R r^2$ y área superficial $A = 4\pi^2 R r$. Dado $R = 5$ cm y $r = 2$ cm, calcular $V$ y $A$.

**111.** La fórmula de Euler para poliedros establece que $V - A + C = 2$, donde $V$ es el número de vértices, $A$ el de aristas y $C$ el de caras. Verificar esta fórmula para: (a) cubo ($V=8$, $A=12$, $C=6$); (b) tetraedro ($V=4$, $A=6$, $C=4$); (c) octaedro ($V=6$, $A=12$, $C=8$); (d) dodecaedro ($V=20$, $A=30$, $C=12$); (e) icosaedro ($V=12$, $A=30$, $C=20$).
