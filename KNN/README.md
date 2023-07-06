# KNN

Este código es parte de la "Práctica 2" donde el objetivo de esta práctica es utilizar el algoritmo de clasificación K vecinos más cercanos (K-Nearest Neighbors) para analizar un conjunto de datos de flores Iris y evaluar el desempeño del modelo utilizando diferentes valores de k.

## Requisitos
Antes de ejecutar este código, asegúrate de tener instaladas las siguientes bibliotecas de Python:

- scikit-learn: Esta biblioteca proporciona herramientas para el aprendizaje automático, incluyendo conjuntos de datos de muestra y algoritmos de clasificación.
Puede ser instalado de esta manera:
```bash
  pip install scikit-learn
```
## Descripción del código

El código consta de los siguientes pasos:

Importación de bibliotecas y módulos necesarios:

  - load_iris de sklearn.datasets para cargar el conjunto de datos Iris.
  - KNeighborsClassifier de sklearn.neighbors para crear un clasificador K vecinos más cercanos.
  - StratifiedKFold de sklearn.model_selection para realizar validación cruzada estratificada.
  - numpy para realizar operaciones numéricas.
  - Varias métricas de evaluación, como accuracy_score, precision_score, recall_score y f1_score, de sklearn.metrics para evaluar el rendimiento del modelo.

Carga de los datos de flores Iris:

- Se utiliza la función load_iris() para cargar los datos en el objeto iris.
- Las características se almacenan en la variable X y las etiquetas en la variable y.

Definición de los valores de k:

- Se define una lista de valores de k (número de vecinos más cercanos) a evaluar. En este caso, se utilizan los valores 1, 4 y 7.

Inicialización de listas para almacenar las métricas:

- Se definen varias listas para almacenar los valores de las métricas de evaluación para cada valor de k.

Validación cruzada y evaluación del modelo:

- Se utiliza la validación cruzada estratificada con 10 pliegues (StratifiedKFold) para dividir los datos en conjuntos de entrenamiento y prueba de manera estratificada.
- Para cada pliegue y cada valor de k, se realiza lo siguiente:
  - Se crea un clasificador K vecinos más cercanos (KNeighborsClassifier) con el valor actual de k.
  - Se entrena el modelo utilizando el conjunto de entrenamiento.
  - Se realizan predicciones en el conjunto de prueba.
  - Se calculan las métricas de evaluación (exactitud, precisión, sensibilidad y puntuación F1) utilizando las etiquetas verdaderas del conjunto de prueba y las predicciones realizadas por el modelo.
  - Se agregan los valores de las métricas a las listas correspondientes según el valor de k.
  - Se imprimen los resultados de cada ejecución.

Cálculo de promedios:

- Se calculan los promedios de las métricas para cada valor de k utilizando la función np.mean().

Impresión de los resultados:

- Se imprimen los promedios de las métricas para cada valor de k.

Ejecución del código
- Para ejecutar este código, sigue los siguientes pasos:

  - Asegúrate de tener instaladas las bibliotecas mencionadas en los requisitos.

  - Copia y pega el código en un entorno de desarrollo de Python o en un archivo de script con extensión .py.

  - Ejecuta el código.

## Autores

- [@EdgarSotoAvalos](https://github.com/EdgarSotoAvalos)
