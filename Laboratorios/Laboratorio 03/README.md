# IEE2463 - Laboratorio 3

## Comentarios generales

Aquellos que lograron ver el archivo el día de ayer, deben notar la nueva Task #1, que es la final. Este archivo ya no sufrirá modificaciones. A modo de sugerencias para este laboratorio, les recomendamos comenzar de la siguiente forma:


### PWM 

0. Estudiar qué es un timer, qué es una PWM (Pulse Width Modulation) y cómo se relaciona el timer en la generación de una PWM. Información hay bastante disponible en la web y en los datasheet. Un buen punto de partida (no exclusivo) es la [siguiente página](https://www.electroschematics.com/9941/avr-pwm/)
	- Determinar de cuantos bits son los timer de cada microcontrolador y cuántos tiene cada uno. 
	- (Lean las primeras páginas del datasheet para obtener información rápida de esto)

1. Realizar un código de prueba que permita controlar una PWM en alguno de los microcontroladores, ya sea cambiando el duty cycle a intervalos regulares (que suba y baje linealmente) o definiendo un valor fijo y cambiarlo por código al compilarlo. 

2. Realizar la misma acción en el otro microcontrolador, programando una PWM para cambiar el duty cycle de alguna forma definida por usted. 

3. Intentar responder las siguientes preguntas ? 
	- ¿qué modo de operación del útil para generar una PWM ?
	- ¿por qué escogí el modo de operación anterior?
	- ¿cómo puedo generar una nueva PWM manteniendo el valor de la anterior?
	- ¿qué microcontrolador me permitirá tener 3 PWM, con valores de duty cycle distintos, en pines distintos y funcionando en paralelo? 
	
4. Programar un código que tenga más de una PWM funcionando en paralelo. Elegir un microcontrolador para cada Task.


### ADC

0. Estudiar que es un ADC (Analog Digital Converter), para poder determinar cuál es su utilidad y cómo puede ser usado en el laboratorio. Información hay bastante disponible en la web y en los datasheet. Un buen punto de partida (no exclusivo)
 es la [siguiente página](https://www.electroschematics.com/10053/avr-adc/).

1. Determinar los modos de operación del ADC y determinar las diferencias existentes en cada uno de los modos de operación, con el obtjetivo de responder a las siguientes preguntas.

	- ¿Qué es necesario configurar para realizar una conversión de ADC? 
	- ¿Qué modo de operación es útil? 
	- ¿Por qué escogí el modo de operación anterior? 
	- Algunos microcontroladores tienen una arquitectura de 8 bits, ¿cómo puedo trabajar con un ADC que me entrega un valor en 8, 10 u 12 bits ? (HINT: Most significant bits and less significant bits.)

2. Con lo anterior, determine el rango entre los que se mueve su señal de ADC y cómo esta puede ser utilizada para configurar una PWM. 

3. Realice un script de prueba que permita modificar una PWM con una medición de ADC y ver cómo esta varía al girar el potenciómetro entregado. 

4. Repetir el paso anterior para cada microcontrolador.


## Task 1

Una vez terminados los pasos anteriores ydeterminado el microcontrolador a utilizar, el paso siguiente, es hacer comenzar a hacer el código para el task 1. Formas de comenzar esto hay varias, recomendamos siempre comenzar de un caso base:

	1. Comenzar con una PWM y un ADC, realizando la conversión de la medición pertinente (ojo con los tipos de variables).
	2. Agregar una PWM y controlar ambas con ADC
	3. Agregar un botón y poder seleccionar que canal controlar (puede agregar un led de visualizador para que conozca en qué estado se encuentra).
	4. Volver al paso 2 si es que algo falla.
	5. Agregar un nuevo canal y crear una máquina de 3 estados que permita modificar cada PWM por separado mediante el ADC. 
	6. Realizar los ajustes necesarios para dejar el código operativo


## Task 2

Escoger el siguiente microcontrolador (recuerde que debe ser distinto para cada Task), en el que ya debería tener un código que permita variar una PWM con un ADC conectado al potenciómetro. Ahora deberá ajustar los valores para que se comporte como debe.

	1. Estudiar el datasheet del fotodiodo incluido en el enunciado. 
	2. Determinar valores de resistencia a ciertos niveles de luz
	3. Convertir esos valores de resistencia a voltaje a medir por el ADC
	4. Probar las mediciones con el fotodiodo conectado al ADC
	5. Volver al paso 3 hasta obtener el resultado esperado.
	6. Iterar.