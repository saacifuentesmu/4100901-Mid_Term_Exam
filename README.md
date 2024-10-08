# 4100901-Mid_Term_Exam
Please fork this repo, then clone it into your computer, and place your work for the Mid term exam here.

## Criterio de Evaluación 

* Funcionalidad: 60% (valor equivalente para cada requerimiento)
* Repositorio: 20% (commits entendibles que describan los cambios realizados)
* Documentación: 20% (en código y readme del repositorio)


## Instrucciones

Implemente un sistema de señales direccionales como se especifica.

### Requerimientos del sistema:

#### No funcionales:
1. Tener 2 botones: Giro Izquierda, Giro Derecha.
2. Tener 2 luces(LEDs): Luz Izquierda, Luz Derecha.
3. Tener un puerto de depuración con el PC: USART2 @256000 bauds

#### Funcionales:
4. Debe enviar mensajes con información por consola cuando se presionen los botones o hayan eventos en los LEDs.
5. Para que la presión de boton sea valida, se debe tener presionado el botón durante 100ms.
6. Si un botón de giro se presiona 1 vez: la luz del lado correspondiente parpadea 3 veces.
7. Si un botón de giro se presiona 2 o mas veces durante 500ms: la luz del lado correspondiente parpadea indefinidamente.
8. Si un botón de giro se presiona y la luz del otro lado esta activa: se desactiva la luz del otro lado.
9. Si los dos botones se presionan en menos de 500ms: las luces se comportan como las estacionarias de un carro.
10. La frecuencia de parpadeo de las luces debe ser de 4Hz.
