


## CAPÍTULO 17: PROGRAMACIÓN DECLARATIVA

Este capítulo incluye problemas diseñados para ser resueltos utilizando el paradigma de programación declarativa. Este enfoque se centra en *qué* debe lograrse en lugar de *cómo* hacerlo, utilizando lenguajes y técnicas como SQL, expresiones regulares, lógica de restricciones, y lenguaje de consulta de bases de datos.

1. **Consultas Básicas en SQL**: Escribe una consulta SQL para seleccionar todos los registros de una tabla de empleados que tengan un salario mayor a $50,000.

2. **Filtrado con SQL**: Crea una consulta SQL que seleccione los nombres de todos los estudiantes que tengan una calificación superior a 85 en una tabla de calificaciones.

3. **Agrupamiento y Agregación**: Escribe una consulta SQL para agrupar empleados por departamento y calcular el salario promedio de cada departamento.

4. **Uniones en SQL**: Implementa una consulta SQL que una dos tablas, `Pedidos` y `Clientes`, para mostrar los detalles de los pedidos y la información del cliente correspondiente.

5. **Expresiones Regulares para Validación de Correos Electrónicos**: Escribe una expresión regular que valide si una cadena es un correo electrónico válido.

6. **Sustitución de Texto con Expresiones Regulares**: Utiliza expresiones regulares para encontrar y reemplazar todas las apariciones de un número de teléfono en un formato específico por otro formato en un documento de texto.

7. **Generación de Listas con Comprehensión de Listas**: Utiliza comprensión de listas para generar una lista de los cuadrados de los números del 1 al 10.

8. **Filtro Declarativo con Haskell**: Escribe una función en Haskell que filtre los números pares de una lista usando la función `filter`.

9. **Mapeo Declarativo**: Implementa una función en un lenguaje funcional como Haskell o Scala que tome una lista de cadenas y devuelva una lista con la longitud de cada cadena utilizando la función `map`.

10. **Composición de Funciones**: Escribe una función que componga dos funciones dadas y aplíquelas a una lista de números en Haskell.

11. **Declaración de Hechos en Prolog**: Define hechos en Prolog para una familia (padre, madre, hijo) y escribe reglas para determinar relaciones como hermano, abuelo, y primo.

12. **Consulta de Datos Jerárquicos**: Usa SQL para consultar una tabla jerárquica (por ejemplo, una estructura de empleados y gerentes) para mostrar todos los empleados bajo un gerente específico.

13. **Optimización de Consultas**: Escribe una consulta SQL para seleccionar los tres productos más vendidos en una tabla de ventas.

14. **Restricciones de Integridad Referencial**: Define restricciones en SQL para asegurar que cada pedido en una tabla de `Pedidos` esté asociado con un cliente válido en una tabla de `Clientes`.

15. **Filtro de Datos con XML**: Utiliza XPath para seleccionar todos los elementos de un archivo XML que contengan un atributo específico.

16. **Declaración de Regla en Prolog**: Implementa una regla en Prolog para determinar si una persona es un antepasado de otra persona basándose en hechos de padres e hijos.

17. **Consultas Recursivas en SQL**: Escribe una consulta recursiva en SQL para encontrar todos los empleados en una jerarquía de la empresa que dependen de un gerente específico.

18. **Consulta de Bases de Datos NoSQL**: Utiliza un lenguaje de consulta como MongoDB para seleccionar todos los documentos en una colección donde el campo `estado` es "activo".

19. **Definición de Datos con JSON**: Crea un esquema JSON que defina un objeto `Libro` con propiedades como `título`, `autor`, `año de publicación`, y `género`.

20. **Filtros en Plantillas de Manejo de Datos**: Utiliza un motor de plantillas como Handlebars para filtrar y mostrar solo los elementos de una lista que cumplen con una condición específica.

21. **Definición de Reglas de Negocio en Prolog**: Implementa reglas en Prolog para un sistema de control de acceso, donde los usuarios tienen diferentes niveles de acceso basados en su rol.

22. **Expresiones Regulares para Extracción de Datos**: Escribe una expresión regular que extraiga todas las URLs de un documento HTML.

23. **Declaración de Políticas de Seguridad**: Define políticas de acceso en un sistema utilizando un enfoque declarativo, especificando quién puede acceder a qué recursos y bajo qué condiciones.

24. **Transformaciones de Datos en XSLT**: Escribe una hoja de estilos XSLT para transformar un documento XML de un formato a otro.

