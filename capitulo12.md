# Capítulo 12: Algoritmos Clásicos y Estructuras de Datos

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

Los algoritmos y las estructuras de datos son el vocabulario fundamental de la programación. Dominarlos permite escribir código que no solo funciona, sino que escala. Un algoritmo de búsqueda lineal puede ser aceptable con 100 registros; con 10 millones, necesitas búsqueda binaria. Este capítulo cubre las estructuras y algoritmos que todo programador debe conocer antes de enfrentar entrevistas técnicas, proyectos de alto rendimiento o competencias de programación. Los problemas están ordenados de menor a mayor complejidad dentro de cada subtema.

## Búsqueda y Ordenamiento

**1.** Implementar búsqueda lineal que reciba una lista y un valor objetivo, y devuelva el índice donde se encuentra o −1 si no existe. Medir el número de comparaciones realizadas. ¿Cómo cambia ese número cuando el elemento está al principio, al final o no existe?

**2.** Implementar búsqueda binaria iterativa y recursiva sobre una lista ordenada. Verificar que ambas produzcan el mismo resultado en 20 pruebas. ¿Cuántas comparaciones hace cada versión en el peor caso para una lista de 1,000,000 elementos?

**3.** Implementar los seis algoritmos de ordenamiento clásicos: burbuja, selección, inserción, quicksort, mergesort y heapsort. Para cada uno, contar comparaciones e intercambios al ordenar la misma lista de 1,000 números aleatorios. Presentar resultados en tabla comparativa.

**4.** Dado un arreglo casi ordenado (solo 5 elementos fuera de lugar en una lista de 1,000), demostrar experimentalmente qué algoritmo es más eficiente midiendo tiempo de ejecución para: arreglo casi ordenado, ordenado al revés y completamente aleatorio.

**5.** Implementar ordenamiento externo para un archivo de 10 millones de enteros que no cabe en RAM. Dividir en bloques manejables, ordenar cada bloque y fusionarlos con una cola de prioridad. Verificar que el archivo de salida está correctamente ordenado.

## Estructuras de Datos Lineales

**6.** Implementar una pila con las operaciones push, pop, peek e isEmpty. Usarla para verificar que una expresión con paréntesis, corchetes y llaves esté balanceada. Probar con: `{[()]}` (válido), `([)]` (inválido), `(((` (inválido).

**7.** Implementar una cola y usarla para simular la fila de atención en una ventanilla del IMSS: llegan pacientes cada 1–5 minutos (aleatorio), la atención toma 3–7 minutos (aleatorio). Simular 8 horas e imprimir tiempo de espera promedio y máximo.

**8.** Implementar una lista enlazada simple con inserción al inicio, inserción al final, eliminación por valor y búsqueda. Luego implementar la inversión de la lista en su lugar sin copiar a un arreglo auxiliar.

**9.** Implementar una lista doblemente enlazada para representar el historial de navegación de un explorador web: avanzar, retroceder y agregar nueva página eliminan el historial hacia adelante. El historial tiene un límite máximo de 50 páginas.

**10.** Implementar una tabla hash con manejo de colisiones por encadenamiento. Insertar los RFC de 10,000 contribuyentes ficticios (13 caracteres) y medir: número de colisiones, longitud promedio de las cadenas y tiempo de búsqueda promedio.

## Árboles

**11.** Implementar un árbol binario de búsqueda (BST) con inserción, búsqueda y eliminación. Insertar los 32 estados de México en orden alfabético y luego en orden aleatorio. Comparar la altura del árbol resultante en cada caso.

**12.** Implementar los tres recorridos de un árbol binario: preorden, inorden y postorden, de forma recursiva e iterativa. Verificar que el recorrido inorden de un BST produce los elementos en orden ascendente.

**13.** Implementar un árbol AVL que mantenga el balance automáticamente mediante rotaciones. Demostrar que la altura con $n$ nodos es siempre $O(\log n)$ insertando 1,000 elementos y midiendo la altura resultante vs. un BST no balanceado.

**14.** Implementar un montículo binario mínimo con inserción y extracción del mínimo. Usarlo para implementar el algoritmo de Huffman: dado un texto en español, construir el árbol, generar los códigos de cada carácter y calcular la tasa de compresión.

