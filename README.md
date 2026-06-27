# Problemas para Resolver con Computadora

**Donald D. Spencer** — Editorial Limusa, 1985  
Versión en español de *Problems for Computer Solution* (Hayden Book Company)  
Traducción: Guillermo García Talavera  
Extensión moderna 2026: TecNM Tijuana

---

Preocupado por retos incrementales a los estudiantes o hobbies del área que involucre algoritmos y computación, esta dedicado para Uds. una generación resiliente con habilidades técnicas y de proyección.

Este repositorio contiene una transcripción digital del libro clásico de 1985, convertida de PDF a Markdown para facilitar su consulta, búsqueda y actualización. Los problemas originales estaban pensados para lenguajes como BASIC, FORTRAN, APL o PL/1 — aquí quedan disponibles para resolverse con Python, C, JavaScript o cualquier lenguaje moderno. El contenido ha sido modernizado para jóvenes programadores mexicanos en 2026.

Los capítulos 12 al 22 son una **extensión de elaboración propia**: reemplazan el material más envejecido del libro original con capítulos completamente nuevos sobre las disciplinas más relevantes de la programación moderna, incluyendo LLMs, agentes autónomos, sistemas embebidos con IA y seguridad responsable — temas que no tienen equivalente en ningún otro libro de problemas en español.

## Contenido

### Capítulos originales (Spencer 1985 — modernizados)

| Capítulo | Tema | Problemas |
|----------|------|-----------|
| [01](capitulo01.md) | Problemas Introductorios | 90 |
| [02](capitulo02.md) | Álgebra | 130 |
| [03](capitulo03.md) | Geometría | 111 |
| [04](capitulo04.md) | Trigonometría | 43 |
| [05](capitulo05.md) | Probabilidad y Estadística | 97 |
| [06](capitulo06.md) | Matemáticas Intermedias | 120 |
| [07](capitulo07.md) | Teoría de los Números | 92 |
| [08](capitulo08.md) | Ciencias: Química, Física y Biología | 43 |
| [09](capitulo09.md) | Administración | 65 |
| [10](capitulo10.md) | Diversión con la Computadora | 51 |
| [11](capitulo11.md) | Miscelánea de Problemas | 46 |
| | **Subtotal** | **888** |

### Capítulos de extensión moderna (TecNM 2026)

| Capítulo | Tema | Problemas |
|----------|------|-----------|
| [12](capitulo12.md) | Estructuras de Datos y Algoritmos Avanzados | 32 |
| [13](capitulo13.md) | Paradigmas de Programación | 22 |
| [14](capitulo14.md) | Programación Orientada a Objetos y Patrones de Diseño | 25 |
| [15](capitulo15.md) | Bases de Datos y Persistencia | 22 |
| [16](capitulo16.md) | Desarrollo Web y APIs | 22 |
| [17](capitulo17.md) | Sistemas Concurrentes y Distribuidos | 18 |
| [18](capitulo18.md) | Inteligencia Artificial Clásica | 20 |
| [19](capitulo19.md) | Ingeniería de LLMs y Prompts | 20 |
| [20](capitulo20.md) | Agentes Autónomos y Sistemas Multi-Agente | 20 |
| [21](capitulo21.md) | Sistemas Embebidos e IoT con IA | 20 |
| [22](capitulo22.md) | Seguridad, Ética e IA Responsable | 22 |
| | **Subtotal** | **243** |

| | **TOTAL** | **1,131** |

## Estado del proyecto

### Transcripción y modernización (caps. 1–11)

- [x] Extracción del PDF (OCR)
- [x] División por capítulos
- [x] Corrección completa de errores OCR en todos los capítulos
- [x] Conversión de fórmulas a LaTeX estilo *GitHub math inline-block* (`$formula$`)
- [x] Conversión de unidades imperiales a sistema métrico (SI)
- [x] Eliminación de encabezados y pies de página del OCR
- [x] Modernización de precios a valores MXN 2026 (referencia: salario mínimo Zona Libre Frontera Norte)
- [x] Actualización de fechas y referencias culturales al contexto mexicano actual
- [x] Eliminación de problemas redundantes dentro y entre capítulos
- [x] Sustitución de contexto anglosajón por referentes mexicanos (IMSS, CETES, IMECA, ISAI, etc.)

### Extensión moderna (caps. 12–22)

- [x] Cap. 12: Estructuras de Datos y Algoritmos Avanzados (Metro CDMX, RFC, CURP, 32 estados)
- [x] Cap. 13: Paradigmas de Programación (funcional, lógico, declarativo, metaprogramación)
- [x] Cap. 14: POO y Patrones de Diseño (GoF completo con contexto TecNM/SAT/IMSS)
- [x] Cap. 15: Bases de Datos y Persistencia (SQL avanzado, NoSQL, vectorial, privacidad)
- [x] Cap. 16: Desarrollo Web y APIs (REST, GraphQL, auth, PWA, microservicios)
- [x] Cap. 17: Sistemas Concurrentes y Distribuidos (Raft, SAGA, streaming IoT)
- [x] Cap. 18: Inteligencia Artificial Clásica (ML desde cero, datos INEGI/IMSS)
- [x] Cap. 19: Ingeniería de LLMs y Prompts *(único en español a este nivel)*
- [x] Cap. 20: Agentes Autónomos y Multi-Agente *(único en español a este nivel)*
- [x] Cap. 21: Sistemas Embebidos e IoT con IA (TinyML, LoRa, maquilas de Tijuana)
- [x] Cap. 22: Seguridad, Ética e IA Responsable (LFPDPPP, CNBV, fairness, privacidad diferencial)
- [ ] Agregar soluciones de referencia en Python/C

## Convención de LaTeX

Todos los archivos usan el estilo **GitHub math inline-block**: fórmulas con `$formula$` en línea. No se usa ningún entorno `\begin{}`. Este formato renderiza correctamente en GitHub.

## Cómo contribuir

1. Revisar un capítulo y corregir errores residuales
2. Modernizar el enunciado de un problema
3. Agregar una solución de referencia en cualquier lenguaje moderno
4. Proponer un nuevo problema para los capítulos de extensión (abrir un issue)

## Licencia

Capítulos 1–11: Transcripción con fines educativos. Los derechos del contenido original pertenecen a Editorial Limusa / Hayden Book Company.  
Capítulos 12–22: Elaboración propia, licencia CC BY-NC-SA 4.0. Atribución: TecNM Campus Tijuana, 2026.
