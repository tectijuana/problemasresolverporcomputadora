# Capítulo 20: Agentes Autónomos y Sistemas Multi-Agente

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

Un agente autónomo es un programa que percibe su entorno, razona sobre él y toma acciones para alcanzar un objetivo — en bucle, sin intervención humana en cada paso. Los sistemas multi-agente son redes de agentes que colaboran, compiten o se especializan para resolver problemas que ningún agente individual podría. En 2026, los agentes son la frontera más activa de la IA aplicada: desde asistentes de programación hasta sistemas de investigación científica autónoma. Este capítulo es de los primeros en el mundo en presentar estos conceptos como problemas algorítmicos concretos con criterios de evaluación claros.

## Fundamentos de Agentes

**1.** Implementar el ciclo ReAct (Reason → Act → Observe) para un agente que resuelve problemas de matemáticas: el agente razona sobre qué herramienta usar (calculadora, buscador, intérprete Python), ejecuta la acción, observa el resultado y decide si continuar o terminar. Probar con 20 problemas de álgebra de este libro. Medir la tasa de respuestas correctas vs. un LLM sin herramientas.

**2.** Construir un agente de búsqueda con memoria: el agente debe responder preguntas sobre la situación económica actual de México. Tiene acceso a tres herramientas: `buscar_web(query)`, `leer_url(url)` y `calcular(expresion)`. La memoria de corto plazo (contexto de la conversación) y la de largo plazo (base de datos vectorial de artículos ya consultados) deben evitar buscar la misma información dos veces.

**3.** Implementar un agente de debugging de código: dado un programa Python con errores, el agente debe: a) leer el código, b) identificar el error, c) proponer una corrección, d) ejecutar el código corregido, e) verificar que pasa las pruebas, f) si falla, reintentar con otro enfoque. El agente se detiene cuando el código pasa todas las pruebas o tras 5 intentos.

**4.** Construir un agente con planificación jerárquica: dado el objetivo de alto nivel *"preparar el informe mensual de ventas de la empresa"*, el agente debe descomponer el objetivo en subtareas (obtener datos, limpiarlos, calcular métricas, generar gráficas, redactar conclusiones, formatear PDF), ejecutarlas en orden respetando dependencias, y manejar fallos en pasos intermedios.

**5.** Implementar evaluación de agentes: dado un benchmark de 50 tareas con resultado esperado conocido (preguntas factuales, cálculos, búsquedas, generación de código), medir para cada agente: tasa de éxito, número promedio de pasos por tarea, costo en tokens, y latencia. Comparar un agente simple (ReAct) vs. un agente con planificación vs. un agente con memoria.

## Herramientas y Memoria

**6.** Construir el toolkit de herramientas para un agente fiscal del SAT: `consultar_rfc(rfc)` que verifica si el RFC existe y está activo, `calcular_isr(ingresos, deducciones)` que aplica la tabla ISR vigente, `generar_cfdi(datos)` que valida el formato del XML, y `consultar_obligaciones(rfc)` que lista las declaraciones pendientes. El agente usa estas herramientas para responder consultas de contribuyentes.

**7.** Implementar memoria episódica para un agente de soporte técnico: el agente almacena cada conversación resuelta (problema, diagnóstico, solución) en una base de datos vectorial. Cuando llega un nuevo problema, primero busca en la memoria si ya resolvió algo similar y reutiliza la solución exitosa en lugar de razonar desde cero. Medir la reducción en tokens y latencia gracias a la memoria.

**8.** Construir un agente con memoria de trabajo estructurada: el agente mantiene un *scratchpad* explícito (lista de hechos conocidos, lista de preguntas pendientes, plan actual) que actualiza en cada paso. Demostrar que esta memoria estructurada mejora la coherencia en tareas que requieren más de 10 pasos, comparado con un agente que solo usa el contexto del LLM.

## Sistemas Multi-Agente

**9.** Diseñar e implementar un sistema de revisión de código con múltiples agentes especializados: el agente Orquestador divide el código recibido entre tres agentes paralelos (Revisor de Seguridad, Revisor de Rendimiento, Revisor de Estilo), recopila sus reportes y genera un informe integrado. Probar con 10 proyectos Python de GitHub de estudiantes del TecNM.

