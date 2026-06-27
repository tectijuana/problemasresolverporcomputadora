# Capítulo 13: Paradigmas de Programación

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

Un paradigma de programación es una forma de pensar sobre los problemas y de estructurar las soluciones. Los paradigmas imperativos, orientados a objetos, funcionales, lógicos y declarativos no son lenguajes: son filosofías. Los mejores programadores de 2026 no son "programadores de Python" o "programadores de JavaScript" — son programadores que saben elegir el paradigma correcto para cada problema. Este capítulo explora los paradigmas fundamentales con sus lenguajes canónicos, desde los conceptos universales hasta las herramientas que hoy usan Meta, Jane Street y Nubank.

> **Distribución sugerida (4 sesiones × 4 horas):**
> Sesión 1 — Funcional general + BEAM + Haskell (P1–P14) · Sesión 2 — OCaml + Clojure (P15–P24) · Sesión 3 — Lógica general + Prolog/Datalog/ASP (P25–P35) · Sesión 4 — Metaprogramación y proyectos integradores (P36–P44)

---

## Programación Funcional

> *P1–P8: resolubles en cualquier lenguaje. Establece los conceptos que los lenguajes siguientes implementan de forma nativa.*

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

> *Usar Erlang/OTP (erlang.org), Elixir (elixir-lang.org) y GHC Haskell (haskell.org/ghc). Los problemas de Erlang y Elixir comparten la misma VM (BEAM); los conceptos aprendidos en uno se transfieren directamente al otro.*

**9.** En **Erlang**, implementar `suma/1`, `maximo/1`, `filtrar/2`, `mapear/2` y `reducir/3` usando exclusivamente pattern matching y recursión de cola (*tail recursion*) — sin el módulo `lists`. Verificar que son tail-recursive: deben procesar listas de 10,000,000 de elementos sin desbordamiento de pila. Medir el tiempo y comparar con las versiones de la biblioteca estándar.

**10.** En **Erlang**, implementar un sistema de monitoreo de sismos del CENAPRED usando el modelo de actores: cada sensor es un proceso Erlang que envía mensajes `{lectura, Magnitud, Timestamp}` al coordinador cada segundo. Si un sensor cae (simularlo con `exit(Pid, kill)`), un supervisor OTP con estrategia `one_for_one` lo reinicia automáticamente. Demostrar el principio *"let it crash"*: el sistema debe seguir funcionando aunque fallen hasta el 50% de los sensores simultáneamente.

**11.** En **Erlang**, construir un `GenServer` OTP que mantenga el estado del sistema de calificaciones del TecNM: `handle_call` para consultas síncronas, `handle_cast` para actualizaciones asíncronas. Implementar `terminate/2` para persistir el estado en disco al detenerse y `init/1` para recuperarlo al arrancar. El servidor debe tolerar 1,000 llamadas concurrentes sin condición de carrera.

**12.** En **Elixir**, procesar el padrón de proveedores del gobierno federal (1,000,000 de registros en CSV) usando exclusivamente el operador pipe `|>` y el módulo `Stream` (evaluación perezosa): leer → filtrar activos → normalizar RFC → agrupar por entidad federativa → calcular monto total → ordenar. El uso de memoria debe permanecer constante (menos de 50 MB) independientemente del tamaño del archivo — demostrar con `:observer.start()`.

**13.** En **Elixir**, construir un sistema de gestión de turnos para módulos del SAT usando `GenServer` y `DynamicSupervisor`: cada módulo de atención es un proceso supervisado; el supervisor crea y elimina módulos dinámicamente según la demanda. Implementar: `agregar_contribuyente/2`, `llamar_siguiente/1`, `tiempo_espera_estimado/1` y `reporte_atencion/0` (estadísticas globales en tiempo real).

**14.** En **Haskell**, modelar el sistema de cuentas del IMSS usando tipos algebraicos: `data Cuenta = Individual RFC Saldo | Empresarial RFC [RFC] Saldo | Suspendida RFC Motivo`. Implementar la type class `Consultable` con instancias para cada constructor. Usar `Maybe Cuenta` para búsquedas que pueden fallar y `Either String Saldo` para operaciones con error descriptivo. El sistema de tipos debe hacer imposible en tiempo de compilación operar sobre una cuenta suspendida sin manejar ese caso explícitamente.

---

## Programación Funcional con OCaml

> *Usar OCaml con Dune como sistema de build (ocaml.org · dune.build). OCaml es el lenguaje detrás de Hack, Flow e Infer en Meta/Facebook, del primer compilador de Rust, y de toda la infraestructura cuantitativa de Jane Street. Su sistema de módulos y functores no tiene equivalente en ningún otro lenguaje de uso general.*

