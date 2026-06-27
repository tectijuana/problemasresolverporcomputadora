# Capítulo 14: Programación Orientada a Objetos y Patrones de Diseño

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

La Programación Orientada a Objetos (POO) no es solo una forma de organizar código — es un modelo mental para mapear el mundo real en estructuras de software. Los patrones de diseño GoF (*Gang of Four*) son soluciones probadas a problemas recurrentes que los ingenieros de software han enfrentado durante décadas. Dominar POO y los 23 patrones GoF es la diferencia entre código que funciona y código que puede mantenerse, extenderse y reutilizarse. Este capítulo usa contextos reales del ecosistema mexicano: instituciones educativas, sistemas de salud, comercio electrónico y administración pública.

## Clases, Objetos y Encapsulamiento

**1.** Diseñar la clase `AlumnoTecNM` con atributos privados: CURP, matrícula, nombre, carrera y lista de calificaciones por materia. Implementar métodos para: calcular promedio general, determinar si está en riesgo escolar (promedio < 7.0 o más de 2 materias reprobadas), generar su kardex formateado y validar que el CURP tenga el formato oficial de la SEP.

**2.** Diseñar la clase `CuentaBancaria` con número de cuenta, CLABE interbancaria, titular y saldo. Implementar operaciones de depósito, retiro (con verificación de fondos), transferencia y generación de estado de cuenta mensual. El saldo nunca debe ser negativo y la CLABE debe tener exactamente 18 dígitos.

**3.** Diseñar el sistema de nómina de una empresa: clase `Empleado` con RFC, NSS, sueldo bruto y tipo de contrato. Implementar el cálculo automático de: cuota IMSS trabajador (1.65%), INFONAVIT (5%), ISR según tabla vigente 2026, y sueldo neto. Incluir método para generar el recibo de nómina en formato de texto.

**4.** Implementar la clase `ExpedienteMedico` para un hospital público: paciente (nombre, CURP, tipo de sangre), diagnósticos con fecha, medicamentos prescritos con dosis y alergias conocidas. Asegurar que ningún medicamento prescrito pertenezca a la lista de alergias del paciente — lanzar excepción descriptiva si hay conflicto.

**5.** Diseñar la clase `VehiculoSAT` con placas, número de serie (VIN), propietario (RFC), año-modelo, tenencia anual calculada según el valor del vehículo y las tarifas del estado de Baja California. Implementar el método `calcular_multas(dias_retraso)` para pagos vencidos de tenencia.

## Herencia, Polimorfismo e Interfaces

**6.** Diseñar una jerarquía de clases para el sistema educativo mexicano: clase base `InstitucionEducativa` con nombre, clave de centro de trabajo (CCT) y municipio. Subclases: `Primaria`, `Secundaria`, `Preparatoria`, `TecNM`, `Universidad`. Cada subclase implementa `calcular_costo_semestre()` y `verificar_requisitos_ingreso(alumno)` con reglas distintas.

**7.** Diseñar una jerarquía de `Vehiculo`: subclases `Automovil`, `Motocicleta`, `Camion` y `Bicicleta`. Cada uno implementa `calcular_costo_verificacion()`, `requiere_tenencia()` y `emite_contaminantes()` de forma distinta según la ley de tránsito del Estado de México. Demostrar polimorfismo procesando una lista heterogénea de vehículos.

**8.** Diseñar el sistema de pagos de una plataforma de comercio electrónico mexicana. Clase base abstracta `MetodoPago` con método `procesar_pago(monto)`. Subclases concretas: `TarjetaCredito`, `SPEI`, `PayPal`, `OXXOPay`, `MercadoPago`. Cada una tiene su propia lógica de comisiones, tiempos de acreditación y manejo de errores.

**9.** Implementar el patrón de interfaces con duck typing: definir las interfaces `Serializable` (métodos `to_json`, `from_json`), `Comparable` (método `compare_to`) y `Printable` (método `pretty_print`). Implementarlas en las clases `Alumno`, `Materia` y `Calificacion`. Demostrar que una función genérica puede operar sobre cualquier objeto que implemente `Comparable` sin saber su tipo concreto.

## Patrones Creacionales

**10.** Implementar el patrón **Singleton** para un logger centralizado del sistema: solo puede existir una instancia que escriba a un archivo de log con timestamp, nivel de severidad y mensaje. Demostrar que dos módulos distintos obtienen la misma instancia aunque la soliciten por separado. Implementar también una versión thread-safe.

**11.** Implementar el patrón **Factory Method** para un sistema de generación de reportes del TecNM: la clase `ReporteFactory` decide qué tipo concreto de reporte crear (`ReportePDF`, `ReporteExcel`, `ReporteHTML`) según el parámetro recibido. Agregar un nuevo tipo de reporte no debe requerir modificar la factory existente.

