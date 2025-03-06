# Entrenamiento de Red Neuronal con MNIST

## Descripción
Este script implementa una red neuronal en Keras para entrenar y evaluar un modelo de clasificación de dígitos escritos a mano utilizando la base de datos MNIST. Se carga el conjunto de datos, se preprocesan las imágenes, se define la arquitectura de la red y se entrena utilizando un optimizador.

## Requisitos
Antes de ejecutar el script, asegúrate de tener instaladas las siguientes bibliotecas:

- `numpy`
- `keras`
- `matplotlib`

Puedes instalarlas usando:
```bash
pip install numpy keras matplotlib
```

## Estructura del Código
1. **Importación de bibliotecas**: Se incluyen las librerías necesarias para el procesamiento de datos, el modelo de red neuronal y la visualización de imágenes.
2. **Carga del conjunto de datos MNIST**: Se dividen los datos en entrenamiento y prueba.
3. **Preprocesamiento**:
   - Normalización de imágenes (escalado a valores entre 0 y 1).
   - Conversión de etiquetas a formato *one-hot encoding*.
4. **Definición del modelo**:
   - Capa de entrada con 784 neuronas (28x28 píxeles aplanados).
   - Capa oculta con 512 neuronas y activación ReLU.
   - Capa de salida con 10 neuronas y activación softmax.
5. **Compilación y entrenamiento**:
   - Optimización con *RMSprop*.
   - Función de pérdida *categorical_crossentropy*.
   - Entrenamiento durante 8 épocas con lotes de 128 imágenes.
6. **Evaluación**:
   - Se evalúa la precisión del modelo en el conjunto de prueba.
   - Se muestra la precisión final en pantalla.

## Ejecución
Para ejecutar el script, simplemente corre el siguiente comando en la terminal:
```bash
python main.py
```
Si se ejecuta directamente, el modelo entrenará y evaluará automáticamente los datos de MNIST.

## Resultados
Al finalizar el entrenamiento, el script imprimirá la precisión obtenida en el conjunto de prueba. También visualizará una imagen de muestra del conjunto de datos.