25. **Consultas Funcionales en LINQ**: Utiliza LINQ para consultar una colección de objetos `Empleado` para seleccionar aquellos que tienen más de 5 años de experiencia.

26. **Definición de Validaciones en un Esquema de Base de Datos**: Define validaciones en una base de datos SQL para asegurar que el campo `edad` en una tabla de `Usuarios` siempre tenga un valor mayor que cero.

27. **Generación de Plantillas de Correo Electrónico**: Utiliza un lenguaje de plantillas para definir un correo electrónico que salude al usuario por su nombre y le envíe un resumen de su cuenta.

28. **Creación de Vistas en SQL**: Crea una vista SQL para mostrar solo los clientes activos y sus pedidos recientes.

29. **Filtrado de Datos en JSON**: Escribe una consulta JSONPath para seleccionar todos los elementos de un objeto JSON donde el campo `activo` es verdadero.

30. **Declaración de Condiciones de Filtro en Haskell**: Utiliza filtros en Haskell para seleccionar todos los números impares de una lista.

31. **Combinación de Consultas**: Utiliza operadores de combinación en SQL (`JOIN`) para combinar información de múltiples tablas en una sola consulta.

32. **Definición de Funciones Lambda**: Escribe una función lambda en Python para multiplicar todos los elementos de una lista por 2.

33. **Uso de Operadores de Consulta en MongoDB**: Escribe una consulta en MongoDB para encontrar todos los documentos en una colección de `productos` que tengan un precio mayor a $100.

34. **Expresiones Regulares para Dividir Cadenas**: Escribe una expresión regular que divida una cadena de texto en palabras, ignorando los signos de puntuación.

35. **Declaración de Esquemas en GraphQL**: Define un esquema en GraphQL para una aplicación de blog que incluya tipos como `Post`, `Comentario`, y `Usuario`.

36. **Consultas de Optimización en SQL**: Escribe una consulta SQL optimizada para contar el número de ventas por producto en una tabla de ventas.

37. **Definición de Cláusulas de Ordenación**: Utiliza SQL para ordenar los resultados de una consulta por la fecha de creación de forma descendente.

38. **Programación Declarativa con Terraform**: Escribe un archivo de configuración en Terraform para crear una instancia de servidor en la nube con configuraciones específicas.

39. **Declaración de Reglas de Descuento en un Sistema de Ventas**: Utiliza un lenguaje de reglas de negocio para definir descuentos aplicables basados en el tipo de producto y la cantidad comprada.

40. **Combinación de Datos con MapReduce**: Implementa una tarea MapReduce para sumar las ventas totales por región en un gran conjunto de datos.

41. **Generación de Reportes con SQL**: Crea un reporte utilizando SQL que muestre las ventas mensuales de cada producto en el último año.

42. **Definición de Políticas de Autorización en OAuth**: Configura un servidor de autorización OAuth para definir qué aplicaciones pueden acceder a qué recursos de un usuario.

43. **Validación de Contraseñas Seguras**: Escribe una expresión regular que valide contraseñas que contengan al menos una letra mayúscula, una letra minúscula, un número y un carácter especial.

44. **Consultas Declarativas en SPARQL**: Utiliza SPARQL para consultar una base de datos RDF y encontrar todos los libros escritos por un autor específico.

45. **Definición de Triggers en SQL**: Crea un `trigger` en SQL que actualice automáticamente el campo `fecha_modificación` de una tabla de `Usuarios` cada vez que se actualice un registro.

46. **Declaración de Restricciones de Unicidad**: Define una restricción de unicidad en una tabla de base de datos para asegurar que los nombres de usuario sean únicos.

47. **Filtrado y Ordenación en Elasticsearch**: Escribe una consulta en Elasticsearch para filtrar documentos que contienen una palabra clave específica y ordenarlos por relevancia.

48. **Consultas en un Grafo RDF**: Utiliza un lenguaje de consulta para grafos como Cypher para encontrar relaciones entre nodos en un grafo social.

49. **Definición de Políticas de Control de Acceso en XACML**: Escribe una política en XACML para controlar el acceso a recursos basándose en roles y atributos de usuario.

50. **Transformaciones de Datos en Pandas**: Utiliza Pandas para aplicar transformaciones de datos, como la normalización de valores numéricos en un DataFrame.

51. **Declaración de Esquemas en YAML**: Define un esquema de configuración de servidor en YAML, especificando detalles como puerto, base

 de datos y autenticación.

