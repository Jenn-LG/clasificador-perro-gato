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

--------------------------------------------------------------------------------------------