**15.** En **OCaml**, implementar un evaluador de expresiones matemáticas usando tipos algebraicos de datos (`type expr = Num of float | Add of expr * expr | Mul of expr * expr | Neg of expr`). El pattern matching del compilador OCaml debe advertir con un error si algún caso queda sin cubrir — demostrar cómo esta garantía en tiempo de compilación elimina la clase entera de errores de "caso no manejado" que existen en Python o JavaScript. Extender el tipo con `Div of expr * expr` y observar qué casos nuevos exige el compilador manejar.

**16.** En **OCaml**, diseñar el sistema de calificaciones del TecNM usando el sistema de módulos: definir la firma `module type ALUMNO` con los tipos y funciones públicas (`.mli`), implementarla en dos módulos distintos (`AlumnoHashtbl` con tabla hash y `AlumnoArbol` con árbol rojo-negro), y escribir código cliente que funcione con cualquier implementación sin cambios. Demostrar que cambiar de implementación es una sola línea. Esto ilustra por qué Meta eligió OCaml para construir sistemas de tipos donde la abstracción es crítica.

**17.** En **OCaml**, implementar el funtor `MakeConjunto(Ord: ORDENABLE)` que crea un conjunto ordenado con operaciones `agregar`, `contiene`, `union`, `interseccion` y `diferencia`. Instanciarlo para tres tipos distintos: `ConjuntoMaterias` (strings), `ConjuntoCalificaciones` (enteros) y `ConjuntoFechas` (registros con año/mes/día). Demostrar que el funtor garantiza en tiempo de compilación que no se puede mezclar un `ConjuntoMaterias` con un `ConjuntoCalificaciones`.

**18.** En **OCaml**, implementar un verificador de tipos bidireccional simplificado al estilo de Flow o Hack — el mismo tipo de herramienta que usa Meta para detectar errores en millones de líneas de código. El lenguaje de entrada tiene: enteros, booleanos, funciones y aplicación de funciones. El verificador debe: a) *inferir* el tipo de expresiones sin anotaciones, b) *verificar* que las anotaciones explícitas son correctas, c) reportar errores con el mensaje `"se esperaba tipo T pero se encontró S en expresión E"`. Probar con al menos 10 expresiones válidas e inválidas.

**19.** En **OCaml**, implementar una caché LRU (*Least Recently Used*) de 100 entradas usando referencias (`ref`) y una lista doblemente enlazada mutable. Comparar esta implementación con una versión puramente funcional usando un árbol balanceado + mapa de timestamps. Medir: a) latencia de acceso para 1,000,000 operaciones, b) uso de memoria, c) líneas de código. Documentar en qué escenarios la mutabilidad controlada en OCaml justifica abandonar la pureza — y cuándo no.

---

## Programación Funcional con Clojure

> *Usar Clojure con Leiningen o deps.edn (clojure.org). Clojure es el lenguaje con el que Nubank — el banco digital más grande de América Latina, con millones de clientes en México — construyó toda su plataforma de crédito y pagos. Su modelo de estado inmutable con identidades explícitas resuelve una clase entera de bugs de concurrencia por diseño.*

**20.** En **Clojure**, demostrar el modelo de estructuras de datos persistentes: crear un mapa de cuenta bancaria `{:saldo 10000 :titular "García"}` y aplicar 10 operaciones sucesivas de depósito y retiro con `assoc` y `update`. Guardar cada versión intermedia en un vector. Demostrar que: a) ninguna operación modifica la versión anterior, b) todas las versiones históricas son accesibles en O(1), c) el uso de memoria total es $O(n \log n)$, no $O(n^2)$. Esto ilustra por qué Nubank eligió Clojure para sistemas de pagos donde la auditoría del historial es un requisito legal.

**21.** En **Clojure**, procesar el padrón de beneficiarios del programa Bienestar (1,000,000 registros) usando secuencias perezosas con `lazy-seq` y transductores compuestos con `comp`. El pipeline: filtrar activos → normalizar CURP → enriquecer con municipio → agrupar por estado → calcular estadísticas. Medir la memoria usada con `(.. Runtime/getRuntime totalMemory)` al inicio y al final — debe procesar todo el padrón sin cargar más de 50 MB en memoria simultáneamente.

