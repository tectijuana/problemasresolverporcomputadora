# Capítulo 13: Paradigmas de Programación

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

Un paradigma de programación es una forma de pensar sobre los problemas y de estructurar las soluciones. Los paradigmas imperativos, orientados a objetos, funcionales, lógicos y declarativos no son lenguajes: son filosofías. Los mejores programadores de 2026 no son "programadores de Python" o "programadores de JavaScript" — son programadores que saben elegir el paradigma correcto para cada problema. Este capítulo explora los paradigmas fundamentales con problemas concretos que muestran cuándo y por qué cada uno brilla.

> **Distribución sugerida (4 sesiones × 4 horas):**
> Sesión 1 — Conceptos funcionales (P1–P8) y lenguajes funcionales puros (P9–P14) · Sesión 2 — Lógica general y CSP (P15–P19) · Sesión 3 — Prolog/Datalog/ASP (P20–P25) · Sesión 4 — Metaprogramación y proyectos integradores (P26–P34)

---

## Programación Funcional

> *Problemas P1–P8: resolubles en cualquier lenguaje. P9–P14 exigen Erlang, Elixir o Haskell.*

**1.** Implementar una función `suma_lista` que calcule la suma de una lista de números usando recursión pura, sin bucles ni variables mutables. Luego implementarla usando `reduce`. Comparar la legibilidad y el rendimiento de ambas versiones para listas de 10, 1,000 y 100,000 elementos.

**2.** Dado un padrón electoral simulado de 1,000,000 de registros con campos nombre, estado, edad y partido preferido, usar solo `map`, `filter` y `reduce` para calcular: a) la edad promedio de votantes mayores de 30 en Baja California, b) el partido con más simpatizantes menores de 25 años.

**3.** Implementar una función de composición `compose(f, g)` que devuelva una nueva función $h(x) = f(g(x))$. Usarla para construir un pipeline de transformación de texto: eliminar acentos → convertir a minúsculas → eliminar signos → dividir en palabras → contar frecuencias.

**4.** Implementar memoización genérica como decorador o función de orden superior. Aplicarla a la función de Fibonacci recursiva y medir la aceleración para `fib(40)` con y sin memoización.

**5.** Implementar una función `flat_map` (también llamada `bind` o `chain`) que aplique una función que devuelve una lista a cada elemento de una lista y aplane el resultado. Usarla para generar todos los pares $(a, b)$ con $a \in \{1..5\}$, $b \in \{1..5\}$, $a < b$.

**6.** Implementar un sistema de procesamiento de datos de ventas de una tienda OXXO usando solo funciones puras: leer CSV de ventas diarias → filtrar ventas con descuento → calcular impuesto IVA → agrupar por categoría → ordenar por total. Ninguna función debe modificar su entrada.

**7.** Implementar la función `unfold`: dado un valor inicial y una función de paso, generar una secuencia perezosa. Usarla para generar la secuencia de Fibonacci, la de números primos y la de Collatz para un número dado.

**8.** Construir un evaluador de expresiones matemáticas usando funciones puras y recursión. La entrada es una cadena como `"3 + 4 * (2 - 1)"` y la salida el resultado numérico. Sin variables globales ni efectos secundarios.

---

## Programación Funcional con Erlang, Elixir y Haskell

> *Usar Erlang/OTP (erlang.org), Elixir (elixir-lang.org) y GHC Haskell (haskell.org/ghc) — todos libres y multiplataforma. Los problemas de Erlang y Elixir comparten la misma VM (BEAM); los conceptos aprendidos en uno se transfieren directamente al otro.*

**9.** En **Erlang**, implementar `suma/1`, `maximo/1`, `filtrar/2`, `mapear/2` y `reducir/3` usando exclusivamente pattern matching y recursión de cola (*tail recursion*) — sin tocar el módulo `lists`. Verificar que son tail-recursive: deben procesar listas de 10,000,000 de elementos sin desbordamiento de pila. Medir el tiempo de ejecución y comparar con las versiones equivalentes del módulo `lists` de la biblioteca estándar.

**10.** En **Erlang**, implementar un sistema de monitoreo de sismos del CENAPRED usando el modelo de actores: cada sensor es un proceso Erlang que envía mensajes `{lectura, Magnitud, Timestamp}` al proceso coordinador cada segundo. Si un proceso sensor cae (simularlo con `exit(Pid, kill)`), un supervisor OTP con estrategia `one_for_one` lo reinicia automáticamente. Demostrar el principio *"let it crash"*: el sistema debe seguir funcionando aunque fallen hasta el 50% de los sensores simultáneamente.

