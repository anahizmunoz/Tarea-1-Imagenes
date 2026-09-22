# Tarea 1 - Procesamiento de Imágenes

Las preguntas fueron desarrolladas en Google Colab, por lo que las instrucciones de uso y ejemplos presentados a continuación están basados en dicho entorno.

## Pregunta 1: 

### Librerías necesarias
- cv2
- cv2_imshow
- numpy

### Descripción
La solución se divide en dos funciones: una función auxiliar encargada de realizar la interpolación entre los puntos de control y una función principal llamada `ColorSaturation`.
La función principal recibe una imagen en formato RGB, un arreglo de puntos de control y un modo de operación. Actualmente se puede trabajar en espacio HS (utilizando HSV) o en espacio CIE L*c*h*.

### Ejemplo de uso
```python
imagen = cv2.imread("/content/P1_IMG_2402.tif")
imagen = cv2.cvtColor(imagen, cv2.COLOR_BGR2RGB)
puntos = [(x, x), (x1, x1)]
resultado = ColorSaturation(imagen, puntos, "HS")
cv2_imshow(cv2.cvtColor(resultado, cv2.COLOR_RGB2BGR))
```

## Pregunta 2: 
### Librerías necesarias

- numpy
- cv2
- cv2_imshow

### Descripción
La función recibe cinco parámetros:
- `imagen`: imagen en escala de grises.
- `tamano_region`: tamaño de las regiones utilizadas para el procesamiento.
- `separacion`: distancia entre regiones consecutivas.
- `contraste`: factor de ajuste de contraste.
- `nro_bins`: cantidad de niveles de intensidad utilizados para construir los histogramas.

### Ejemplo de uso
```python
imagen = cv2.imread("/content/P2_IMG_2423.tif")
imagen = cv2.cvtColor(imagen, cv2.COLOR_BGR2GRAY)

resultado = ecualizacion_local(imagen, 1, 25, 20, 256)

cv2_imshow(cv2.cvtColor(resultado, cv2.COLOR_GRAY2RGB))
```
## Pregunta 3
### Librerías necesarias

- numpy
- cv2
- cv2_imshow

### Descripción

La función recibe tres parámetros:

- `imagen`
- `factor`
- `modo`

Se recomienda entregar la imagen en formato RGB o en escala de grises. La función puede trabajar correctamente con cualquiera de los dos formatos. 
