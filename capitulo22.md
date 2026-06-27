# Capítulo 22: Seguridad, Ética e IA Responsable

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

El programador que solo sabe construir cosas pero no sabe protegerlas ni cuestionarlas es un peligro para sus usuarios. La seguridad informática no es un complemento opcional — es una responsabilidad profesional. Y en la era de la IA, la responsabilidad va más lejos: los algoritmos que construimos pueden discriminar, manipular, vigilar y tomar decisiones que afectan millones de vidas. Este capítulo es el cierre de todo el libro: no solo enseña a programar sistemas seguros, sino a preguntarse si lo que estamos construyendo es correcto construirlo. Los problemas combinan técnica con reflexión ética, porque esa es la formación que México necesita de sus ingenieros.

## Criptografía Aplicada

**1.** Implementar desde cero el cifrado AES-128 en modo CBC: dado un mensaje de texto y una clave de 128 bits, cifrar el mensaje y luego descifrarlo verificando que se recupera el original. Sin usar librerías criptográficas — implementar las operaciones SubBytes, ShiftRows, MixColumns y AddRoundKey a partir de las especificaciones del estándar FIPS-197.

**2.** Implementar el protocolo de intercambio de claves Diffie-Hellman: dos partes (Alice y Bob) generan sus claves públicas y las intercambian por un canal inseguro. Demostrar que ambos llegan al mismo secreto compartido sin haber transmitido ese secreto. Usar un primo seguro de 2048 bits. Explicar por qué Eve, que interceptó las claves públicas, no puede calcular el secreto.

**3.** Construir un sistema de firma digital con ECDSA (Elliptic Curve Digital Signature Algorithm): generar un par de claves (privada/pública) para una entidad del SAT, firmar un mensaje (comprobante fiscal), y verificar la firma. Demostrar que modificar un solo byte del mensaje hace que la verificación falle. Usar la curva P-256.

**4.** Implementar un gestor de contraseñas seguro: almacenar las contraseñas cifradas con AES-256-GCM usando una clave derivada de la contraseña maestra mediante PBKDF2 con 100,000 iteraciones y sal aleatoria. Implementar también verificación de contraseñas con bcrypt (costo 12). Demostrar por qué almacenar contraseñas en texto plano o con MD5 es inseguro mostrando un ataque de diccionario.

**5.** Construir un sistema de certificados digitales simplificado inspirado en PKI: una CA (autoridad certificadora) firma certificados con su clave privada RSA-2048. Los clientes verifican la autenticidad del certificado de un servidor usando la clave pública de la CA. Simular un ataque de man-in-the-middle que intenta sustituir el certificado y demostrar que el sistema lo detecta.

## Seguridad de Aplicaciones Web

**6.** Implementar y demostrar los 5 ataques más críticos del OWASP Top 10 en una aplicación web de práctica (nunca en sistemas reales): SQL Injection, Cross-Site Scripting (XSS), Cross-Site Request Forgery (CSRF), Insecure Direct Object Reference (IDOR) y Server-Side Request Forgery (SSRF). Para cada ataque, implementar también la contramedida que lo previene.

**7.** Construir un escáner de vulnerabilidades básico para APIs REST: dado el endpoint base de una API de prueba, el escáner debe detectar automáticamente: endpoints sin autenticación, parámetros vulnerables a inyección, respuestas con información sensible en headers y rate limiting ausente. Reportar los hallazgos con nivel de severidad CVSS.

**8.** Implementar un Web Application Firewall (WAF) simplificado como middleware: analizar cada request entrante contra una lista de patrones maliciosos (payloads SQLi, XSS, path traversal), registrar en log los intentos detectados, bloquear el request y responder con 403. Medir la tasa de falsos positivos con tráfico legítimo y ajustar las reglas para minimizarlos sin reducir la detección.

**9.** Construir un sistema de auditoría de seguridad de dependencias: dado el `requirements.txt` o `package.json` de un proyecto, consultar la base de datos de CVEs (Common Vulnerabilities and Exposures) y reportar todas las versiones de dependencias con vulnerabilidades conocidas, su severidad CVSS y la versión segura disponible. Integrar el escáner como hook de pre-commit.

## Seguridad en IA

**10.** Implementar y demostrar ataques adversariales en una red neuronal de clasificación de imágenes: usando el método FGSM (Fast Gradient Sign Method), generar imágenes adversariales que el modelo clasifica incorrectamente con alta confianza pero que son visualmente indistinguibles del original para un humano. Calcular la perturbación mínima $\epsilon$ necesaria para engañar al modelo en el 90% de los casos.

**11.** Implementar una defensa contra ataques de envenenamiento de datos (*data poisoning*): dado un dataset de entrenamiento para clasificar correos como spam/no-spam, simular un atacante que inserta 5% de muestras envenenadas (spam etiquetado como no-spam). Implementar técnicas de detección: análisis de influencia, clustering del espacio de características y filtrado estadístico de outliers.

