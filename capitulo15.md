# Capítulo 15: Bases de Datos y Persistencia

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

Toda aplicación que vale la pena guarda datos. Saber diseñar esquemas, escribir consultas eficientes y elegir el motor de persistencia correcto es una habilidad que distingue a los desarrolladores junior de los senior. Este capítulo cubre SQL desde los fundamentos hasta las consultas avanzadas, las bases de datos NoSQL para casos donde SQL no es la mejor opción, el diseño de esquemas relacionales bien normalizados y las bases de datos vectoriales que potencian las aplicaciones de IA modernas. Los ejemplos usan contextos reales mexicanos: padrón de contribuyentes, sistemas escolares, salud pública y comercio electrónico.

## SQL Básico

**1.** Crear la base de datos `escuela_tecnm` con las tablas: `alumno` (matrícula, nombre, CURP, carrera, semestre, promedio), `materia` (clave, nombre, créditos, horas_semana), `inscripcion` (alumno_id, materia_id, semestre, calificacion). Insertar datos de prueba: 200 alumnos, 30 materias y 1,500 inscripciones. Escribir consultas para: a) top 10 alumnos por promedio por carrera, b) materias con más reprobados, c) alumnos con carga completa (5 materias o más).

**2.** Diseñar la base de datos `inventario_farmacia` con productos (clave, nombre, principio_activo, presentación, precio, stock), proveedores (RFC, razón_social, contacto) y pedidos. Escribir consultas para: productos con stock menor al mínimo, costo total del inventario por categoría, proveedor con mayor volumen de ventas en el último trimestre.

**3.** Crear la tabla `transacciones_spei` con: CLABE origen, CLABE destino, monto, fecha_hora, concepto y estatus. Con 1,000,000 de registros simulados, escribir consultas para: total transferido por día de la semana, hora pico de mayor actividad, usuarios con más de 50 transacciones en un día (posible fraude).

**4.** Modelar el sistema de citas médicas del IMSS: pacientes (NSS, nombre, fecha_nacimiento, tipo_sangre), médicos (empleado_id, especialidad, CEDULA_profesional), consultorios (número, hospital, piso) y citas (paciente_id, médico_id, consultorio_id, fecha_hora, diagnóstico). Escribir consultas para encontrar médicos sin citas disponibles en los próximos 7 días y pacientes que no han asistido a consulta en más de un año.

## SQL Intermedio

**5.** Escribir consultas con `JOIN` múltiples para el sistema `escuela_tecnm`: a) nombre del alumno, materia y calificación de todos los reprobados en el semestre actual, b) profesores que imparten más de 3 materias simultáneamente, c) salones con más del 90% de ocupación. Usar `INNER JOIN`, `LEFT JOIN` y `FULL OUTER JOIN` según corresponda.

**6.** Implementar consultas con funciones de ventana (`WINDOW FUNCTIONS`): a) ranking de alumnos por promedio dentro de cada carrera usando `RANK()`, b) promedio móvil de calificaciones de cada alumno a lo largo de los semestres usando `AVG() OVER`, c) diferencia de calificación de cada alumno respecto al semestre anterior usando `LAG()`.

**7.** Optimizar el rendimiento de consultas: crear índices apropiados para la base de datos `inventario_farmacia`, analizar el plan de ejecución (`EXPLAIN ANALYZE`) antes y después de indexar, y documentar la mejora en tiempo de respuesta para consultas sobre 1,000,000 de registros.

**8.** Implementar transacciones ACID para el sistema bancario: transferencia SPEI que debe actualizar dos cuentas atómicamente. Si la cuenta origen no tiene fondos suficientes o la CLABE destino no existe, revertir toda la operación. Implementar manejo de deadlocks con reintentos automáticos.

**9.** Crear vistas materializadas y procedimientos almacenados para el sistema escolar: vista `reporte_semestral` que consolida calificaciones y promedios, procedimiento `calcular_becas()` que identifica candidatos a beca académica según reglamento, y trigger `actualizar_promedio` que recalcula el promedio del alumno cada vez que se inserta una calificación.

## SQL Avanzado