**22.** En **Clojure**, simular el sistema de transferencias SPEI usando STM (*Software Transactional Memory*) con `ref` y `dosync`. Crear 50 cuentas con saldo inicial de \$10,000 MXN cada una. Lanzar 200 hilos simultáneos que realizan transferencias aleatorias entre cuentas. Al finalizar, verificar que: a) la suma total de saldos es idéntica al inicio (conservación), b) ninguna cuenta tiene saldo negativo, c) no ocurrió ningún deadlock. El STM de Clojure debe garantizar las tres propiedades sin un solo `lock` explícito en el código.

**23.** En **Clojure**, implementar las macros `mi-when`, `mi-unless`, `mi-cond` y `mi-and` usando `defmacro` y expansión de macros. Luego implementar la macro `defruta` que permite definir rutas de una API REST de forma declarativa: `(defruta :GET "/alumnos/:id" obtener-alumno)` debe expandirse en el código de registro del handler correspondiente. Usar `macroexpand-1` para inspeccionar la expansión y verificar que el código generado es correcto. Comparar el resultado con la biblioteca Compojure, que usa el mismo patrón.

**24.** En **Clojure** con `core.async`, construir un pipeline de procesamiento de pagos con tarjeta al estilo del sistema de Nubank: canal de entrada de transacciones → go block de validación de fondos → go block de detección de fraude (simular con latencia aleatoria de 10–100ms) → go block de autorización → canal de resultado. Usar `alts!` para implementar un timeout de 200ms: si la detección de fraude tarda más, la transacción se aprueba con bandera de revisión posterior. Medir el throughput: ¿cuántas transacciones por segundo procesa el pipeline con 8 workers?

---

## Programación Lógica y Declarativa

> *P25–P29: resolubles en cualquier lenguaje. P30–P35 exigen Prolog, Datalog o ASP.*

**25.** Implementar en Python o cualquier lenguaje imperativo un motor de inferencia simple basado en reglas de la forma `si A y B entonces C`. Cargar reglas de elegibilidad para el programa Sembrando Vida de la SADER (criterios de superficie, cultivo y ubicación) e inferir si un productor dado es elegible.

**26.** Representar el árbol genealógico de una familia mexicana de 4 generaciones usando hechos y reglas en cualquier lenguaje. Implementar consultas: ¿quién es el abuelo paterno de X? ¿Cuáles primos tienen más de 5 años de diferencia? ¿Quiénes son los hermanos de X?

**27.** Implementar el problema de coloración de mapas como un CSP: dado el mapa de los estados de la República Mexicana y sus fronteras, colorear con 4 colores de manera que ningún par de estados fronterizos tenga el mismo color. Usar backtracking con propagación de restricciones (arco-consistencia AC-3).

**28.** Implementar un solucionador de Sudoku usando CSP con backtracking y las tres reglas de propagación: nodo-consistencia, arco-consistencia y consistencia de camino. Medir cuántas posiciones se resuelven por propagación pura (sin backtracking).

**29.** Construir un sistema de consultas tipo SQL sobre una lista de diccionarios en Python, implementando: `SELECT` (proyección), `WHERE` (filtro), `ORDER BY`, `GROUP BY` y `JOIN` entre dos colecciones. Probar con una base de datos de alumnos del TecNM y sus calificaciones.

---

## Programación Lógica con Prolog, Datalog y ASP

> *Usar SWI-Prolog (swi-prolog.org), Soufflé (souffle-lang.github.io) y Clingo (potassco.github.io/clingo).*

**30.** En SWI-Prolog, definir los hechos y reglas del Metro de la Ciudad de México: `estacion/2` (nombre, línea), `conecta/3` (estación_A, estación_B, línea). Implementar el predicado `ruta/3` que encuentre, por backtracking, todas las rutas posibles entre dos estaciones incluyendo transbordos. Consultar: ¿cuántas rutas distintas existen de Pantitlán a Bellas Artes con máximo 2 transbordos?

**31.** En SWI-Prolog, modelar las relaciones familiares de una familia mexicana de 4 generaciones con los hechos `padre/2` y `madre/2`. Definir con reglas: `abuelo/2`, `abuela/2`, `tio/2`, `prima/2`, `hermano/2` y `descendiente/2` (recursivo). Demostrar el uso del corte (`!`) para evitar respuestas duplicadas y de la negación por fallo (`\+`) para el predicado `no_emparentados/2`.

**32.** En SWI-Prolog, implementar los predicados clásicos de listas desde cero: `mi_member/2`, `mi_append/3`, `mi_length/2`, `mi_reverse/2`, `mi_nth/3`, `mi_flatten/2` y `mi_permutation/2`. Usarlos para resolver: dado el plan de estudios ISC del TecNM, ¿cuántas ordenaciones distintas de las materias del primer semestre son posibles si Cálculo Diferencial debe ir antes que Cálculo Integral?

