# Introducción a Arduino

<img src="ElCableAmarillo.png" /><br>
*Fondo Europeo de Desarrollo Regional - Una manera de hacer Europa*



***



En este apartado explicamos las principales características de Arduino, y como instalar el software que utilizaremos para programar una placa de Arduino.

- [Qué es Arduino](#qué-es-arduino)
    - [Hardware](#hardware)
    - [Software](#software)
- [Instalar Arduino](#instalar-arduino)
	- [Instalación en Linux](#instalación-en-linux)
	- [Instalación en Windows](#instalación-en-windows)
	- [Instalación en Mac](#instalación-en-mac)
	- [Acceder a Arduino](#acceder-a-arduino)



***



## Qué es Arduino

**Arduino** es una plataforma para prototipado de electrónica basada en hardware y software libre y fácil de utilizar. Podemos construir circuitos electrónicos y programarlos para:
- iniciarnos en el mundo de la electrónica y robótica.
- construir componentes electrónicos a nuestro gusto.
- crear nuestro propio modelo de negocio.

![Arduino UNO Rev3](Imágenes/Arduino UNO Rev3.png)


<br />


Arduino se apoya en 2 pilares fundamentales; [Hardware](#hardware) (placa de Arduino) y [Software](#software) (entorno de programación).

### Hardware

Las principales características que podemos encontrar en nuestra placa de Arduino UNO Rev3, son las siguientes:
- El microcontrolador es un **circuito integrado programable** capaz de realizar operaciones matemáticas complejas a gran velocidad.
- Normalmente el modo de alimentación de una placa de Arduino es mediante el puerto USB mientras se está programando, pero hay ocasiones en la que necesitamos que el código de nuestra placa se siga ejecutándose sin estar conectado al equipo. Probablemente la forma más habitual de alimentar Arduino (sin utilizar tu equipo) es mediante una fuente de alimentación o pila de 9V. 
- Arduino dispone de un **regulador de voltaje interno** que actúa para que la tensión de alimentación no supere los 12V, ya que en caso contrario podemos dañar el regulador y con ello la placa de Arduino. Por otro lado, para tensiones inferiores a 7V en la alimentación, es probable que la placa no llegue a encenderse. La mayoría de los componentes electrónicos de Arduino utilizan una tensión operativa de 5V (ya regulada).
- Tanto las **entradas** como las **salidas** dotan al sistema de información y realizan diferentes actuaciones.

| Características Arduino UNO Rev3           |           |
| ------------------------------------------ | --------- |
| Microcontrolador                           | ATmega328 |
| Tensión operativa                          | 5V        |
| Tensión de alimentación                    | 7-12V     |
| Entradas digitales                         | 14        |
| Salidas digitales                          | 14        |
| Entradas analógicas                        | 6         |
| Memoria flash                              | 32Kb      |
| SRAM                                       | 2Kb       |
| EEPROM                                     | 1Kb       |
| Velocidad del reloj                        | 16MHz     |
| Máxima VC para entradas                    | 40mA      |
| Máxima VC para pines 3.3V                  | 50mA      |


<br />


Arduino contiene la siguiente distribución de pines:
- Disponemos de **14 pines digitales** que pueden ser configurados como entradas o salidas, de los cuales (serigrafiadas con el símbolo ~) pueden ser utilizados como señales digitales **PWM 6 pines**.
- Igualmente diponemos de **6 pines analógicos** serigrafiadas desde A0 hasta A5 para las entradas analógicas.
- También disponemos de **3 pines GND** para conectar a tierra nuestros circuitos.
- Y por último **2 pines de alimentación** de 5V y 3.3V respectivamente.

![Pines Arduino UNO Rev3](Imágenes/Pines Arduino UNO Rev3.png)

| Pines Arduino UNO Rev3  |           |
| ----------------------- | --------- |
| Entradas digitales      | 14        |
| Salidas digitales       | 14        |
| Salidas PWM       	  | 6         |
| Entradas analógicas     | 6         |
| GND (tierra)            | 3         |
| VCC 3.3V                | 1         |
| VCC 5V                  | 1         |


<br />


### Software

Independientemente del lenguaje de programación que vayamos a utilizar, es indispensable tener instalado en primer lugar el software [Arduino IDE](#arduino-ide), aunque también vamos a instalar [Scratch 4 Arduino](#scratch-4-arduino) para programar utilizando un lenguaje de programación por bloques.

![Software](Imágenes/Software.png)


<br />


#### Arduino IDE

El Software Arduino IDE se compone de 3 partes principalmente:
- Barra de navegación o botonera con diferentes botones:
    - Verificar: Se encarga de verificar la sintaxis de nuestro programa.
    - Cargar: Si la verificación ha sido correcta, podemos cargar el código en nuestra placa de Arduino.
    - Nuevo: Simplemente abrimos un documento vacio (salvo funciones principales) para comenzar un nuevo programa.
    - Abrir: Para abrir proyectos en otros directorios o rutas.
    - Guardar: Simplemente guarda el programa en el directorio que especifiquemos (si es la primera vez que lo guardamos).
    - Monitor serial: Supongamos que necesitamos saber en algún momento qué ocurre dentro de nuestra placa de Arduino, pues bien, mediante el monitor serial podemos enviar datos que se mostrarán en nuestro monitor.
- Editor: Es la parte principal de Arduino IDE, básicamente donde se programan las líneas y líneas de código en lenguaje processing.
- Notificaciones: Conocido normalmente por consola, es la parte de depuración donde notifica al programador sobre errores de sintaxis, comunicación, etc.

![Software Arduino IDE](Imágenes/Software Arduino IDE.png)


<br />


#### Scratch 4 Arduino

El Software Scratch 4 Arduino (S4A) se compone de 5 partes principalmente:
- Grupo de instrucciones clasificadas por colores en las siguientes categorías:
    - Movimiento: Conjunto de instrucciones relacionadas con el control de los pines de la tarjeta de Arduino, asñi como el control del movimiento de cualquier personaje del escenario.
    - Apariencia: Instrucciones orientadas a modificar el aspecto de los personajes de nuestra aplicación. Para el caso de arduino, es un conjunto de instrucciones que apenas se utiliza.
    - Sonido: Conjunto de instrucciones relacionadas con la elaboración de aplicaciones musicales, emitiendo sonidos y notas musicales.
    - Lápiz: Scratch nos ofrece la posibilidad de que los personajes dejen un rastro durante sus movimientos por el escenario como si arrastrase un lápiz durante su trayectoria. Este rastro se genera con las instrucciones que podemos encontrar en esta sección.
    - Control: Las instrucciones incluídas en esta sección son impresindibles para crear la lógica de nuestros programas. Incluyen condicionales, bucles y llamadas de acción.
    - Sensores: Instrucciones de iteración con el ratón, el teclado, sonidos y los personajes.
    - Operadores: operaciones matemáticas, lógicas y con cadenas de texto.
    - variables: Instrucciones para el almacenamiento y gestión de datos.
- Instrucciones: Las instrucciones de cada grupo corresponden a instrucciones de programación, en este caso del lenguaje de programación por bloques de Scratch (S4A).
- Editor: Es la parte principal donde estructuramos nuestro programa.
    - Programas: Se compone de todas las instrucciones que hace funcionar el código que programemos.
    - Disfraces: Cada objeto o sprite puede tener diferentes apariencias o disfraces para utilizar a lo largo de nuestro programa.
    - Sonido: También es posible añadir o grabar sonidos y guardarlos para futuros usos.
- Escenario: La ventana principal o escenario es el resultado de nuestro programa.
- Objetos: Distinguimos principalemente lso objetos de tipo Arduino y los sprites.
    - Objetos de tipo arduino son aquellos que interactuán con Arduino.
    - El resto de sprites son similar al entorno de scratch y no interactúan con Arduino.

![Software Scratch 4 Arduino](Imágenes/Software Scratch 4 Arduino.png)




***



#### Licencia

<img src="http://i.creativecommons.org/l/by-sa/4.0/88x31.png" /> Esta obra se distribuye bajo licencia [Reconocimiento-CompartirIgual 4.0 Internacional (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.es_ES).