**10.** Implementar consultas recursivas con `WITH RECURSIVE` para: a) encontrar todos los subordinados directos e indirectos de un director en el organigrama de la SEP, b) calcular el costo total de una lista de materiales (BOM) con múltiples niveles de componentes para manufactura maquiladora.

**11.** Diseñar e implementar particionado de tablas para `transacciones_spei`: particionar por mes del año. Verificar que las consultas de un rango de fechas usen partition pruning y no escaneen particiones innecesarias. Medir la mejora en tiempo de respuesta.

**12.** Implementar búsqueda de texto completo (*full-text search*) sobre una base de datos de 500,000 artículos del Diario Oficial de la Federación (DOF). Comparar la velocidad de `LIKE '%palabra%'` vs. índices de texto completo para búsquedas de términos jurídicos específicos.

## Bases de Datos NoSQL

**13.** Modelar el catálogo de productos de una tienda en línea usando MongoDB (o equivalente documental). Cada producto tiene atributos variables según su categoría (electrónica, ropa, alimentos). Implementar consultas de: búsqueda por atributos específicos de categoría, productos con precio entre rangos, y actualización masiva de precios con factor de incremento.

**14.** Implementar un sistema de sesiones de usuario usando Redis: almacenar token JWT, datos de sesión y preferencias del usuario con TTL de 24 horas. Implementar lista de tokens revocados (blacklist) para logout seguro. Medir la latencia de lectura/escritura vs. una base de datos SQL equivalente.

**15.** Diseñar un sistema de métricas de aplicación usando una base de datos de series de tiempo (InfluxDB o TimescaleDB): registrar CPU, memoria, latencia de API y errores cada 10 segundos. Implementar consultas para: percentil 99 de latencia por endpoint en la última hora, detección de anomalías por desviación estándar, y downsampling automático de datos de más de 30 días.

**16.** Implementar un grafo de relaciones sociales usando Neo4j o equivalente: usuarios, seguidores, publicaciones y likes. Consultas que son costosas en SQL pero naturales en grafos: amigos en común, grado de separación entre dos usuarios, usuarios influenciadores (mayor PageRank) dentro de una comunidad.

## Diseño de Esquemas y Modelado

**17.** Tomar el esquema de la base de datos `clinica_imss` (pacientes, médicos, consultas, medicamentos, hospitales) y normalizarlo hasta la Tercera Forma Normal (3FN). Documentar cada paso: identificar dependencias funcionales, eliminar redundancias y justificar por qué cada tabla quedó en 3FN.

**18.** Diseñar el esquema de un sistema de e-commerce mexicano completo con: usuarios, productos, categorías, inventario por almacén, órdenes, ítems de orden, pagos (múltiples métodos), envíos (con tracking), devoluciones y reseñas. El esquema debe soportar múltiples monedas, múltiples tiendas y facturación electrónica CFDI.

**19.** Diseñar e implementar una estrategia de migración de datos: el sistema de nómina de una empresa tiene 20 años de datos en un esquema Legacy (tabla plana de 80 columnas). Migrar a un esquema normalizado moderno sin pérdida de información, manteniendo el sistema Legacy activo durante la migración (migración en caliente).

---

## Problemas adicionales

**20.** Implementar una base de datos vectorial (pgvector o Chroma) para búsqueda semántica sobre el catálogo de cursos del TecNM: convertir las descripciones de cada curso a embeddings, y dado el texto de perfil de un estudiante, encontrar los 5 cursos más relevantes por similitud semántica. Comparar con búsqueda por palabras clave.

**21.** Diseñar una arquitectura CQRS (Command Query Responsibility Segregation) para el sistema de reservaciones del aeropuerto de Tijuana: lado escritura con base de datos transaccional normalizada, lado lectura con base de datos desnormalizada optimizada para consultas. Implementar la sincronización entre ambos lados mediante eventos.

**22.** Implementar *database sharding* horizontal para la base de datos de clientes de una fintech mexicana con 10,000,000 de usuarios: distribuir por hash del RFC entre 4 shards. Implementar consultas que afectan múltiples shards y manejo de transacciones distribuidas con protocolo de dos fases (2PC).