**11.** En **Erlang**, construir un `GenServer` OTP que mantenga el estado del sistema de calificaciones del TecNM: `handle_call` para consultas síncronas (obtener promedio de un alumno), `handle_cast` para actualizaciones asíncronas (registrar calificación). Implementar `terminate/2` para persistir el estado en disco al detenerse y `init/1` para recuperarlo al arrancar. El servidor debe tolerar 1,000 llamadas concurrentes sin condición de carrera.

**12.** En **Elixir**, procesar el padrón de proveedores del gobierno federal (1,000,000 de registros en CSV) usando exclusivamente el operador pipe `|>` y el módulo `Stream` (evaluación perezosa): leer → filtrar activos → normalizar RFC → agrupar por entidad federativa → calcular monto total de contratos → ordenar descendente. El uso de memoria debe permanecer constante (menos de 50 MB) independientemente del tamaño del archivo — demostrar con `:observer.start()`.

**13.** En **Elixir**, construir un sistema de gestión de turnos para módulos del SAT usando `GenServer` y `DynamicSupervisor`: cada módulo de atención es un proceso supervisado; el supervisor crea y elimina módulos dinámicamente según la demanda. Implementar: `agregar_contribuyente/2` (encola en el módulo con menor espera), `llamar_siguiente/1`, `tiempo_espera_estimado/1` (promedio histórico del módulo) y `reporte_atencion/0` (estadísticas globales en tiempo real).

**14.** En **Haskell**, modelar el sistema de cuentas del IMSS usando tipos algebraicos de datos: `data Cuenta = Individual RFC Saldo | Empresarial RFC [RFC] Saldo | Suspendida RFC Motivo`. Implementar la type class `Consultable` con instancias para cada constructor. Usar `Maybe Cuenta` para búsquedas que pueden no encontrar resultados y `Either String Saldo` para operaciones que pueden fallar con mensaje descriptivo. El sistema de tipos de Haskell debe hacer imposible en tiempo de compilación operar sobre una cuenta suspendida sin manejar ese caso explícitamente.

---

## Programación Lógica y Declarativa

> *Los problemas P15–P19 pueden resolverse en cualquier lenguaje. Los problemas P20–P25 exigen Prolog, Datalog o ASP.*

**15.** Implementar en Python o cualquier lenguaje imperativo un motor de inferencia simple basado en reglas de la forma `si A y B entonces C`. Cargar reglas de elegibilidad para el programa Sembrando Vida de la SADER (criterios de superficie, cultivo y ubicación) e inferir si un productor dado es elegible.

**16.** Representar el árbol genealógico de una familia mexicana de 4 generaciones usando hechos y reglas en cualquier lenguaje. Implementar consultas: ¿quién es el abuelo paterno de X? ¿Cuáles primos tienen más de 5 años de diferencia? ¿Quiénes son los hermanos de X?

**17.** Implementar el problema de coloración de mapas como un CSP (*Constraint Satisfaction Problem*): dado el mapa de los estados de la República Mexicana y sus fronteras, colorear con 4 colores de manera que ningún par de estados fronterizos tenga el mismo color. Usar backtracking con propagación de restricciones (arco-consistencia AC-3).

**18.** Implementar un solucionador de Sudoku usando CSP con backtracking y las tres reglas de propagación: nodo-consistencia, arco-consistencia y consistencia de camino. Medir cuántas posiciones se resuelven por propagación pura (sin backtracking).

**19.** Construir un sistema de consultas tipo SQL sobre una lista de diccionarios en Python, implementando: `SELECT` (proyección), `WHERE` (filtro), `ORDER BY`, `GROUP BY` y `JOIN` entre dos colecciones. Probar con una base de datos de alumnos del TecNM y sus calificaciones.

---

## Programación Lógica con Prolog, Datalog y ASP

> *Usar SWI-Prolog (swi-prolog.org), Soufflé (souffle-lang.github.io) y Clingo (potassco.github.io/clingo) según el problema. Todos son libres y multiplataforma.*

**20.** En SWI-Prolog, definir los hechos y reglas del Metro de la Ciudad de México: `estacion/2` (nombre, línea), `conecta/3` (estación_A, estación_B, línea). Implementar el predicado `ruta/3` que encuentre, por backtracking, todas las rutas posibles entre dos estaciones incluyendo transbordos. Consultar: ¿cuántas rutas distintas existen de Pantitlán a Bellas Artes con máximo 2 transbordos?

**21.** En SWI-Prolog, modelar las relaciones familiares de una familia mexicana de 4 generaciones con los hechos `padre/2` y `madre/2`. Definir con reglas: `abuelo/2`, `abuela/2`, `tio/2`, `prima/2`, `hermano/2` y `descendiente/2` (recursivo). Demostrar el uso del corte (`!`) para evitar respuestas duplicadas y de la negación por fallo (`\+`) para el predicado `no_emparentados/2`.

