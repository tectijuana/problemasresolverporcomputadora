
## CAPÍTULO 16: PROGRAMACIÓN ORIENTADA A EVENTOS

Este capítulo incluye problemas diseñados para ser resueltos utilizando el paradigma de programación orientada a eventos. Estos problemas se centran en la creación de aplicaciones que responden a diferentes tipos de eventos como clics de ratón, pulsaciones de teclas, eventos de temporización, y cambios de estado en la interfaz de usuario.

1. **Calculadora con Eventos de Clic**: Crea una calculadora simple con botones para los números y operaciones (+, -, *, /). Cada botón debe desencadenar un evento de clic que actualice la pantalla de la calculadora.

2. **Galería de Imágenes**: Implementa una galería de imágenes donde al hacer clic en una miniatura se muestre la imagen en tamaño completo. Usa eventos de clic para manejar la selección de imágenes.

3. **Juego de Adivinar el Número**: Crea un juego donde el usuario debe adivinar un número entre 1 y 100. Utiliza un evento para manejar las entradas del usuario y otro para verificar si el número es correcto.

4. **Formulario de Registro con Validación**: Implementa un formulario de registro que valide los campos (como correo electrónico, contraseña) al perder el enfoque (evento `blur`). Muestra mensajes de error si las validaciones fallan.

5. **Aplicación de Reloj Digital**: Crea un reloj digital que se actualice cada segundo utilizando un evento de temporización (`setInterval`). Muestra la hora actual en formato de 24 horas.

6. **Juego de Memoria**: Implementa un juego de memoria donde al hacer clic en dos tarjetas, si coinciden, permanecen descubiertas. Si no, se ocultan de nuevo. Usa eventos de clic para manejar las selecciones de tarjetas.

7. **Lista de Tareas Pendientes**: Crea una lista de tareas pendientes donde los usuarios puedan agregar tareas, marcarlas como completadas o eliminarlas. Usa eventos de clic para manejar las acciones de agregar, marcar y eliminar.

8. **Reproductor de Música**: Implementa un reproductor de música básico con controles para reproducir, pausar, detener y cambiar de pista. Usa eventos para manejar los controles.

9. **Calculadora de Edad**: Crea una aplicación que calcule la edad del usuario basándose en la fecha de nacimiento seleccionada en un control de fecha. Usa eventos para actualizar automáticamente la edad mostrada al cambiar la fecha.

10. **Ventana Modal**: Implementa una ventana modal que se abra al hacer clic en un botón y se cierre al hacer clic en un botón de cierre dentro de la ventana modal. Usa eventos de clic para abrir y cerrar la ventana.

11. **Deslizamiento de Imágenes Automático**: Crea un carrusel de imágenes que se deslice automáticamente cada 3 segundos y que también permita al usuario deslizar manualmente haciendo clic en flechas de navegación.

12. **Contador de Clics**: Implementa una aplicación que cuente el número de clics en un botón y muestre el total en la pantalla. Usa un evento de clic para incrementar el contador.

13. **Simulador de Semáforo**: Crea una simulación de semáforo que cambie automáticamente entre rojo, amarillo y verde utilizando eventos de temporización (`setInterval`).

14. **Desplegable de Menú**: Implementa un menú desplegable que se muestre al pasar el ratón sobre un elemento del menú y se oculte al mover el ratón fuera del menú. Usa eventos de `mouseover` y `mouseout`.

15. **Aplicación de Cronómetro**: Crea un cronómetro con botones para iniciar, pausar y reiniciar. Usa eventos de clic para manejar los controles y eventos de temporización para actualizar el tiempo.

16. **Cambio de Tema Dinámico**: Implementa una aplicación que permita a los usuarios cambiar entre temas claro y oscuro haciendo clic en un botón. Usa eventos para cambiar las clases CSS y aplicar los estilos correspondientes.

17. **Juego de Respuestas Múltiples**: Crea un juego de preguntas y respuestas múltiples donde el usuario pueda seleccionar una respuesta haciendo clic. Muestra si la respuesta seleccionada es correcta o incorrecta al hacer clic.

18. **Calculadora de Propinas**: Implementa una aplicación que calcule la propina y el total a pagar basándose en el importe de la factura y el porcentaje de propina seleccionado. Usa eventos para actualizar los cálculos al cambiar los valores de entrada.

19. **Formulario de Contacto con Mensajes Emergentes**: Crea un formulario de contacto que, al enviar, muestre un mensaje emergente de confirmación o error. Usa eventos de clic y de envío para manejar las acciones.

20. **Juego de Lanzamiento de Moneda**: Crea un juego donde el usuario pueda lanzar una moneda virtual haciendo clic en un botón. Muestra el resultado (cara o cruz) utilizando un evento de clic.

21. **Barra de Progreso Dinámica**: Implementa una barra de progreso que se llene al cargar una página. Usa eventos de temporización para simular el llenado progresivo.

22. **Arrastrar y Soltar**: Crea una aplicación de arrastrar y soltar donde los usuarios puedan mover elementos entre dos contenedores. Usa eventos de `dragstart`, `dragover`, y `drop` para manejar la funcionalidad.

23. **Juego de Tic-Tac-Toe**: Implementa el clásico juego de tres en raya (tic-tac-toe) para dos jugadores utilizando eventos de clic para colocar las X y O.

24. **Teclado Virtual**: Crea un teclado virtual que escriba en un área de texto al hacer clic en las teclas del teclado en pantalla. Usa eventos de clic para capturar las entradas.

