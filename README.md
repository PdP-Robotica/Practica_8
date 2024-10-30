# Práctica 8
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

Es decir que se seguiran usando el Pallet 0 y las mismas coordenadas para definir el área de trabajo. Teniendo las mismas posiciones (1º punto = esquina inferior izquierda, 2º = esquina inferior derecha y 3º = esquina superior izquierda). De igual manera se utilizan las mismas coordenadas como se muestra en la imagen.

![image](https://github.com/user-attachments/assets/093fb58c-a417-4cbc-ab27-7a51b3ec43a3)

Ahora bien, a diferencia de la práctica pasada el comando utilizado cambia para generar una matriz de 3x2 obteniendo lo siguiente:

**<h1>Pallet 0, E1, E2, E3, 3, 2</h1>**

### 2.- Obtener las coordenadas para cada fusible

Ahora bien, como se debe de recoger un fusible de cada uno de los 6 contenedores, es necesario recolectar cada posición de manera individual, obteniendo las siguientes:

![image](https://github.com/user-attachments/assets/ed536e21-7eff-46c0-9700-06529eff2bdd)

Es importante mencionar que se guardaron dos posiciones para cada fusibles, sobre el fusible y tocando el fusible, esto con el objetivo de evitar colisiones a la hora de recolectarlos.

### 3.- Escribir el código

Una vez declaradas las posiciones se procede a realizar el código obteniendo el siguiente:
```plaintext
Function main
	
Motor On
Power Low
Speed 30
Accel 30, 30
SpeedS 800
AccelS 4000, 4000
Home
On 2

	Pallet 0, E1, E2, E3, 3, 2
	Go arriba_punto1
	Move agarrar_punto1
	Off 2
	Move arriba_punto1
	Home
	Go Pallet(0, 1, 1) 
	On 2
  	Home
	Go arriba_punto2
	Move agarrar_punto2
	Off 2
	Move arriba_punto2
  	Home
	Go Pallet(0, 1, 2) 
	On 2
	Home
	Go arriba_punto3
	Move agarrar_punto3
	Off 2
	Move arriba_punto3
	Home
	Go Pallet(0, 2, 1)
	On 2
  	Home
	Go arriba_punto4
	Move agarrar_punto4
	Off 2
	Move arriba_punto4
	Home
	Move Pallet(0, 2, 2)
	On 2
	Home
	Go arriba_punto5
	Move agarrar_punto5
	Off 2
	Move arriba_punto5
	Home
	Go Pallet(0, 2, 2)
	On 2
	Home
	Go arriba_punto6
	Move agarrar_punto6
	Off 2
	Move arriba_punto6
	Home
	Go Pallet(0, 3, 2) 
	On 2
	Home

Fend

```
## Video de ejecución de la práctica


https://github.com/user-attachments/assets/449224f5-30d6-47eb-b650-a8f6637ecd92


## Conclusiones

- **Luis Fernando Duarte Reséndiz**


La integración de la función "Pallet" para organizar fusibles demostró ser una herramienta clave en la mejora de la precisión y eficiencia en la manipulación automatizada de componentes. A través de la programación de una matriz 3x2, el robot logró colocar cada fusible en su posición exacta de forma autónoma, destacando la capacidad de las tecnologías automatizadas para ejecutar tareas repetitivas con alta precisión y reducir el margen de error, beneficiando significativamente el flujo de trabajo industrial.

- **Mauricio Alberto Gómez Arroyo**

La implementación de la función "Pallet" para organizar fusibles en una matriz de 3x2 demostró ser altamente efectiva para la automatización del proceso de manipulación. La precisión del robot al seguir las coordenadas predefinidas garantiza un acomodo ordenado y eficiente de los fusibles, reduciendo significativamente el tiempo de operación y el margen de error. Este enfoque automatizado no solo optimiza el almacenamiento y acceso a las piezas pequeñas, sino que también mejora la consistencia y la productividad en el entorno de trabajo.

- **Diego Brandon Guzmán Sierra**

El uso de la función "Pallet" en la práctica permitió establecer un sistema automatizado de alta precisión para la colocación de fusibles. Esta implementación mostró cómo una programación adecuada puede reducir drásticamente la intervención manual y aumentar la consistencia en la manipulación de componentes pequeños. La configuración de la matriz 3x2 no solo facilitó el almacenamiento y acceso de los fusibles, sino que también optimizó los tiempos de operación y mejoró la eficiencia general del proceso.

- **Bryan Hiadim Vera Hernández**

La aplicación de la función "Pallet" en la práctica demostró la eficacia de las soluciones automatizadas para tareas de precisión en la industria. La organización de fusibles en una matriz de 3x2 mediante la programación del robot no solo mejoró la exactitud del acomodo, sino que también redujo considerablemente el tiempo requerido para completar la tarea. Este método automatizado permitió una gestión más ordenada y accesible de los fusibles, destacando la relevancia de la automatización para optimizar procesos industriales y reducir errores.

## Referencias

-De proyectos, A. y. D. (s/f). Manual del usuario. Epson.com. Recuperado de 	https://files.support.epson.com/far/docs/epson_rc_pl_70_users_guide_spanish_(v73r2).pdf

-Robot Epson C4 de 6 ejes compactos. (s. f.). Productos | Epson México. https://epson.com.mx/Para-el-trabajo/Rob%C3%B3tica/6-Ejes/Robot-Epson-C4-de-6-ejes-compactos/p/RC4-A601ST75
