# Clasificación de imágenes de perros y gatos usando redes neuronales densas y convolucionales

## Descripción

En este repositorio se utilizan redes neuronales sobre un conjunto de imágenes de `tensorflow-datasets`. Dicho conjunto consta de imágenes de perros y gatos.

Para obtener los modelos convolucionales, de manera general, se realizó el siguiente trabajo:

1. Configurar un entorno adecuado para las versiones de librerías que se van a utilizar.
2. Importar las librerías necesarias (por ejemplo, `tensorflow==2.15.0`, `numpy`, `keras`, etc.).
3. Cargar el dataset.
4. Procesar las imágenes con las librerías `cv2` y `numpy` (una vez convertidas en arreglos).
5. Dividir en conjuntos de entrenamiento y validación.
6. Realizar aumento de datos usando `ImageDataGenerator`.
7. Crear un modelo usando redes neuronales convolucionales, ajustarlo y evaluarlo, generando matrices de confusión, curvas de pérdida y accuracy.
8. Repetir el punto 7 pero con una red neuronal densa.
9. Guardar los modelos en archivos con formato `.h5`.

Una vez creados los modelos, utilizamos `tensorflowjs` para convertirlos en archivos `.json` y sus respectivos `.bin`.

Posteriormente, se creó este repositorio que nos permite implementar nuestro modelo como una página en línea usando `Vercel`.

Dicha página cuenta con:
- Dos botones para seleccionar el modelo a utilizar para la clasificación de imágenes
- Un botón para activar el modo oscuro
- Un espacio para proyectar la cámara web
- Un enlace que redirige a este repositorio de GitHub

## Desafíos y limitaciones

La mayor parte del tiempo se dedicó a resolver problemas con el versionado de las librerías, tanto que no fue posible crear un archivo `.yml` o `.txt` que contuviera la información del entorno. No se realizó una búsqueda de hiperparámetros debido a que dependíamos de la velocidad de ejecución en `Colab`; al realizar varios intentos, la GPU dejaba de funcionar.

## Libretas de JupyterLab

Dado que la mayor parte del trabajo se realizó en `Colab`, se incluyen los enlaces a las dos libretas utilizadas:

1. **Libreta principal**: Contiene todo el trabajo **excepto** la conversión de los modelos a archivos `.json` y sus respectivos `.bin`:
   - Enlace: `https://colab.research.google.com/drive/1eNcKtyuuLMWs2RCciOES8clkBVZGCgoA?usp=sharing`
   - La celda importante tiene estructura de `Script` por si se desea corregir la limitación mencionada.
   - Observación: El número de épocas en `hist_---- = modelo-----.fit(------)` es bajo (originalmente se usaron 50 para el modelo convolucional y 70 para el denso. Al cambiar estos parámetros obtendrá un accuracy alrededor de .88 y .67 para el modelo convolucional y denso, respectivamente), ya que el propósito es demostrar el funcionamiento.

2. **Libreta de conversión**: Convierte los modelos a archivos `.json` y `.bin`:
   - Enlace: `https://colab.research.google.com/drive/1iYTUIRBgjuSQncrpE28XzFAcstm9DhYE?usp=sharing`

## Importante

Este repositorio utiliza como base lo visto en el video `https://www.youtube.com/watch?v=DbwKbsCWPSg` de `RingaTech`.