**15.** Implementar un trie (árbol de prefijos) para almacenar palabras del español. Implementar búsqueda exacta, búsqueda por prefijo (autocompletar) y conteo de palabras que comienzan con un prefijo dado. Probar con un vocabulario de 10,000 palabras.

## Grafos

**16.** Representar el mapa del Metro CDMX como un grafo no dirigido. Implementar BFS para encontrar la ruta con menor número de estaciones entre dos estaciones dadas. Imprimir el camino completo y el número de transbordos.

**17.** Modelar la red de carreteras entre las capitales de los 32 estados de México como grafo ponderado (distancia en km). Implementar Dijkstra para encontrar la ruta más corta entre cualquier par de ciudades.

**18.** Usando la misma red de capitales, implementar Kruskal para encontrar el árbol de expansión mínima: la red de menor longitud total que conecte todas las capitales. ¿Cuántos km de carretera se necesitan en total?

**19.** Implementar Floyd-Warshall para calcular la distancia más corta entre todos los pares de nodos. Identificar la ciudad "más central": aquella con menor distancia máxima a cualquier otra ciudad de la red.

**20.** Detectar ciclos en un grafo dirigido usando DFS con coloración de nodos. Aplicarlo para verificar que un conjunto de dependencias entre módulos de software no tiene dependencias circulares (el grafo de dependencias debe ser un DAG).

## Algoritmos sobre Cadenas

**21.** Implementar el algoritmo KMP para búsqueda de patrones. Comparar su velocidad con búsqueda ingenua buscando una secuencia de ADN de 20 nucleótidos dentro de un genoma de 1,000,000 de bases. Medir comparaciones realizadas por cada algoritmo.

**22.** Calcular la distancia de Levenshtein entre dos palabras. Construir un corrector ortográfico que sugiera las 3 palabras más cercanas a una palabra mal escrita, consultando un diccionario de 50,000 palabras del español mexicano.

**23.** Encontrar la subcadena palíndroma más larga en un texto usando programación dinámica. Probar con discursos de figuras históricas mexicanas. ¿Cuál es el palíndromo más largo que aparece naturalmente en el texto?

## Algoritmos con Complejidad Avanzada

**24.** Implementar el problema de la mochila 0/1 con programación dinámica. Una mochila de 15 kg debe llenarse con equipos de laboratorio con pesos y valores específicos; maximizar el valor total sin exceder el límite de peso.

**25.** Implementar una máquina de estados finita (DFA) para validar: a) CURP (18 caracteres), b) RFC persona física (13 caracteres), c) RFC persona moral (12 caracteres). El autómata debe rechazar cualquier cadena que no cumpla el formato oficial de la SEP/SAT.

**26.** Implementar la Transformada Rápida de Fourier (FFT) iterativa. Usarla para analizar frecuencias de una señal de audio muestreada a 44,100 Hz y detectar las frecuencias dominantes de un tono musical dado.

**27.** Implementar un generador de números pseudoaleatorios por congruencia lineal: $X_{n+1} = (aX_n + c) \bmod m$. Verificar la calidad de la distribución con una prueba chi-cuadrada sobre 100,000 muestras generadas.

---

## Problemas adicionales

> *Problemas de mayor complejidad para estudiantes avanzados.*

**28.** Implementar un árbol de segmentos con actualización puntual y consulta de rango (suma, mínimo, máximo) en $O(\log n)$. Usarlo para responder 1,000,000 de consultas de suma sobre un arreglo de 100,000 calificaciones de estudiantes.

**29.** Implementar el algoritmo de Tarjan para componentes fuertemente conexas. Aplicarlo para identificar grupos de páginas web que se enlazan mutuamente en un grafo de hipervínculos con 10,000 nodos.

**30.** Implementar una caché LRU de tamaño $k$ usando tabla hash y lista doblemente enlazada con operaciones en $O(1)$. Simular acceso a 10,000 páginas web y calcular la tasa de aciertos para $k = 100, 500, 1000$.

**31.** Resolver el TSP (viajante de comercio) para 15 ciudades de la República Mexicana usando: a) fuerza bruta, b) vecino más cercano, c) 2-opt de mejora local. Comparar calidad de soluciones y tiempo de cómputo de cada enfoque.

**32.** Implementar el algoritmo de Aho-Corasick para búsqueda simultánea de múltiples patrones. Usarlo para detectar en un documento todas las apariciones de los nombres de los 32 estados de México en una sola pasada del texto.
