# Capítulo 19: Ingeniería de LLMs y Prompts

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

Los Modelos de Lenguaje de Gran Escala (LLMs) son la tecnología más transformadora de la primera mitad del siglo XXI. Pero usarlos bien — obtener respuestas precisas, confiables, reproducibles — es una disciplina de ingeniería, no magia. La ingeniería de prompts, la evaluación de modelos, el ajuste fino (*fine-tuning*), la generación aumentada por recuperación (RAG) y la detección de alucinaciones son habilidades que ningún programador de 2026 puede ignorar. Este capítulo es posiblemente el primero en el mundo en presentar estos temas como problemas algorítmicos con criterios de evaluación objetivos, en español, para estudiantes latinoamericanos.

## Fundamentos de Prompts

**1.** Diseñar tres versiones de un prompt para que un LLM resuelva el siguiente problema: *"Un tren sale de CDMX a Guadalajara a 120 km/h. Otro sale de Guadalajara a CDMX a 90 km/h. La distancia es 500 km. ¿A qué distancia de CDMX se cruzan?"* La versión A es el prompt directo, la versión B agrega `"Piensa paso a paso"`, y la versión C usa *few-shot* con un ejemplo similar resuelto. Medir la tasa de respuestas correctas con cada versión ejecutando cada prompt 10 veces. ¿Cuánto mejora el *chain-of-thought*?

**2.** Implementar un sistema de evaluación automática de prompts: dado un conjunto de 50 preguntas con respuesta correcta conocida sobre derecho fiscal mexicano (ISR, IVA, CFDI), probar 5 variaciones del prompt del sistema y medir la tasa de precisión de cada variante. La evaluación debe ser reproducible y documentar el prompt exacto, el modelo, la temperatura y la versión.

**3.** Diseñar y comparar cuatro estrategias de prompting para que un LLM genere código Python correcto: a) prompt directo, b) chain-of-thought, c) *tree-of-thoughts* (pedir al modelo que explore 3 enfoques y elija el mejor), d) self-consistency (generar 5 respuestas y votar por la más frecuente). Probar con 20 problemas de este mismo libro y medir el porcentaje de código que pasa las pruebas unitarias.

**4.** Implementar un sistema de prompts con roles múltiples: para analizar la viabilidad de un proyecto de software, crear prompts que simulen una junta con tres perspectivas — el arquitecto técnico (valida factibilidad), el gerente de producto (valida valor de negocio) y el abogado (valida riesgos legales y de propiedad intelectual). Estructurar el sistema para que cada "personaje" critique las posiciones de los otros.

## RAG — Generación Aumentada por Recuperación

**5.** Construir un sistema RAG básico sobre la Ley Federal del Trabajo (LFT) de México: indexar el texto completo de la LFT en una base de datos vectorial, y dado cualquier artículo de la LFT como consulta, encontrar los 5 artículos más relacionados por similitud semántica. Comparar la precisión de búsqueda semántica vs. búsqueda por palabras clave para consultas como *"vacaciones de trabajadores eventuales"*.

**6.** Construir un chatbot de soporte académico para el TecNM usando RAG: indexar el reglamento de titulación, el plan de estudios de Ingeniería en Sistemas Computacionales y las circulares del semestre. El chatbot debe responder preguntas como *"¿Cuántos créditos necesito para realizar residencias profesionales?"* citando el documento y el número de artículo específico.

**7.** Implementar RAG con re-ranking: después de recuperar los 20 fragmentos más similares a la consulta, usar un modelo de cross-encoding para re-ordenarlos y devolver los 5 más relevantes. Comparar la calidad de respuestas del LLM con los top-5 por similitud coseno vs. los top-5 por re-ranking en 30 consultas de prueba.

**8.** Construir un sistema RAG multi-documento con grafos de conocimiento: dado un corpus de 1,000 artículos del DOF sobre regulaciones ambientales, construir un grafo donde los nodos son entidades (leyes, dependencias, fechas) y las aristas son relaciones (modifica, deroga, hace referencia a). Las consultas pueden cruzar múltiples documentos siguiendo las relaciones del grafo.

## Evaluación y Confiabilidad