**12.** Construir un sistema de detección de deepfakes de audio: dado un dataset de grabaciones reales e IA-generadas de políticos mexicanos, entrenar un clasificador que distinga voz auténtica de voz sintetizada. Analizar qué características espectrales distinguen mejor ambas clases (MFCC, espectrograma, pitch, jitter). Reportar la precisión del clasificador y sus limitaciones.

**13.** Implementar una auditoría de sesgo algorítmico en un clasificador de crédito: dado un modelo que aprueba o rechaza solicitudes de crédito, calcular métricas de equidad (fairness): paridad demográfica, igualdad de oportunidades e igualdad de error predictivo, desagregadas por género, estado de origen y nivel de ingresos. Identificar si el modelo discrimina algún grupo y proponer ajustes.

## Privacidad y Datos Personales

**14.** Implementar técnicas de anonimización de datos para un dataset de expedientes médicos del IMSS: aplicar k-anonimidad (k=5) con supresión de cuasi-identificadores (edad → rango, municipio → zona), l-diversidad para atributos sensibles (diagnóstico) y t-closeness. Verificar que el dataset anonimizado cumple las tres propiedades y que la utilidad analítica se preserva.

**15.** Implementar privacidad diferencial: agregar ruido calibrado (mecanismo de Laplace) a estadísticas sobre una base de datos de salarios del IMSS de tal forma que el resultado final cumple $\epsilon$-differential privacy con $\epsilon = 1.0$. Demostrar que la presencia o ausencia de cualquier individuo cambia el resultado en menos del factor $e^\epsilon = 2.72$.

**16.** Construir un sistema de gestión de consentimientos para una app de salud que recopila datos personales: implementar el flujo completo conforme a la Ley Federal de Protección de Datos Personales en Posesión de los Particulares (LFPDPPP): solicitar consentimiento explícito por categoría de dato, registrar las decisiones con timestamp, permitir revocación en cualquier momento, y eliminar todos los datos del usuario dentro de 72 horas de solicitarlo.

## Ética en IA y Reflexión Profesional

**17.** Analizar el impacto ético de un sistema de reconocimiento facial implementado en el transporte público de Tijuana para identificar personas con órdenes de arresto: a) Identificar los grupos de derechos fundamentales involucrados (privacidad, presunción de inocencia, no discriminación). b) Calcular el impacto de una tasa de error del 1% dado el volumen de viajeros diarios. c) Proponer un diseño alternativo que alcance el objetivo de seguridad con menor costo en derechos.

**18.** Diseñar el proceso de evaluación de impacto ético (AI Impact Assessment) para un sistema de IA que determina la asignación de plazas docentes en el TecNM basándose en el historial de calificaciones de estudiantes: a) Identificar los grupos afectados y sus intereses. b) Detectar posibles fuentes de sesgo en los datos de entrenamiento. c) Proponer métricas de auditoría continua. d) Definir el proceso de apelación para decisiones automatizadas.

**19.** Construir un framework de *responsible AI* para una startup mexicana de fintech: documentar las políticas de: uso aceptable del modelo, transparencia hacia los usuarios afectados, registro de decisiones automatizadas, auditoría periódica de sesgo y proceso de revisión humana obligatoria para decisiones de alto impacto (créditos mayores a \$50,000). El framework debe cumplir con la regulación de la CNBV y el INAI.

---

## Problemas adicionales

**20.** Implementar un sistema de *honeypot* para detectar bots maliciosos en el portal de servicios del gobierno: agregar campos invisibles al HTML que ningún humano llenaría, detectar velocidades de llenado de formulario imposibles para humanos (< 2 segundos), y bloquear IPs que muestren estos patrones. Registrar los intentos detectados para análisis forense.

**21.** Construir un sistema de respuesta a incidentes (IRS) para una empresa: cuando se detecta un incidente de seguridad (acceso no autorizado, fuga de datos, ransomware), el sistema debe: a) contener automáticamente el daño (aislar el sistema afectado), b) notificar al equipo de seguridad en menos de 5 minutos, c) generar un reporte del incidente con timeline, d) activar el plan de continuidad de negocio. Implementar el plan basado en el estándar NIST SP 800-61.

**22.** Implementar un sistema de detección de fraude en tiempo real para transacciones SPEI: dado un flujo de transacciones, detectar en menos de 100ms si una transacción es potencialmente fraudulenta usando un modelo de ML entrenado con patrones históricos. Las transacciones sospechosas se marcan para revisión humana — no se bloquean automáticamente. Implementar el circuito completo: modelo, API de predicción, registro de decisiones y panel de revisión humana. Justificar por qué la decisión final debe ser humana.
