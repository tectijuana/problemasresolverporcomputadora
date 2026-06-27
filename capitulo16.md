# Capítulo 16: Desarrollo Web y APIs

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

El desarrollo web es la disciplina de programación con mayor demanda laboral en México y el mundo. En 2026, construir una aplicación web moderna significa dominar el frontend (HTML, CSS, JavaScript, React/Vue), el backend (APIs REST o GraphQL), la autenticación segura, el despliegue en la nube y las pruebas automatizadas. Este capítulo cubre la ruta completa desde una página estática hasta una aplicación de producción, con problemas concretos contextualizados en el ecosistema digital mexicano.

## Frontend Básico

**1.** Construir una calculadora del SAT: página HTML con formulario para ingresar ingreso anual, deducciones personales y tipo de contribuyente (persona física asalariada, honorarios o actividad empresarial). Calcular el ISR anual según las tablas 2026 del SAT, mostrar el desglose por tasa y actualizar el resultado en tiempo real mientras el usuario escribe (sin recargar la página).

**2.** Implementar una calculadora de nómina quincenal responsiva: dado el sueldo mensual bruto de un trabajador, calcular y mostrar en tarjetas separadas: sueldo bruto, cuota IMSS trabajador, INFONAVIT, ISR, y sueldo neto. Incluir un slider para ajustar el número de dependientes económicos y que los cálculos se actualicen automáticamente.

**3.** Construir un mapa interactivo de las zonas de riesgo sísmico de México usando Leaflet.js: cargar el GeoJSON de municipios de México, colorear por nivel de riesgo sísmico (bajo, medio, alto, muy alto) según datos del CENAPRED, y mostrar información del municipio al hacer clic.

**4.** Implementar un dashboard de estadísticas del TecNM con gráficas interactivas usando Chart.js o D3.js: matrícula por carrera (barras), evolución histórica de egresados (línea), distribución por género (pastel), y mapa de calor de eficiencia terminal por plantel. Los datos deben cargarse desde un archivo JSON y las gráficas deben ser responsivas.

## APIs REST y Backend

**5.** Diseñar e implementar una API REST completa para el sistema de biblioteca del TecNM con los recursos: `libros`, `autores`, `usuarios` y `prestamos`. Implementar CRUD completo para cada recurso, con paginación, filtros, ordenamiento y búsqueda. La API debe seguir las convenciones REST: verbos HTTP correctos, códigos de estado apropiados y respuestas JSON consistentes.

**6.** Implementar versionado de API: la misma biblioteca debe servir `/api/v1/` y `/api/v2/` simultáneamente. La v2 añade campos nuevos a las respuestas y cambia el formato de fechas. Los clientes de v1 deben seguir funcionando sin cambios. Implementar deprecation warnings en los headers de v1.

**7.** Construir una API de consulta del RFC: dada una cadena de texto, validar si tiene el formato correcto de RFC (persona física o moral), extraer sus componentes (nombre, fecha, homoclave) y verificar que la homoclave es consistente con los datos. Documentar la API con OpenAPI/Swagger.

**8.** Implementar un sistema de webhooks: cuando se procesa un pago en el sistema (evento `pago.completado`), notificar automáticamente a URLs externas registradas. Incluir: firma HMAC para verificar autenticidad, reintentos automáticos con backoff exponencial si la URL destino falla, y log de todas las entregas con su estatus.

**9.** Construir una API GraphQL para el sistema escolar del TecNM: queries para obtener alumnos con sus materias y calificaciones en una sola consulta (sin N+1 problem), mutations para registrar calificaciones, y subscriptions en tiempo real para notificar cuando se publica una calificación nueva.

## Autenticación y Seguridad

**10.** Implementar autenticación JWT completa: registro con email y contraseña (hash bcrypt), login que devuelve access token (15 min) y refresh token (7 días), middleware de autorización que valida el token en cada request protegido, y endpoint de logout que invalida el refresh token. Almacenar refresh tokens en Redis con TTL.

