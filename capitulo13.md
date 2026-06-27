# Capítulo 13: Paradigmas de Programación

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

Un paradigma de programación es una forma de pensar sobre los problemas y de estructurar las soluciones. Los paradigmas imperativos, orientados a objetos, funcionales, lógicos y declarativos no son lenguajes: son filosofías. Los mejores programadores de 2026 no son "programadores de Python" o "programadores de JavaScript" — son programadores que saben elegir el paradigma correcto para cada problema. Este capítulo explora cinco paradigmas fundamentales con problemas concretos que muestran cuándo y por qué cada uno brilla.

> **Distribución sugerida (4 sesiones × 4 horas):**
> Sesión 1 — Funcional (P1–P8) · Sesión 2 — Lógico general (P9–P13) · Sesión 3 — Prolog/Datalog/ASP (P14–P19) · Sesión 4 — Metaprogramación y proyectos integradores (P20–P28)

---

## Programación Funcional

**1.** Implementar una función `suma_lista` que calcule la suma de una lista de números usando recursión pura, sin bucles ni variables mutables. Luego implementarla usando `reduce`. Comparar la legibilidad y el rendimiento de ambas versiones para listas de 10, 1,000 y 100,000 elementos.

**2.** Dado un padrón electoral simulado de 1,000,000 de registros con campos nombre, estado, edad y partido preferido, usar solo `map`, `filter` y `reduce` para calcular: a) la edad promedio de votantes mayores de 30 en Baja California, b) el partido con más simpatizantes menores de 25 años.

**3.** Implementar una función de composición `compose(f, g)` que devuelva una nueva función $h(x) = f(g(x))$. Usarla para construir un pipeline de transformación de texto: eliminar acentos → convertir a minúsculas → eliminar signos → dividir en palabras → contar frecuencias.

**4.** Implementar memoización genérica como decorador o función de orden superior. Aplicarla a la función de Fibonacci recursiva y medir la aceleración para `fib(40)` con y sin memoización.

**5.** Implementar una función `flat_map` (también llamada `bind` o `chain`) que aplique una función que devuelve una lista a cada elemento de una lista y aplane el resultado. Usarla para generar todos los pares $(a, b)$ con $a \in \{1..5\}$, $b \in \{1..5\}$, $a < b$.

**6.** Implementar un sistema de procesamiento de datos de ventas de una tienda OXXO usando solo funciones puras: leer CSV de ventas diarias → filtrar ventas con descuento → calcular impuesto IVA → agrupar por categoría → ordenar por total. Ninguna función debe modificar su entrada.

**7.** Implementar la función `unfold`: dado un valor inicial y una función de paso, generar una secuencia perezosa. Usarla para generar la secuencia de Fibonacci, la de números primos y la de Collatz para un número dado.

**8.** Construir un evaluador de expresiones matemáticas usando funciones puras y recursión. La entrada es una cadena como `"3 + 4 * (2 - 1)"` y la salida el resultado numérico. Sin variables globales ni efectos secundarios.

---

## Programación Lógica y Declarativa

> *Los problemas P9–P13 pueden resolverse en cualquier lenguaje. Los problemas P14–P19 exigen Prolog, Datalog o ASP.*

**9.** Implementar en Python o cualquier lenguaje imperativo un motor de inferencia simple basado en reglas de la forma `si A y B entonces C`. Cargar reglas de elegibilidad para el programa Sembrando Vida de la SADER (criterios de superficie, cultivo y ubicación) e inferir si un productor dado es elegible.

**10.** Representar el árbol genealógico de una familia mexicana de 4 generaciones usando hechos y reglas en cualquier lenguaje. Implementar consultas: ¿quién es el abuelo paterno de X? ¿Cuáles primos tienen más de 5 años de diferencia? ¿Quiénes son los hermanos de X?

**11.** Implementar el problema de coloración de mapas como un CSP (*Constraint Satisfaction Problem*): dado el mapa de los estados de la República Mexicana y sus fronteras, colorear con 4 colores de manera que ningún par de estados fronterizos tenga el mismo color. Usar backtracking con propagación de restricciones (arco-consistencia AC-3).

**12.** Implementar un solucionador de Sudoku usando CSP con backtracking y las tres reglas de propagación: nodo-consistencia, arco-consistencia y consistencia de camino. Medir cuántas posiciones se resuelven por propagación pura (sin backtracking).

**13.** Construir un sistema de consultas tipo SQL sobre una lista de diccionarios en Python, implementando: `SELECT` (proyección), `WHERE` (filtro), `ORDER BY`, `GROUP BY` y `JOIN` entre dos colecciones. Probar con una base de datos de alumnos del TecNM y sus calificaciones.

---

## Programación Lógica con Prolog, Datalog y ASP

> *Usar SWI-Prolog (swi-prolog.org), Soufflé (souffle-lang.github.io) y Clingo (potassco.github.io/clingo) según el problema. Todas son herramientas libres y multiplataforma.*

**14.** En SWI-Prolog, definir los hechos y reglas del Metro de la Ciudad de México: `estacion/2` (nombre, línea), `conecta/3` (estación_A, estación_B, línea). Implementar el predicado `ruta/3` que encuentre, por backtracking, todas las rutas posibles entre dos estaciones incluyendo transbordos. Consultar: ¿cuántas rutas distintas existen de Pantitlán a Bellas Artes con máximo 2 transbordos?

