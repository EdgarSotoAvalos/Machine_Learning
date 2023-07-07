# CNN

Este código utiliza TensorFlow y Keras para crear un modelo de red neuronal convolucional (CNN) para la clasificación de imágenes. El modelo se entrena utilizando un generador de datos de imágenes y se evalúa utilizando un conjunto de pruebas. También se muestran algunas métricas de evaluación y se generan gráficos para visualizar el rendimiento del modelo.

## Requisitos
- TensorFlow
- Keras
- numpy
- pandas
- matplotlib
- scikit-learn
- Banco de Imagenes

## Instalación
Asegúrate de tener las bibliotecas requeridas instaladas en tu entorno de Python. Puedes instalarlas utilizando pip:
```bash
  pip install tensorflow keras numpy pandas matplotlib scikit-learn
```
## Descripción del código

- Importación de bibliotecas: El código comienza importando las bibliotecas necesarias, como numpy, pandas, tensorflow y las clases relevantes de Keras.

- Generación de datos: Se definen dos generadores de datos de imágenes, uno para el conjunto de entrenamiento y otro para el conjunto de validación. Los generadores aplican transformaciones a las imágenes, como escalamiento, corte y volteo, para aumentar la variabilidad de los datos. También se especifica el tamaño de las imágenes de entrada y la proporción de validación.

- Configuración de generadores: Se configuran los generadores de datos para leer las imágenes de los directorios de entrenamiento y validación. También se especifica el tamaño del lote y el tipo de clase (en este caso, binario).

- Construcción del modelo: Se crea un modelo secuencial utilizando la clase Sequential de Keras. El modelo consta de capas convolucionales, capas de agrupación máxima, una capa de aplanamiento y capas totalmente conectadas. Se utiliza la función de activación ReLU en las capas convolucionales y la función de activación sigmoide en la capa de salida.

- Compilación del modelo: El modelo se compila especificando el optimizador, la función de pérdida y las métricas a utilizar durante el entrenamiento.

- Resumen del modelo: Se imprime un resumen del modelo, mostrando la arquitectura y el número de parámetros entrenables.

- Entrenamiento del modelo: Se entrena el modelo utilizando el generador de datos de entrenamiento. Se especifica el número de pasos por época y el número total de épocas. También se utiliza el generador de datos de prueba para la validación durante el entrenamiento.

- Visualización de la precisión y la pérdida: Se traza la precisión y la pérdida del modelo durante el entrenamiento y la validación utilizando la biblioteca matplotlib.

- Predicciones y evaluación: Se realizan predicciones en el conjunto de prueba utilizando el modelo entrenado. Las predicciones se convierten en etiquetas binarias y se calculan diversas métricas de evaluación, como la matriz de confusión, la precisión, la recuperación y la puntuación F1.