25. **Filtro de Lista en Tiempo Real**: Implementa un filtro que permita a los usuarios buscar elementos en una lista. Los elementos deben filtrarse en tiempo real a medida que el usuario escribe en un campo de búsqueda.

26. **Deslizador de Volumen**: Crea un control deslizante que ajuste el volumen de un reproductor de audio. Usa eventos de `input` para cambiar el volumen.

27. **Tablero de Juego de Serpientes y Escaleras**: Implementa un juego de serpientes y escaleras donde los jugadores muevan su ficha haciendo clic en un botón para lanzar un dado.

28. **Simulador de Máquina Expendedora**: Crea una simulación de una máquina expendedora donde los usuarios puedan seleccionar un producto y pagar. Usa eventos de clic para manejar las selecciones y el pago.

29. **Validación de Tarjeta de Crédito**: Implementa una aplicación que valide los números de tarjeta de crédito en tiempo real a medida que el usuario los introduce. Usa eventos de teclado para la validación.

30. **Sistema de Notificación de Chat**: Crea un sistema de chat simple que muestre notificaciones cuando un nuevo mensaje llega. Usa eventos de temporización para simular la llegada de mensajes.

31. **Interfaz de Usuario de Juego de Rol**: Implementa una interfaz de usuario para un juego de rol donde los personajes puedan atacar, defender y usar objetos. Usa eventos de clic para manejar las acciones del jugador.

32. **Desplegables Condicionales**: Crea un formulario con campos desplegables que cambien dinámicamente su contenido basado en la selección anterior. Usa eventos de cambio (`change`) para actualizar las opciones.

33. **Juego de Lanzamiento de Dardos**: Implementa un juego de lanzamiento de dardos donde los jugadores hagan clic para lanzar un dardo a un tablero. Usa eventos de clic para determinar la posición del impacto.

34. **Interfaz de Arrastrar y Redimensionar**: Crea una aplicación donde los usuarios puedan arrastrar y redimensionar elementos en una página. Usa eventos de `mousedown`, `mousemove`, y `mouseup` para manejar la funcionalidad.

35. **Reproductor de Video con Controles**: Implementa un reproductor de video con controles para reproducir, pausar, avanzar y retroceder. Usa eventos para manejar las interacciones con los controles.

36. **Contador de Palabras en Tiempo Real**: Crea una aplicación que cuente el número de palabras y caracteres en un área de texto mientras el usuario escribe. Usa eventos de teclado para actualizar los conteos en tiempo real.

37. **Juego de Ping Pong**: Implementa un simple juego de ping pong donde el jugador controle una paleta para devolver la pelota. Usa eventos de teclado para mover la paleta y manejar las colisiones.

38. **Simulación de Semáforo Inteligente**: Crea una simulación de un semáforo que cambie de estado basándose en sensores que detecten la presencia de vehículos. Usa eventos para simular la detección de vehículos.

39. **Chat en Tiempo Real**: Implementa un chat en tiempo real donde los mensajes se envían y reciben sin recargar la página. Usa eventos de WebSocket para manejar la comunicación.

40. **Generador de Memes**: Crea una aplicación que permita a los usuarios seleccionar una imagen, escribir un texto, y generar un meme. Usa eventos de entrada para capturar y mostrar el texto sobre la imagen.

41. **Juego de Simón**: Implementa el clásico juego de Simón, donde los usuarios deben repetir una secuencia de colores haciendo clic en botones de colores que se iluminan.

42. **Simulación de Radar de Objetos**: Crea una simulación de un radar que detecte y mu

estre objetos en una pantalla. Usa eventos de temporización para actualizar la posición de los objetos detectados.

43. **Editor de Texto Simple**: Implementa un editor de texto con características como negrita, cursiva y subrayado. Usa eventos de clic para aplicar los estilos al texto seleccionado.

44. **Juego de Pesca Virtual**: Crea un juego donde los usuarios hagan clic para lanzar una caña de pescar y atrapar peces. Usa eventos de clic para lanzar y eventos de temporización para mover los peces.

45. **Juego de Carrera de Autos**: Implementa un juego de carrera de autos donde los jugadores controlen el auto usando las teclas de flecha. Usa eventos de teclado para manejar el control del auto.

46. **Simulación de Invernadero**: Crea una simulación de un invernadero donde los usuarios puedan ajustar las condiciones de luz y temperatura. Usa eventos para cambiar las condiciones y ver cómo afectan a las plantas.

47. **Juego de Atrapalos Todos**: Implementa un juego donde los usuarios deben hacer clic para atrapar objetos que caen desde la parte superior de la pantalla. Usa eventos de clic para detectar las capturas.

48. **Editor de Imágenes**: Crea una aplicación que permita a los usuarios cargar una imagen y aplicarle filtros. Usa eventos de cambio para manejar la carga de imágenes y la aplicación de filtros.

49. **Calendario Interactivo**: Implementa un calendario donde los usuarios puedan agregar, editar y eliminar eventos. Usa eventos de clic para manejar la interacción con los días del calendario.

50. **Simulación de Gestión de Semillas**: Crea una aplicación para gestionar semillas, donde los usuarios puedan plantar, regar y cosechar plantas. Usa eventos para manejar las acciones de cuidado de las plantas.

Estos problemas están diseñados para aplicar conceptos de programación orientada a eventos, proporcionando oportunidades para trabajar con diferentes tipos de eventos en aplicaciones interactivas y dinámicas.