**11.** Implementar autenticación OAuth 2.0 con Google como proveedor: el usuario hace clic en "Iniciar sesión con Google", se redirige a Google para autorizar, Google regresa con un código, la aplicación intercambia el código por tokens, y crea o actualiza el perfil del usuario. Manejar correctamente el state anti-CSRF.

**12.** Implementar protecciones de seguridad básicas en una API REST: rate limiting por IP (máximo 100 requests por minuto), protección contra SQL injection con queries parametrizadas, validación y sanitización de todas las entradas, headers de seguridad (CORS, CSP, HSTS, X-Frame-Options), y detección de payloads maliciosos.

## Componentes, Estado y SPA

**13.** Construir una aplicación de lista de tareas (to-do) como SPA con React o Vue: componentes para lista de tareas, formulario de nueva tarea, filtros (todas/pendientes/completadas) y estadísticas. El estado debe persistir en localStorage. Implementar drag-and-drop para reordenar tareas. Sin librerías de UI externas — solo CSS propio.

**14.** Implementar un sistema de formularios con validación reactiva: formulario de registro de alumno al TecNM con campos: nombre, CURP (validar formato en tiempo real), email institucional (dominio `@tectijuana.edu.mx`), carrera (select), semestre, y foto de perfil (validar tamaño < 2MB y formato PNG/JPG). Los errores aparecen al perder el foco, no al enviar.

**15.** Construir un reproductor de noticias del DOF (Diario Oficial de la Federación) con React: consumir la API pública del DOF, listar las publicaciones recientes, implementar búsqueda en tiempo real (debounced 300ms), marcar artículos como favoritos (persistidos en localStorage) y compartir por enlace directo.

## Testing y Despliegue

**16.** Escribir pruebas unitarias para la API de biblioteca del TecNM usando Jest o pytest: probar cada endpoint con casos felices, casos de error (404, 400, 401) y casos límite (IDs inválidos, campos faltantes, payloads demasiado grandes). Alcanzar cobertura de código mayor al 80%.

**17.** Implementar pruebas de integración end-to-end con Playwright o Cypress para el sistema de inscripción en línea del TecNM: simular el flujo completo de un alumno que busca materias, selecciona horarios, verifica conflictos, confirma inscripción y descarga su comprobante.

**18.** Dockerizar la aplicación de biblioteca del TecNM: crear `Dockerfile` para el backend, `docker-compose.yml` que levante el backend, la base de datos PostgreSQL y el servidor Redis. El entorno de producción debe ser idéntico al de desarrollo. Implementar healthchecks y restart policies.

---

## Problemas adicionales

**19.** Implementar Server-Sent Events (SSE) para un tablero de monitoreo en tiempo real del sistema escolar: cuando un docente publica una calificación, todos los alumnos inscritos en esa materia reciben la notificación en su navegador sin recargar la página. Comparar con WebSockets: ¿cuándo conviene cada enfoque?

**20.** Construir una PWA (Progressive Web App) del horario escolar del TecNM: funcionar offline con Service Workers, instalable en el celular, sincronizar datos cuando recupere conexión, y enviar notificaciones push recordando exámenes 24 horas antes. Alcanzar puntuación de 90+ en Lighthouse.

**21.** Implementar una API con caché multinivel: caché en memoria (5 min), caché en Redis (1 hora) y base de datos como última capa. El sistema debe invalidar la caché automáticamente cuando los datos cambien. Medir la reducción en latencia y en carga a la base de datos con 10,000 requests concurrentes.

**22.** Diseñar e implementar un API Gateway para el ecosistema de microservicios del TecNM: enrutar requests a los servicios correctos (alumnos, materias, calificaciones, biblioteca), agregar autenticación centralizada, rate limiting por servicio, logging unificado y circuit breaker para cuando un servicio falla.
