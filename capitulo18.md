# Capítulo 18: Inteligencia Artificial Clásica

> *Capítulo de elaboración propia — extensión moderna del libro de Donald D. Spencer para programadores mexicanos 2026*

## Introducción

Antes de usar un modelo de lenguaje, antes de llamar a una API de IA, todo programador debe entender cómo funcionan los algoritmos de aprendizaje automático desde adentro. Este capítulo implementa los algoritmos clásicos de ML desde cero — sin sklearn, sin TensorFlow, sin PyTorch — para que quede claro qué hace cada modelo, por qué funciona y cuándo falla. Los datos de entrenamiento y prueba usados en los problemas provienen de fuentes mexicanas reales: INEGI, IMSS, SEP y registros públicos disponibles.

## Regresión

**1.** Implementar regresión lineal simple con descenso de gradiente desde cero: dado un dataset de precios de vivienda en Tijuana (metros cuadrados vs. precio en MXN, 500 registros del INFONAVIT), encontrar la línea que mejor ajusta los datos. Implementar el cálculo del error cuadrático medio (MSE) y la $R^2$. Graficar la curva de aprendizaje (error vs. iteraciones).

**2.** Implementar regresión lineal múltiple usando la ecuación normal $\hat{\beta} = (X^TX)^{-1}X^Ty$. Predecir el salario mensual de egresados del TecNM a partir de: carrera, semestre de egreso, promedio, idiomas que habla y ciudad de trabajo. Usar datos del INEGI sobre egresados de IES. Interpretar los coeficientes.

**3.** Implementar regresión logística binaria con descenso de gradiente: predecir si un alumno del TecNM reprobará el semestre (1) o no (0) a partir de sus calificaciones parciales, asistencia y materias en curso. Implementar la función sigmoide, la función de pérdida de entropía cruzada y calcular precisión, recall y F1-score.

**4.** Implementar regresión polinomial de grado $k$ transformando las características: dado el crecimiento poblacional de la ZMT (Zona Metropolitana de Tijuana) de 1950 a 2020, ajustar un polinomio de grado 1, 2, 3 y 5. Identificar el grado que mejor generaliza sin sobreajuste usando validación cruzada.

## Clasificación

**5.** Implementar el clasificador k-Nearest Neighbors (kNN) desde cero: clasificar tipos de aguacate Hass de Michoacán (calidad A, B, C) a partir de peso, diámetro y color (valores RGB). Probar con $k = 1, 3, 5, 7, 11$ y seleccionar el mejor $k$ por validación cruzada de 5 pliegues.

**6.** Implementar Naive Bayes gaussiano para clasificación de texto: dado un dataset de correos del gobierno federal etiquetados como "spam" o "legítimo" (10,000 correos), entrenar el clasificador calculando la probabilidad condicional de cada palabra y la probabilidad a priori de cada clase. Reportar matriz de confusión y F1-score.

**7.** Implementar un árbol de decisión (CART) desde cero: calcular la impureza de Gini para cada posible corte, elegir el mejor corte en cada nodo y construir el árbol hasta profundidad máxima $d$. Usar el árbol para predecir si un crédito del INFONAVIT será pagado puntualmente o incurrirá en mora, a partir de 8 características del solicitante.

**8.** Implementar Random Forest como ensemble de $N$ árboles de decisión entrenados con bootstrap: comparar la precisión del bosque vs. un árbol solo para el problema de mora del INFONAVIT. Graficar la importancia de cada característica según el bosque. ¿Qué variables son más predictivas de la mora?

**9.** Implementar Support Vector Machine (SVM) con kernel lineal usando el algoritmo SMO simplificado: clasificar registros del padrón electoral en dos grupos (votó/no votó en la última elección) a partir de edad, escolaridad y distancia a la casilla. Visualizar el hiperplano de separación y los vectores de soporte.

## Agrupamiento y Reducción de Dimensiones

**10.** Implementar k-means desde cero: agrupar los 2,469 municipios de México en $k$ clusters según indicadores socioeconómicos del INEGI (IDH, cobertura de agua potable, internet, salud). Para $k = 3, 5, 8$, calcular la inercia intra-cluster y el coeficiente de silueta. ¿Cuántos grupos representan mejor la realidad?

**11.** Implementar PCA (Análisis de Componentes Principales) desde cero usando la descomposición de valores singulares (SVD): reducir el dataset de municipios de 20 dimensiones a 2 para visualizarlo. ¿Qué porcentaje de la varianza capturan las primeras 2 componentes? ¿Qué características forman cada componente?

**12.** Implementar DBSCAN (Density-Based Spatial Clustering): dado un mapa de coordenadas GPS de reportes ciudadanos en la app Mejora Tu Ciudad de Tijuana, identificar automáticamente los "puntos calientes" de problemas urbanos (baches, alumbrado, basura) sin especificar el número de clusters. Filtrar ruido (reportes aislados).

## Redes Neuronales desde Cero

**13.** Implementar un Perceptrón simple y entrenarlo con la regla del perceptrón: clasificar solicitudes de crédito bancario como aprobadas o rechazadas. Demostrar que el perceptrón no puede resolver el problema XOR y explicar por qué.

**14.** Implementar una red neuronal multicapa (MLP) con propagación hacia adelante y hacia atrás (backpropagation): arquitectura 4-8-4-1 (4 entradas, dos capas ocultas, 1 salida). Entrenarla para predecir si un paciente del IMSS tiene riesgo de diabetes tipo 2 a partir de 4 variables clínicas (IMC, glucosa en ayunas, presión arterial, edad). Sin usar ninguna librería de ML.

**15.** Implementar una red neuronal convolucional (CNN) simplificada para clasificar dígitos escritos a mano del dataset MNIST (o equivalente de dígitos de códigos postales mexicanos): una capa convolucional + pooling + capa densa. Alcanzar precisión mayor al 95% en el conjunto de prueba.

## Evaluación y Métricas

**16.** Implementar desde cero las métricas de evaluación para clasificación: precisión (accuracy), precisión por clase (precision), exhaustividad (recall), F1-score, y curva ROC con área bajo la curva (AUC). Aplicarlas al modelo de riesgo de diabetes del problema 14 y determinar el umbral de clasificación óptimo.

**17.** Implementar validación cruzada estratificada de $k$ pliegues y búsqueda de hiperparámetros (grid search): optimizar los hiperparámetros del árbol de decisión del problema 7 (profundidad máxima, mínimo de muestras por hoja, criterio de impureza). Reportar el intervalo de confianza del 95% para la precisión del modelo óptimo.

---

## Problemas adicionales

**18.** Implementar el algoritmo de Expectation-Maximization (EM) para mezcla de gaussianas: dado un dataset de tiempos de espera en módulos del SAT con distribución bimodal (hay dos turnos de atención con diferentes tiempos promedio), estimar los parámetros de las dos gaussianas componentes.

**19.** Implementar gradient boosting desde cero (una versión simplificada de XGBoost): ensemble de árboles donde cada árbol corrige los errores del anterior. Comparar con Random Forest en el problema de mora del INFONAVIT. ¿Cuál alcanza mayor precisión con el mismo número de árboles?

**20.** Construir un sistema de detección de anomalías no supervisado para transacciones financieras del SPEI: entrenar un autoencoder simple con transacciones normales y usar el error de reconstrucción como puntaje de anomalía. Calibrar el umbral para detectar el 90% de las transacciones fraudulentas con menos del 1% de falsos positivos.
