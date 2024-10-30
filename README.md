# Practica_8
## Integrantes:
- Luis Fernando Duarte Reséndiz.
  
- Mauricio Alberto Gómez Arroyo.

- Diego Brandon Guzmán Sierra.

- Bryan Hiadim Vera Hernández.

## Introducción

La práctica tiene como objetivo programar el robot utilizando la función "Pallet", un comando previamente implementado en la práctica anterior. En esta ocasión, la función será utilizada para realizar el acomodo preciso de fusibles a lo largo de una superficie, permitiendo su organización en una matriz de 3x2. Esto implica la declaración de una estructura matricial que asigna de manera automática cada fusible a una posición específica, siguiendo las coordenadas predefinidas para cada punto de la matriz.

Gracias a esta configuración, el robot puede posicionar los fusibles sin intervención manual, ajustándose a una secuencia ordenada que facilita tanto su almacenamiento como su acceso posterior. La automatización del acomodo es especialmente útil para mejorar la eficiencia y precisión en el proceso de manipulación de piezas pequeñas, como los fusibles, optimizando el tiempo de operación y reduciendo el margen de error.

## Instrucciones

### 1. Uso de la función Pallet
La función Pallet necesita algunos parámetros para su correcto funcionamiento. Los cuales son los mismos que se utilizaron en la práctica pasada.

Siendo los mismos, es decir que se seguiran usando el Pallet 0 y las mismas coordenadas para definir el área de trabajo. Teniendo las mismas posiciones (1º punto = esquina inferior izquierda, 2º = esquina inferior derecha y 3º = esquina superior izquierda). De igual manera se utilizan las mismas coordenadas como se muestra en la imagen.

![image](https://github.com/user-attachments/assets/093fb58c-a417-4cbc-ab27-7a51b3ec43a3)

Ahora bien, a diferencia de la práctica pasada el comando utilizado cambia para generar una matriz de 3x2 obteniendo lo siguiente:

<h1>***Pallet 0, E1, E2, E3, 3, 2*</h1>