**10.** Implementar un sistema de investigación científica multi-agente: dado el objetivo *"resume el estado del arte en detección de enfermedades con ML en México"*, el Orquestador asigna a 4 agentes Investigadores la búsqueda paralela de artículos (Google Scholar, PubMed, arXiv, repositorios de CONACYT), un agente Síntesis consolida los resultados evitando duplicados y un agente Editor redacta el informe final.

**11.** Construir un sistema de debate entre agentes para tomar decisiones: dado un proyecto de infraestructura educativa (construir un laboratorio de cómputo en un plantel del TecNM), tres agentes representan posiciones distintas (Infraestructura propone solución on-premise, Nube propone SaaS, Economía evalúa costos) y debaten por 3 rondas. Un agente Árbitro sintetiza la decisión final con justificación.

**12.** Implementar un sistema de agentes con roles de mercado: simular un mercado de carbono donde agentes Empresa (reducen emisiones o compran créditos según su costo marginal) y agentes Regulador (ajustan el precio del carbono para alcanzar la meta de reducción) interactúan en cada periodo. Medir si el sistema converge al precio de equilibrio óptimo.

## Flujos de Trabajo y Orquestación

**13.** Implementar el patrón de orquestación con flujo condicional: un agente Clasificador determina si una consulta ciudadana al gobierno de Tijuana es sobre agua, transporte, seguridad o trámites, y la enruta al agente especializado correspondiente. Si el agente especializado no puede responder, escala al agente de Soporte General. Registrar cada enrutamiento para análisis de eficiencia.

**14.** Construir un pipeline de agentes en cadena para procesamiento de documentos del SAT: Agente 1 extrae texto del PDF, Agente 2 identifica el tipo de documento (declaración, acuse, resolución), Agente 3 extrae las cifras clave, Agente 4 valida la consistencia interna, y Agente 5 genera el resumen. Si cualquier agente falla, el sistema reinicia desde el último punto exitoso.

**15.** Implementar agentes con control de versiones de estado: cada acción del agente genera un snapshot del estado. Si el agente llega a un estado indeseable, puede "retroceder" a cualquier snapshot anterior y tomar un camino alternativo. Demostrar el sistema con un agente que escribe código: si el código genera errores de runtime, retrocede al snapshot antes de ese bloque y lo reescribe.

---

## Problemas adicionales

**16.** Construir un agente de tutoría adaptativa para el TecNM: el agente evalúa el conocimiento actual del alumno con preguntas de diagnóstico, genera un plan de estudio personalizado, explica los conceptos en el orden óptimo (dependencias primero), propone ejercicios adaptados al nivel y ajusta la dificultad según el desempeño en tiempo real.

**17.** Implementar un agente de monitoreo de infraestructura: dado acceso a las métricas del sistema (CPU, memoria, latencia, errores), el agente detecta anomalías, diagnostica la causa raíz consultando logs y métricas históricas, ejecuta acciones correctivas automáticas (reiniciar servicio, limpiar caché, escalar recursos) y escala al ingeniero de guardia si no puede resolver el problema.

**18.** Diseñar e implementar un agente de escritura de código con TDD: el agente recibe una especificación en lenguaje natural, primero escribe las pruebas unitarias que la especificación implica, luego escribe el código que las hace pasar (ciclo rojo-verde-refactorizar), y no termina hasta que todas las pruebas están en verde y la cobertura supera el 90%.

**19.** Construir un sistema de agentes para análisis competitivo de mercado: dado el nombre de una empresa mexicana (por ejemplo, una maquila de Tijuana), los agentes recopilan información de múltiples fuentes (DOF, registros del SAT, LinkedIn, noticias), sintetizan un perfil competitivo con fortalezas, debilidades y oportunidades, y lo presentan en formato de informe ejecutivo.

**20.** Implementar un agente con capacidades de auto-mejora controlada: el agente puede modificar sus propios prompts de sistema basándose en los casos donde falló. Cada semana, analiza los últimos 100 casos fallidos, identifica patrones de error, propone modificaciones a su prompt, las evalúa en un conjunto de validación, y aplica solo las que mejoran el desempeño. Implementar salvaguardas para que las auto-modificaciones no degraden el comportamiento base.