**33.** En SWI-Prolog con la biblioteca `clpfd`, resolver la asignación de horarios de exámenes del TecNM: 8 materias, 4 salones, 2 turnos (mañana/tarde). Restricciones: ningún alumno inscrito en dos materias puede tener examen en el mismo turno y salón; cada salón aloja máximo 2 exámenes por turno. Comparar el código CLP(FD) con la solución de backtracking puro del P28 — ¿cuántas líneas menos?

**34.** En **Datalog** (usando Soufflé), declarar los hechos de prerequisitos del plan de estudios ISC del TecNM. Escribir reglas para calcular: a) el cierre transitivo `prerequisito_transitivo/2`, b) el conjunto de materias que deben aprobarse antes de Residencias Profesionales, c) si existe algún ciclo en el grafo de prerequisitos.

**35.** En **ASP** (Clingo), resolver la asignación de salones para el semestre del TecNM: hechos de materias, salones (con capacidad) y docentes. Restricciones de integridad: ningún docente en dos salones a la misma hora, ningún salón con más alumnos que su capacidad, cada materia con exactamente un salón. Encontrar la asignación que maximiza el uso de los salones disponibles.

---

## Metaprogramación y Aspectos

**36.** Implementar un sistema de decoradores que agreguen comportamiento transversal a funciones: a) `@log` que registra cada llamada con sus argumentos y resultado, b) `@cache` que memoriza resultados, c) `@retry(n)` que reintenta $n$ veces si ocurre una excepción, d) `@timeout(s)` que cancela la ejecución si tarda más de $s$ segundos.

**37.** Implementar un sistema de serialización automática: dada una clase cualquiera, generar automáticamente los métodos `to_json()`, `from_json()`, `to_csv()` y `__repr__()` mediante inspección de los atributos de la clase en tiempo de ejecución.

**38.** Construir un mini-ORM (mapeador objeto-relacional) que permita definir clases Python y automáticamente: crear la tabla SQL correspondiente, generar métodos `save()`, `find_by_id()`, `find_all()` y `delete()`. Probar con las clases `Alumno`, `Materia` e `Inscripcion`.

**39.** Implementar un sistema de validación declarativa: decorar los atributos de una clase con restricciones (`@rango(0,100)`, `@no_vacio`, `@formato_curp`, `@positivo`) y que el sistema valide automáticamente al asignar valores. Cualquier violación lanza una excepción descriptiva.

**40.** Construir un generador de código que, dado un esquema JSON que describe una API REST (rutas, métodos, parámetros, respuestas), genere automáticamente el código boilerplate del servidor en Python/Flask y el cliente en JavaScript.

---

## Problemas adicionales

> *Proyectos integradores que combinan múltiples paradigmas y lenguajes del capítulo.*

**41.** Implementar el patrón de *transductor* en tres lenguajes: Python (con generadores), Elixir (con `Stream`) y Clojure (con `transduce`). El transductor debe procesar 10,000,000 de registros usando memoria constante en los tres casos. Comparar: cantidad de código, legibilidad y velocidad de ejecución. ¿En cuál lenguaje el concepto es más natural y por qué?

**42.** Diseñar un DSL para describir horarios escolares del TecNM e implementarlo en tres formas: a) en Python con metaprogramación (`__init_subclass__`, descriptores), b) en Elixir con macros (`defmacro`), c) en Clojure con `defmacro`. El DSL debe detectar y reportar conflictos de horario. Comparar la expresividad y los límites de la metaprogramación en cada paradigma.

**43.** Construir un sistema de verificación de tipos para el lenguaje del P8 (evaluador de expresiones) en OCaml con el verificador del P18, y demostrar que el mismo sistema de tipos expresado como consultas Datalog (P34) puede detectar los mismos errores de tipo de forma declarativa. ¿Cuándo conviene un verificador imperativo y cuándo uno declarativo?

**44.** Construir un sistema distribuido de procesamiento de pagos que integre tres paradigmas: a) **Erlang/OTP** como núcleo de mensajería tolerante a fallos (supervisores, reintentos), b) **Clojure STM** para el estado compartido de saldos sin deadlocks, c) **OCaml** como verificador de tipos de los mensajes en tiempo de compilación. Documentar qué problema específico resuelve cada paradigma y por qué ninguno de los tres por sí solo sería suficiente.