**15.** En SWI-Prolog, modelar las relaciones familiares de una familia mexicana de 4 generaciones con los hechos `padre/2` y `madre/2`. Definir con reglas: `abuelo/2`, `abuela/2`, `tio/2`, `prima/2`, `hermano/2` y `descendiente/2` (recursivo). Demostrar el uso del corte (`!`) para evitar respuestas duplicadas y de la negación por fallo (`\+`) para el predicado `no_emparentados/2`.

**16.** En SWI-Prolog, implementar los predicados clásicos de listas desde cero: `mi_member/2`, `mi_append/3`, `mi_length/2`, `mi_reverse/2`, `mi_nth/3`, `mi_flatten/2` y `mi_permutation/2`. Usarlos para resolver: dado el plan de estudios de ISC del TecNM, ¿cuántas ordenaciones distintas de las materias del primer semestre son posibles si Cálculo Diferencial debe ir antes que Cálculo Integral?

**17.** En SWI-Prolog con la biblioteca `clpfd` (Constraint Logic Programming over Finite Domains), resolver la asignación de horarios de exámenes del TecNM: 8 materias, 4 salones, 2 turnos (mañana/tarde). Restricciones: ningún alumno inscrito en dos materias puede tener examen en el mismo turno y salón; cada salón aloja máximo 2 exámenes por turno. Comparar el código CLP(FD) con la solución de backtracking puro del P12 — ¿cuántas líneas menos?

**18.** En **Datalog** (usando Soufflé o cualquier motor Datalog), declarar los hechos de prerequisitos del plan de estudios ISC del TecNM: `prerequisito(materia_A, materia_B)` significa que A debe aprobarse antes que B. Escribir reglas para calcular: a) el cierre transitivo `prerequisito_transitivo/2`, b) el conjunto de materias que deben aprobarse antes de poder inscribir Residencias Profesionales, c) si existe algún ciclo en el grafo de prerequisitos (que sería un error en el plan de estudios).

**19.** En **ASP** (Answer Set Programming con Clingo), resolver la asignación de salones para el semestre del TecNM como un problema de optimización: hechos de materias (nombre, alumnos inscritos, horas_semana), salones (nombre, capacidad) y docentes (nombre, materias_que_imparte). Restricciones de integridad: ningún docente puede estar en dos salones a la misma hora, ningún salón puede tener más alumnos que su capacidad, cada materia tiene exactamente un salón asignado. Encontrar la asignación que maximiza el uso de los salones disponibles.

---

## Metaprogramación y Aspectos

**20.** Implementar un sistema de decoradores que agreguen comportamiento transversal a funciones: a) `@log` que registra cada llamada con sus argumentos y resultado, b) `@cache` que memoriza resultados, c) `@retry(n)` que reintenta $n$ veces si ocurre una excepción, d) `@timeout(s)` que cancela la ejecución si tarda más de $s$ segundos.

**21.** Implementar un sistema de serialización automática: dada una clase cualquiera, generar automáticamente los métodos `to_json()`, `from_json()`, `to_csv()` y `__repr__()` mediante inspección de los atributos de la clase en tiempo de ejecución.

**22.** Construir un mini-ORM (mapeador objeto-relacional) que permita definir clases Python y automáticamente: crear la tabla SQL correspondiente, generar métodos `save()`, `find_by_id()`, `find_all()` y `delete()`. Probar con las clases `Alumno`, `Materia` e `Inscripcion`.

**23.** Implementar un sistema de validación declarativa: decorar los atributos de una clase con restricciones (`@rango(0,100)`, `@no_vacio`, `@formato_curp`, `@positivo`) y que el sistema valide automáticamente al asignar valores. Cualquier violación lanza una excepción descriptiva.

**24.** Construir un generador de código que, dado un esquema JSON que describe una API REST (rutas, métodos, parámetros, respuestas), genere automáticamente el código boilerplate del servidor en Python/Flask y el cliente en JavaScript.

---

## Problemas adicionales

> *Proyectos integradores que combinan múltiples paradigmas.*

**25.** Implementar el patrón de *transductor*: una composición de transformaciones (map, filter, take) que opera sobre cualquier fuente de datos (lista, archivo, stream) sin crear colecciones intermedias. Demostrar que procesa 10,000,000 de registros usando memoria constante.

**26.** Diseñar un DSL (lenguaje de dominio específico) embebido en Python para describir horarios escolares del TecNM: cursos, salones, profesores y restricciones (mismo profesor no puede estar en dos salones a la vez, estudiante no puede tener dos clases simultáneas). El sistema debe detectar y reportar conflictos.

**27.** Implementar un sistema de continuaciones (*continuations*) para manejar flujos de control complejos: implementar `call/cc` básico en Python usando excepciones o corrutinas, y usarlo para implementar backtracking y generadores perezosos.

**28.** Construir un framework de pruebas unitarias funcional: `describe`, `it`, `expect`, `beforeEach` — similar a Jest — implementado puramente con funciones de orden superior, sin clases. El framework debe reportar pruebas pasadas, fallidas y el error exacto de cada falla.