**22.** En SWI-Prolog, implementar los predicados clásicos de listas desde cero: `mi_member/2`, `mi_append/3`, `mi_length/2`, `mi_reverse/2`, `mi_nth/3`, `mi_flatten/2` y `mi_permutation/2`. Usarlos para resolver: dado el plan de estudios ISC del TecNM, ¿cuántas ordenaciones distintas de las materias del primer semestre son posibles si Cálculo Diferencial debe ir antes que Cálculo Integral?

**23.** En SWI-Prolog con la biblioteca `clpfd`, resolver la asignación de horarios de exámenes del TecNM: 8 materias, 4 salones, 2 turnos (mañana/tarde). Restricciones: ningún alumno inscrito en dos materias puede tener examen en el mismo turno y salón; cada salón aloja máximo 2 exámenes por turno. Comparar el código CLP(FD) con la solución de backtracking puro del P18 — ¿cuántas líneas menos?

**24.** En **Datalog** (usando Soufflé o cualquier motor Datalog), declarar los hechos de prerequisitos del plan de estudios ISC del TecNM: `prerequisito(materia_A, materia_B)` significa que A debe aprobarse antes que B. Escribir reglas para calcular: a) el cierre transitivo `prerequisito_transitivo/2`, b) el conjunto de materias que deben aprobarse antes de poder inscribir Residencias Profesionales, c) si existe algún ciclo en el grafo de prerequisitos.

**25.** En **ASP** (Answer Set Programming con Clingo), resolver la asignación de salones para el semestre del TecNM: hechos de materias (nombre, alumnos inscritos, horas_semana), salones (nombre, capacidad) y docentes (nombre, materias_que_imparte). Restricciones: ningún docente puede estar en dos salones a la misma hora, ningún salón puede tener más alumnos que su capacidad, cada materia tiene exactamente un salón asignado. Encontrar la asignación que maximiza el uso de los salones disponibles.

---

## Metaprogramación y Aspectos

**26.** Implementar un sistema de decoradores que agreguen comportamiento transversal a funciones: a) `@log` que registra cada llamada con sus argumentos y resultado, b) `@cache` que memoriza resultados, c) `@retry(n)` que reintenta $n$ veces si ocurre una excepción, d) `@timeout(s)` que cancela la ejecución si tarda más de $s$ segundos.

**27.** Implementar un sistema de serialización automática: dada una clase cualquiera, generar automáticamente los métodos `to_json()`, `from_json()`, `to_csv()` y `__repr__()` mediante inspección de los atributos de la clase en tiempo de ejecución.

**28.** Construir un mini-ORM (mapeador objeto-relacional) que permita definir clases Python y automáticamente: crear la tabla SQL correspondiente, generar métodos `save()`, `find_by_id()`, `find_all()` y `delete()`. Probar con las clases `Alumno`, `Materia` e `Inscripcion`.

**29.** Implementar un sistema de validación declarativa: decorar los atributos de una clase con restricciones (`@rango(0,100)`, `@no_vacio`, `@formato_curp`, `@positivo`) y que el sistema valide automáticamente al asignar valores. Cualquier violación lanza una excepción descriptiva.

**30.** Construir un generador de código que, dado un esquema JSON que describe una API REST (rutas, métodos, parámetros, respuestas), genere automáticamente el código boilerplate del servidor en Python/Flask y el cliente en JavaScript.

---

## Problemas adicionales

> *Proyectos integradores que combinan múltiples paradigmas.*

**31.** Implementar el patrón de *transductor*: una composición de transformaciones (map, filter, take) que opera sobre cualquier fuente de datos (lista, archivo, stream) sin crear colecciones intermedias. Demostrar que procesa 10,000,000 de registros usando memoria constante. Implementarlo en Python y comparar el diseño con la versión equivalente en Elixir usando `Stream`.

**32.** Diseñar un DSL (lenguaje de dominio específico) embebido para describir horarios escolares del TecNM: cursos, salones, profesores y restricciones (mismo profesor no puede estar en dos salones a la vez, estudiante no puede tener dos clases simultáneas). Implementarlo en Python con metaprogramación y en Elixir con macros. Comparar la expresividad de ambos enfoques.

**33.** Implementar un sistema de continuaciones (*continuations*) para manejar flujos de control complejos: implementar `call/cc` básico en Python usando excepciones o corrutinas. Comparar con el modelo de actores de Erlang — ¿qué problemas se resuelven más naturalmente con continuaciones y cuáles con paso de mensajes?

**34.** Construir un framework de pruebas unitarias funcional: `describe`, `it`, `expect`, `beforeEach` — similar a Jest — implementado puramente con funciones de orden superior, sin clases. Implementarlo en Python y en Elixir. El framework debe reportar pruebas pasadas, fallidas y el error exacto de cada falla.