**9.** Implementar un sistema de detección de alucinaciones para respuestas de un LLM sobre datos del INEGI: dado que el modelo responde preguntas sobre estadísticas económicas de México, verificar automáticamente cada cifra numérica mencionada contra una base de datos oficial. Clasificar cada respuesta como: verificada, no verificable o incorrecta.

**10.** Diseñar un framework de evaluación LLM-as-a-judge: usar un LLM evaluador (con prompt de sistema cuidadosamente diseñado) para calificar las respuestas de otro LLM generador en una escala de 1-5 por criterios de: relevancia, exactitud factual, claridad y completitud. Medir la correlación entre el juicio automático y el juicio humano en 100 respuestas evaluadas por ambos.

**11.** Implementar pruebas de consistencia para un LLM: hacer la misma pregunta con 5 formulaciones distintas pero semánticamente equivalentes y medir si las respuestas son consistentes. Crear un reporte automático que señale las preguntas donde el modelo es inconsistente y cuantifique el nivel de inconsistencia.

**12.** Construir un sistema de monitoreo de deriva de modelo (*model drift*): dado que un LLM se actualiza periódicamente, ejecutar automáticamente el mismo conjunto de 200 preguntas de referencia y comparar si las respuestas cambiaron significativamente. Alertar cuando más del 5% de las respuestas cambian en más de un umbral de similitud definido.

## Ajuste Fino y Personalización

**13.** Preparar un dataset para fine-tuning de un LLM en el dominio de derecho fiscal mexicano: recopilar y estructurar 500 pares (pregunta, respuesta-ideal) sobre ISR, IVA, CFDI y obligaciones de personas morales. Asegurar diversidad de tipos de preguntas, eliminar duplicados semánticos y dividir en 80% entrenamiento / 10% validación / 10% prueba.

**14.** Implementar *prompt tuning* con *soft prompts*: en lugar de modificar los pesos del modelo, optimizar un vector de tokens de prefijo que maximice la precisión del modelo en 100 preguntas sobre regulaciones del IMSS. Comparar el costo computacional y la precisión vs. fine-tuning completo vs. prompts manuales.

**15.** Implementar RLHF simplificado (Aprendizaje por Refuerzo con Retroalimentación Humana): dado un generador de resúmenes de leyes mexicanas, construir un modelo de recompensa entrenado con 200 comparaciones humanas (resumen A es mejor que resumen B), y usar ese modelo de recompensa para mejorar el generador por gradient ascent.

---

## Problemas adicionales

**16.** Construir un sistema de *prompt injection* defense: dado un chatbot de atención ciudadana del gobierno que usa un LLM, implementar capas de defensa contra ataques de inyección de prompts (instrucciones maliciosas en el texto del usuario que intentan evadir las instrucciones del sistema). Probar con 20 ataques conocidos y medir la tasa de éxito de las defensas.

**17.** Diseñar un benchmark de evaluación de LLMs en español mexicano: crear 100 preguntas culturalmente específicas (historia, leyes, geografía, gastronomía, economía de México) con respuestas verificadas, y evaluar 3 LLMs distintos. Publicar los resultados en formato estándar comparable con benchmarks internacionales.

**18.** Implementar un sistema de *Constitutional AI* simplificado: dado un LLM que puede generar respuestas dañinas, construir un pipeline donde un segundo LLM revisa cada respuesta contra una lista de principios (constitución), revisa si algún principio se viola y corrige la respuesta antes de mostrarla al usuario. Medir la reducción en respuestas problemáticas.

**19.** Construir un sistema de síntesis de documentos largos con preservación de estructura: dado el Plan Nacional de Desarrollo 2025-2030 (más de 200 páginas), generar automáticamente: resumen ejecutivo (1 página), tabla de compromisos por dependencia, y mapa de indicadores con sus metas. Verificar que ninguna cifra en el resumen difiera del documento original.

**20.** Implementar un motor de búsqueda semántica sobre el historial de preguntas de examen de CENEVAL/EXANI-II: indexar 5,000 preguntas de examen de admisión universitaria, y dado el perfil de un estudiante (materias cursadas, calificaciones), recomendar los 20 temas donde debe reforzar su preparación con mayor impacto en su probabilidad de aprobar.
