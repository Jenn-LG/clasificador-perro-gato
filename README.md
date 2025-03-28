![MCD](https://mcd.unison.mx/wp-content/themes/awaken/img/logo_mcd.png)
# Clasificación de imágenes de perros y gatos usando redes neuronales densas y convolucionales

## Descripción

En este repositorio se implementa un clasificador que puede distinguir entre perros y gatos, basándose en las técnicas demostradas en el video de (Ringa Tech)[`https://www.youtube.com/watch?v=DbwKbsCWPSg`].

Para obtener los modelos se realizó el siguiente trabajo:

1. Configurar un entorno adecuado para las versiones de librerías que se van a utilizar.
2. Importar las librerías necesarias (por ejemplo, `tensorflow==2.15.0`, `numpy`, `keras`, etc.).
3. Cargar el dataset.
4. Procesar las imágenes con las librerías `cv2` y `numpy`.
5. Dividir en conjuntos de entrenamiento y validación.
6. Realizar aumento de datos usando `ImageDataGenerator`.
7. Crear un modelo denso y uno convolucional, ajustarlos y evaluarlos, además de sus gráficas accuracy, pérdida y matrices de confusión.
8. Guardar los modelos en archivos con formato `.h5`.
9. Mediante el uso de `tensorflowjs` convertir los modelos en `.json` y `.bin` para generar la página web (usando Vercel).


## Desafíos y limitaciones

La incompatibilidad de las librerías fue un desafío muy grande y consumió la mayoría del tiempo requerido para este proyecto. Después de batallar mucho con las versiones de `Tensorflow` y `tensorflowjs`, se realizó el proceso de la conversión mediante otro script reinstalando las versiones de las libreías instaladas previamente.
Al final, creí que lo había logrado pero el modelo se creo con Tensorflow 2.19.0 en lugar de 2.15.0, no se en que momento se cambió, por lo que al crear la página, no cargaban los modelos porque el tamaño no coincidía.

--------------------------------------------------------------------------------------------
P.D: Agradecimiento especial a (Kevin)[https://github.com/KevinMundo11] ya que me ayudó con la costrucción de los botones en el html y por eso no tuve problemas en esa parte. Además para la página me dió sus archivos .json y .bin los cuales no tenián problema con el tamaño porque lo corrió en colab.
Los que envié por teams, son mis archivos originales.
