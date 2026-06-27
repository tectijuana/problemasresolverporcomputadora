# Capítulo 17: Sistemas Concurrentes y Distribuidos

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

Los sistemas modernos no son programas secuenciales que corren en un solo núcleo. Son colecciones de procesos que se ejecutan en paralelo, se comunican por red, comparten recursos y deben sobrevivir a fallos parciales. Entender la concurrencia — y sus trampas: condiciones de carrera, deadlocks, hambruna — es lo que distingue a un programador que puede construir sistemas que escalan de uno que solo puede construir scripts. Este capítulo cubre desde hilos básicos hasta arquitecturas distribuidas con tolerancia a fallos.

## Concurrencia y Paralelismo

**1.** Implementar el problema clásico productor-consumidor con una cola compartida de tamaño limitado: múltiples productores generan pedidos de una tienda en línea y múltiples consumidores los procesan. Usar semáforos o monitores para evitar condiciones de carrera. Simular 10 productores, 5 consumidores y 10,000 pedidos. Medir el throughput total.

**2.** Implementar el problema de los filósofos comensales con 5 filósofos: detectar y prevenir el deadlock usando el algoritmo de la jerarquía de recursos (numeración de tenedores). Demostrar que sin la solución ocurre deadlock y con ella no. Medir el tiempo de espera promedio de cada filósofo.

**3.** Implementar búsqueda paralela en un arreglo de 100,000,000 de números: dividir el arreglo entre $N$ hilos, cada hilo busca en su segmento y reporta los índices donde encuentra el valor. Medir el speedup para $N = 1, 2, 4, 8, 16$ núcleos y comparar con la ley de Amdahl.

**4.** Implementar multiplicación de matrices $1000 \times 1000$ usando paralelismo: versión secuencial vs. versión con pool de hilos donde cada hilo calcula una fila de la matriz resultado. Medir el speedup y la eficiencia para distintos tamaños de pool.

**5.** Implementar el problema de los lectores-escritores con prioridad a los lectores: múltiples hilos pueden leer simultáneamente la base de datos de vuelos del aeropuerto de Tijuana, pero solo uno puede escribir a la vez y las escrituras no deben esperar indefinidamente.

## Programación Asíncrona

**6.** Implementar un crawler web asíncrono con asyncio (Python) o Node.js: dado el sitio web del TecNM, descargar concurrentemente todas las páginas del dominio sin superar 10 conexiones simultáneas. Medir el tiempo total vs. la versión secuencial. Respetar el archivo `robots.txt`.

**7.** Construir un sistema de notificaciones asíncrono para el sistema escolar: cuando un docente publica calificaciones, enviar emails a todos los alumnos de la materia de forma asíncrona. Si un envío falla, reintentarlo hasta 3 veces con backoff exponencial. El docente no debe esperar a que terminen todos los envíos.

**8.** Implementar el patrón async/await para consumir 5 APIs externas en paralelo: tipo de cambio del Banxico, precio del petróleo, temperatura en CDMX, dólar en efectivo (casas de cambio) y precio del Bitcoin. Consolidar las respuestas en un dashboard y mostrar cuánto tardó cada llamada. Si alguna falla, mostrar el último valor conocido en caché.

**9.** Implementar un pipeline de procesamiento de datos asíncrono con backpressure: el sistema lee registros de un archivo CSV de 10,000,000 de filas, los transforma (limpieza, validación, enriquecimiento con API externa), y los inserta en base de datos. La etapa de inserción debe poder señalar que está sobrecargada para reducir la velocidad de lectura.

## Sistemas Distribuidos

**10.** Implementar un sistema de caché distribuida simplificado (tipo Redis Cluster): 3 nodos que se distribuyen las claves por hash consistente. Si un nodo cae, sus claves se redistribuyen automáticamente entre los restantes. Simular fallos de nodos y verificar que el sistema sigue funcionando.

**11.** Implementar el algoritmo de consenso de Raft simplificado para 3 nodos: elección de líder, replicación de log y detección de fallos por heartbeat. Demostrar que si el líder cae, el sistema elige un nuevo líder y continúa operando en menos de 500ms.

**12.** Construir un sistema de mensajería pub/sub con persistencia: publicadores envían mensajes a tópicos (pedidos, pagos, envíos), suscriptores reciben mensajes de su interés. Si un suscriptor está offline, los mensajes se acumulan y se entregan cuando vuelve. Garantizar entrega at-least-once.

**13.** Implementar circuit breaker para las llamadas a APIs externas del sistema de reservaciones del aeropuerto de Tijuana: si una API falla más de 5 veces en 60 segundos, el circuit breaker se abre y devuelve respuestas cacheadas hasta que la API se recupere. Implementar los tres estados: cerrado, abierto y semi-abierto.

**14.** Diseñar e implementar un sistema de logs distribuidos: múltiples servicios envían logs a un colector central por UDP (sin bloquear al servicio que envía), el colector los agrega, los enriquece con metadata (hostname, servicio, timestamp) y los escribe a disco en lotes. Implementar rotación de archivos y compresión automática de logs viejos.

---

## Problemas adicionales

**15.** Implementar una cola de tareas distribuida (simplificación de Celery): workers registrados en un broker central (Redis), tareas se encolan y se distribuyen round-robin entre workers disponibles. Si un worker muere con una tarea en progreso, la tarea se reasigna automáticamente a otro worker tras un timeout.

**16.** Construir un sistema de streaming de eventos en tiempo real para el monitoreo de la red de agua potable de Tijuana: sensores envían lecturas de presión y caudal cada segundo, el sistema detecta anomalías (presión fuera de rango) en tiempo real y alerta al operador en menos de 2 segundos desde la lectura del sensor.

**17.** Implementar *sagas* para un proceso de compra distribuida en e-commerce: el proceso involucra 4 servicios independientes (inventario, pago, envío, notificación). Si cualquier paso falla, ejecutar las compensaciones correspondientes para deshacer los pasos anteriores y dejar el sistema en estado consistente.

**18.** Diseñar e implementar una estrategia de sincronización de datos entre una app móvil offline-first y un servidor: el usuario puede crear, editar y eliminar datos sin conexión, y cuando recupera internet se sincronizan los cambios con detección y resolución de conflictos (last-write-wins o resolución manual).