**12.** Implementar el patrón **Builder** para construir objetos `Curriculum` complejos paso a paso: datos personales, experiencia laboral (lista), educación (lista), habilidades técnicas, idiomas y referencias. El Builder valida que los campos obligatorios estén presentes antes de construir el objeto final.

**13.** Implementar el patrón **Abstract Factory** para una aplicación que debe funcionar tanto en modo claro como oscuro, y tanto en español como en inglés: la factory abstracta crea botones, cuadros de texto y mensajes de error adaptados al tema y al idioma seleccionado.

## Patrones Estructurales

**14.** Implementar el patrón **Adapter** para integrar tres APIs de clima distintas (OpenWeather, AccuWeather, SMN — Servicio Meteorológico Nacional) que tienen respuestas en formatos diferentes. El adaptador debe presentar una interfaz uniforme `obtener_clima(ciudad)` que devuelva siempre la misma estructura, independientemente de qué API se use.

**15.** Implementar el patrón **Decorator** para un sistema de café: clase base `Cafe` con método `costo()` y `descripcion()`. Decoradores: `Leche`, `Azucar`, `VainillaMexicana`, `Cinnamon`, `ExtraShot`. Los decoradores se pueden combinar en cualquier orden y el costo final se calcula acumulativamente.

**16.** Implementar el patrón **Facade** para simplificar el proceso de registro de un nuevo alumno en el TecNM: internamente coordina verificación de documentos, validación de CURP con RENAPO, asignación de matrícula, creación de cuenta de correo institucional y envío de bienvenida. El usuario de la fachada solo llama `registrar_alumno(datos)`.

**17.** Implementar el patrón **Composite** para representar el organigrama de una dependencia del gobierno federal: cada nodo puede ser una persona (hoja) o un departamento (rama que contiene más nodos). Implementar operaciones que funcionen recursivamente: calcular la nómina total de un departamento y contar el total de empleados a cualquier nivel.

## Patrones de Comportamiento

**18.** Implementar el patrón **Observer** para un sistema de alertas sísmicas: el `CENAPED` (observado) notifica a múltiples suscriptores (aplicaciones móviles, bocinas, semáforos inteligentes) cuando detecta un sismo mayor a 5.0 grados. Cada suscriptor reacciona de forma diferente a la misma notificación.

**19.** Implementar el patrón **Strategy** para el cálculo de rutas en una aplicación de transporte público de CDMX: el contexto acepta diferentes estrategias de ruta (`RutaMasCorta`, `RutaMasRapida`, `RutaMasBarata`, `RutaMenosTransbordos`) y puede cambiar de estrategia en tiempo de ejecución.

**20.** Implementar el patrón **Command** para un editor de texto con historial ilimitado de deshacer/rehacer. Cada operación (insertar texto, eliminar, cambiar formato, mover párrafo) se encapsula como un objeto Command con métodos `execute()` y `undo()`. El historial persiste en disco para recuperarse tras un cierre inesperado.

**21.** Implementar el patrón **Iterator** para una clase `PadronElectoral` que puede contener millones de registros en disco. El iterador debe permitir recorrer los registros uno a uno sin cargarlos todos en memoria, y soportar filtros lazy: `filtrar_por_estado`, `filtrar_por_seccion` y `filtrar_por_rango_edad`.

**22.** Implementar el patrón **Chain of Responsibility** para el sistema de aprobación de gastos de una empresa: montos menores a \$5,000 los aprueba el supervisor, hasta \$50,000 el gerente, hasta \$500,000 el director, mayores requieren el consejo de administración. Si un nivel no puede aprobar, pasa automáticamente al siguiente.

---

## Problemas adicionales

> *Proyectos integradores que combinan múltiples patrones.*

**23.** Diseñar e implementar un sistema completo de biblioteca digital del TecNM usando al menos 5 patrones GoF. El sistema debe manejar libros físicos y digitales, préstamos, reservas, multas por retraso y notificaciones por correo. Documentar qué patrón resuelve qué problema específico.

**24.** Implementar el patrón **State** para modelar el ciclo de vida de una orden de compra en una plataforma de comercio electrónico mexicana: `Pendiente → Confirmada → Pagada → Empacada → Enviada → Entregada` (o `Cancelada` desde cualquier estado válido). Cada estado tiene transiciones válidas e inválidas y acciones al entrar/salir.

**25.** Diseñar un sistema de validación de documentos de identidad mexicanos usando el patrón **Template Method**: el algoritmo general es `cargar → extraer_campos → validar_formato → verificar_checksum → resultado`. Cada tipo de documento (CURP, RFC, INE, pasaporte) implementa los pasos concretos de extracción y validación.
