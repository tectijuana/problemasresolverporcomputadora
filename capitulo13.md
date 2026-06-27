# Capítulo 13: Paradigmas de Programación

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

Un paradigma de programación es una forma de pensar sobre los problemas y de estructurar las soluciones. Los paradigmas imperativos, orientados a objetos, funcionales, lógicos y declarativos no son lenguajes: son filosofías. Los mejores programadores de 2026 no son "programadores de Python" o "programadores de JavaScript" — son programadores que saben elegir el paradigma correcto para cada problema. Este capítulo explora cuatro paradigmas fundamentales con problemas concretos que muestran cuándo y por qué cada uno brilla.

## Programación Funcional

**1.** Implementar una función `suma_lista` que calcule la suma de una lista de números usando recursión pura, sin bucles ni variables mutables. Luego implementarla usando `reduce`. Comparar la legibilidad y el rendimiento de ambas versiones para listas de 10, 1,000 y 100,000 elementos.

**2.** Dado un padrón electoral simulado de 1,000,000 de registros con campos nombre, estado, edad y partido preferido, usar solo `map`, `filter` y `reduce` para calcular: a) la edad promedio de votantes mayores de 30 en Baja California, b) el partido con más simpatizantes menores de 25 años.

**3.** Implementar una función de composición `compose(f, g)` que devuelva una nueva función $h(x) = f(g(x))$. Usarla para construir un pipeline de transformación de texto: eliminar acentos → convertir a minúsculas → eliminar signos → dividir en palabras → contar frecuencias.

**4.** Implementar memoización genérica como decorador o función de orden superior. Aplicarla a la función de Fibonacci recursiva y medir la aceleración para `fib(40)` con y sin memoización.

**5.** Implementar una función `flat_map` (también llamada `bind` o `chain`) que aplique una función que devuelve una lista a cada elemento de una lista y aplane el resultado. Usarla para generar todos los pares de números $(a, b)$ con $a \in \{1..5\}$, $b \in \{1..5\}$, $a < b$.

**6.** Implementar un sistema de procesamiento de datos de ventas de una tienda OXXO usando solo funciones puras: leer CSV de ventas diarias → filtrar ventas con descuento → calcular impuesto IVA → agrupar por categoría → ordenar por total. Ninguna función debe modificar su entrada.

**7.** Implementar la función `unfold`: dado un valor inicial y una función de paso, generar una secuencia perezosa. Usarla para generar la secuencia de números de Fibonacci, la de números primos y la de colatz para un número dado.

**8.** Construir un evaluador de expresiones matemáticas usando funciones puras y recursión. La entrada es una cadena como `"3 + 4 * (2 - 1)"` y la salida el resultado numérico. Sin variables globales ni efectos secundarios.

## Programación Lógica y Declarativa

**9.** Implementar en Python o cualquier lenguaje imperativo un motor de inferencia simple basado en reglas de la forma `si A y B entonces C`. Cargar reglas de elegibilidad para el programa Sembrando Vida de la SADER (criterios de superficie, cultivo y ubicación) e inferir si un productor dado es elegible.

**10.** Representar el árbol genealógico de una familia mexicana de 4 generaciones usando hechos y reglas. Implementar consultas: ¿quién es el abuelo paterno de X? ¿Cuáles primos tienen más de 5 años de diferencia? ¿Quiénes son los hermanos de X?

**11.** Implementar el problema de coloración de mapas como un problema de satisfacción de restricciones (CSP): dado el mapa de los estados de la República Mexicana y sus fronteras, colorear el mapa con 4 colores de manera que ningún par de estados fronterizos tenga el mismo color. Usar backtracking con propagación de restricciones.

**12.** Implementar un solucionador de Sudoku usando CSP con backtracking y las tres reglas de propagación: nodo-consistencia, arco-consistencia y consistencia de camino. Medir cuántas posiciones se resuelven por propagación pura (sin backtracking).

**13.** Construir un sistema de consultas tipo SQL sobre una lista de diccionarios en Python, implementando: `SELECT` (proyección), `WHERE` (filtro), `ORDER BY`, `GROUP BY` y `JOIN` entre dos colecciones. Probar con una base de datos de alumnos del TecNM y sus calificaciones.

## Metaprogramación y Aspectos

**14.** Implementar un sistema de decoradores que agreguen comportamiento transversal a funciones: a) `@log` que registra cada llamada con sus argumentos y resultado, b) `@cache` que memoriza resultados, c) `@retry(n)` que reintenta $n$ veces si ocurre una excepción, d) `@timeout(s)` que cancela la ejecución si tarda más de $s$ segundos.

**15.** Implementar un sistema de serialización automática: dada una clase cualquiera, generar automáticamente los métodos `to_json()`, `from_json()`, `to_csv()` y `__repr__()` mediante inspección de los atributos de la clase en tiempo de ejecución.

**16.** Construir un mini-ORM (mapeador objeto-relacional) que permita definir clases Python y automáticamente: crear la tabla SQL correspondiente, generar métodos `save()`, `find_by_id()`, `find_all()` y `delete()`. Probar con las clases `Alumno`, `Materia` y `Inscripcion`.

**17.** Implementar un sistema de validación declarativa: decorar los atributos de una clase con restricciones (`@rango(0,100)`, `@no_vacio`, `@formato_curp`, `@positivo`) y que el sistema valide automáticamente al asignar valores. Cualquier violación lanza una excepción descriptiva.

**18.** Construir un generador de código que, dado un esquema JSON que describe una API REST (rutas, métodos, parámetros, respuestas), genere automáticamente el código boilerplate del servidor en Python/Flask y el cliente en JavaScript.

---

## Problemas adicionales

> *Problemas integradores que combinan múltiples paradigmas.*

**19.** Implementar el patrón de *transductor*: una composición de transformaciones (map, filter, take) que opera sobre cualquier fuente de datos (lista, archivo, stream) sin crear colecciones intermedias. Demostrar que procesa 10,000,000 de registros usando memoria constante.

**20.** Diseñar un DSL (lenguaje de dominio específico) embebido en Python para describir horarios escolares del TecNM: cursos, salones, profesores y restricciones (mismo profesor no puede estar en dos salones a la vez, estudiante no puede tener dos clases simultáneas). El sistema debe detectar y reportar conflictos.

**21.** Implementar un sistema de continuaciones (*continuations*) para manejar flujos de control complejos: implementar `call/cc` básico en Python usando excepciones o corrutinas, y usarlo para implementar backtracking y generadores perezosos.

**22.** Construir un framework de pruebas unitarias funcional: `describe`, `it`, `expect`, `beforeEach` — similar a Jest — implementado puramente con funciones de orden superior, sin clases. El framework debe reportar pruebas pasadas, fallidas y el error exacto de cada falla.