52. **Definición de Funciones en SQL**: Escribe una función SQL para calcular la comisión de ventas de un empleado basada en un porcentaje de sus ventas totales.

53. **Mapeo de Rutas en un Framework Web Declarativo**: Utiliza un framework web como Flask para definir rutas de URL y vistas correspondientes.

54. **Consultas Declarativas en Amazon Redshift**: Escribe una consulta para analizar grandes conjuntos de datos en un almacén de datos de Amazon Redshift, optimizando el uso de columnas y compresión.

55. **Declaración de Políticas de Seguridad de Contenidos (CSP)**: Configura una política de seguridad de contenido en un sitio web para restringir los recursos que se pueden cargar.

56. **Filtrado de Datos en un Framework Reactivo**: Utiliza un framework como React para crear un componente de filtrado de lista que responda a los cambios de entrada del usuario en tiempo real.

57. **Transformación de Datos en DataFrames con R**: Escribe un script en R para transformar y limpiar datos en un DataFrame, aplicando funciones de filtro y agregación.

58. **Creación de Consultas en un Sistema de Información Geográfica (SIG)**: Escribe una consulta en un sistema SIG para encontrar todas las ubicaciones dentro de un radio de 5 km de un punto dado.

59. **Declaración de Restricciones en XML Schema (XSD)**: Define restricciones en un esquema XML para asegurar que ciertos elementos solo contengan valores numéricos positivos.

60. **Filtrado y Agregación en Apache Hive**: Escribe una consulta en HiveQL para agrupar datos por categoría y calcular el promedio de ventas en cada categoría.

61. **Declaración de Estrategias de Caching en GraphQL**: Configura una estrategia de caching en un servidor GraphQL para optimizar la recuperación de datos.

62. **Definición de Políticas de Escalado en Kubernetes**: Utiliza un archivo de configuración de Kubernetes para definir políticas de escalado automático basadas en la carga de trabajo.

63. **Consultas Declarativas con JPA (Java Persistence API)**: Escribe una consulta en JPQL para seleccionar todos los usuarios que tienen más de 10 publicaciones.

64. **Mapeo de Datos con Apache Beam**: Implementa un flujo de trabajo en Apache Beam para transformar y filtrar datos de un flujo en tiempo real.

65. **Declaración de Esquemas en Protobuf**: Define un esquema de mensaje en Protobuf para un servicio de mensajería, especificando campos como `usuario`, `mensaje`, y `timestamp`.

66. **Consultas y Actualizaciones en una Base de Datos Orientada a Grafos**: Escribe consultas y actualizaciones para modificar los nodos y aristas en una base de datos orientada a grafos como Neo4j.

67. **Validación de Datos con JSON Schema**: Define un esquema de validación en JSON Schema para validar objetos `Producto` con campos como `nombre`, `precio`, y `disponibilidad`.

68. **Consultas Declarativas en Microsoft Power BI**: Utiliza DAX para escribir consultas que calculen medidas de ventas y filtros de datos en un informe de Power BI.

69. **Declaración de Políticas de Acceso en API Gateway**: Configura políticas de acceso en un API Gateway para restringir el acceso a ciertas rutas de la API.

70. **Consultas Declarativas en un Data Lake**: Escribe una consulta para analizar datos almacenados en un Data Lake utilizando un lenguaje de consulta específico de la plataforma, como SQL en Amazon Athena.

71. **Declaración de Estructuras de Datos en YAML**: Define una configuración de despliegue en YAML para una aplicación de microservicios, especificando contenedores, redes y volúmenes.

72. **Consultas en un Sistema de Monitoreo de Aplicaciones**: Escribe una consulta en un sistema de monitoreo como Prometheus para alertar cuando la latencia de una aplicación supere un umbral específico.

73. **Transformación de Datos con Google Dataflow**: Implementa un pipeline en Google Dataflow para procesar y transformar datos de flujos de eventos.

74. **Declaración de Eventos y Acciones en AWS Lambda**: Define eventos de disparador y acciones en un archivo de configuración para funciones Lambda en AWS.

75. **Definición de Roles y Permisos en un Sistema de Gestión de Identidad**: Utiliza un lenguaje declarativo para definir roles y permisos en un sistema de gestión de identidad, como AWS IAM.

Estos problemas están diseñados para aplicar y reforzar los conceptos de programación declarativa, proporcionando oportunidades para trabajar con lenguajes de consulta, transformaciones de datos, definiciones de reglas y esquemas, y configuraciones de políticas y seguridad.
