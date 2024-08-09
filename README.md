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
  * S1(PA1) y S2(PA4) fueron inicializados en STM32CubeMX como EXTi (EXTi 1 y 4 habilitadas).
  * En main.c, linea 272: inicializados como IT-RISING EXTi.
  * En main.c, linea 64: las interrupciones son procesadas.
2. Tener 2 luces(LEDs): Luz Izquierda, Luz Derecha.
  * D3(PA7) y D4(PB6) fueron inicializados en STM32CubeMX como salidas.
3. Tener un puerto de depuración con el PC: USART2
  * USART2 fue inicializado en STM32CubeMX: async, 115200 bauds, 8 bits, 1 stop, no parity.

#### Funcionales:
4. Debe enviar mensajes de información por la consola cuando hayan eventos en el sistema.
  * En main.c, lineas 122 y 136: se envian mensajes por el USART2 cuando se detectan presiones de boton.
5. Si un botón de giro se presiona 1 vez: la luz del lado correspondiente parpadea 3 veces.
  * En main.c, lineas 124 y 138: variables puestas a 6 para 6 toggles (3 blinks).
  * En main.c, lineas 148 y 156: si la variable de blinks es diferente de 0, el LEd hace toggle periodicamente.
6. Si un botón de giro se presiona 2 o mas veces durante 500ms: la luz del lado correspondiente parpadea indefinidamente.
  * En main.c, lineas 127 y 141: la variable de blinks se pone al maximo possible para bliknks infinitos.
7. Si un botón de giro se presiona y la luz del otro lado esta activa: se desactiva la luz del otro lado.
  * En main.c, lineas 131 y 145: los blinks de la luz del lado contrario se deshabilitan si se presiona un boton.
8. La frecuencia de parpadeo de las luces debe ser de 2Hz.
  * En main.c, lineas 152 y 160: se hace el toggle de las luces cada 250 ms cuando estan activas.
