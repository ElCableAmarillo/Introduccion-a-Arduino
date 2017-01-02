# Introducción a Arduino

<img src="ElCableAmarillo.png" /><br>
*Fondo Europeo de Desarrollo Regional - Una manera de hacer Europa*



***



En este apartado explicamos las principales características de nuestra placa de Arduino, y como instalar el software que utilizaremos para programar.

- [Qué es Arduino](#qué-es-arduino)
    - [Hardware](#hardware)
    - [Software](#software)
- [Arduino IDE](#arduino-ide)
    - [Instalar Arduino IDE](#instalar-arduino-ide)
        - [Arduino IDE en Linux](#arduino-ide-en-linux)
        - [Arduino IDE en Windows](#arduino-ide-en-windows)
        - [Arduino IDE en Mac](#arduino-ide-en-mac)
- [Scratch 4 Arduino](#scratch-4-arduino)
    - [Instalar Scratch 4 Arduino](#instalar-scratch-4-arduino)
    - [Cargar el Firmware](#cargar-el-firmware)



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


<br /><br />


## Arduino IDE

Arduino IDE es un editor de texto y compilador para programar y transferir el contenido de las instrucciones a la placa de Arduino en su lenguaje máquina. El lenguaje de programación utilizado es [Processing](https://processing.org/).

El Software Arduino IDE se compone de 3 partes principalmente:
- **Botonera** o barra de navegación:
    - *Verificar*: Se encarga de verificar la sintaxis de nuestro programa.
    - *Cargar*: Si la verificación ha sido correcta, podemos cargar el código en nuestra placa de Arduino.
    - *Nuevo*: Simplemente abrimos un documento vacio (salvo funciones principales) para comenzar un nuevo programa.
    - *Abrir*: Para abrir proyectos en otros directorios o rutas.
    - *Guardar*: Simplemente guarda el programa en el directorio que especifiquemos (si es la primera vez que lo guardamos).
    - *Monitor serial*: Supongamos que necesitamos saber en algún momento qué ocurre dentro de nuestra placa de Arduino, pues bien, mediante el monitor serial podemos enviar datos que se mostrarán en nuestro monitor.
- **Editor** de programación: Es la parte principal de Arduino IDE, básicamente donde se programan las líneas y líneas de código en lenguaje processing.
- **Notificaciones**: Conocido normalmente por consola, es la parte de depuración donde notifica al programador sobre errores de sintaxis, comunicación, etc.

![Software Arduino IDE](Imágenes/Software Arduino IDE.png)


<br />


### Instalar Arduino IDE

En primer lugar debemos acceder y descargar el software desde la página web [Arduino.org](http://www.arduino.org). Dependiendo del sistema operativo que utilicemos procederemos a una de las siguientes instalaciones.

- [Arduino IDE en Linux](#arduino-ide-en-linux)
- [Arduino IDE en Windows](#arduino-ide-en-windows)
- [Arduino IDE en Mac](#arduino-ide-en-mac)


<br />


#### Arduino IDE en Linux

Nos hemos basado en la distribución **Ubuntu** para realizar esta guía de instalación puesto que la mayoría de las distribuciones de Linux a nivel educativo se basan en ella.

Para trabajar con Arduino es preciso que nuestra distribución tenga instalados los siguientes paquetes además de Arduino IDE.

```
- sun's java runtime (jre)
- gcc-avr
- avr-libc
- binutils-avr
```

Para instalar dichos paquetes vamos a necesitar la clave de administrador. A continuación abrimos un nuevo terminal o consola y ejecutamos las siguientes instrucciones:

```
$ sudo add-apt-repository ppa:arduino-ubuntu-team
$ sudo apt-get update
$ sudo apt-get install arduino
```

Para ejecutar la aplicación de Arduino IDE, basta con acceder al menú *Aplicaciones > Programación > Arduino*.


<br />


#### Arduino IDE en Windows

Descargamos el software de Arduino desde la sección de descargas de la página web [Arduino.org](http://www.arduino.org/downloads) y procedemos a ejecutar el programa descargado aceptando la licencia de uso y siguiendo los pasos que aparecen en el instalador.


<br />


#### Arduino IDE en Mac

De igual manera que en el caso de instalación en Windows, en primer lugar descargamos el software de Arduino desde la sección de descargas de la página web [Arduino.org](http://www.arduino.org/downloads) y procedemos a ejecutar el programa descargado aceptando la licencia de uso y siguiendo los pasos que aparecen en el instalador.



<br /><br />



## Scratch 4 Arduino

Scratch 4 arduino es una modificación del software libre Scratch que nos permite crear programas para Arduino UNO, pero teniendo en cuenta que los proyectos siempre serán dependientes de la conexión con S4A.

Está basado en el lenguaje de programación por bloques y sus instrucciones han sido diseñadas con un lenguaje natural, eliminando términos técnicos y empleando una terminología más natural. Así se facilita el acceso a la programación en niveles educativos básicos.

El Software Scratch 4 Arduino se compone de 5 partes principalmente:
- **Grupo de instrucciones** clasificadas por colores en las siguientes categorías:
    - *Movimiento*: Conjunto de instrucciones relacionadas con el control de los pines de la tarjeta de Arduino, asñi como el control del movimiento de cualquier personaje del escenario.
    - *Apariencia*: Instrucciones orientadas a modificar el aspecto de los personajes de nuestra aplicación. Para el caso de arduino, es un conjunto de instrucciones que apenas se utiliza.
    - *Sonido*: Conjunto de instrucciones relacionadas con la elaboración de aplicaciones musicales, emitiendo sonidos y notas musicales.
    - *Lápiz*: Scratch nos ofrece la posibilidad de que los personajes dejen un rastro durante sus movimientos por el escenario como si arrastrase un lápiz durante su trayectoria. Este rastro se genera con las instrucciones que podemos encontrar en esta sección.
    - *Control*: Las instrucciones incluídas en esta sección son impresindibles para crear la lógica de nuestros programas. Incluyen condicionales, bucles y llamadas de acción.
    - *Sensores*: Instrucciones de iteración con el ratón, el teclado, sonidos y los personajes.
    - *Operadores*: operaciones matemáticas, lógicas y con cadenas de texto.
    - *Variables*: Instrucciones para el almacenamiento y gestión de datos.
- **Instrucciones** de programación: Las instrucciones de cada grupo corresponden a instrucciones de programación, en este caso del lenguaje de programación por bloques de Scratch (S4A).
- **Editor**: Es la parte principal donde estructuramos nuestro programa.
    - *Programas*: Se compone de todas las instrucciones que hace funcionar el código que programemos.
    - *Disfraces*: Cada objeto o sprite puede tener diferentes apariencias o disfraces para utilizar a lo largo de nuestro programa.
    - *Sonido*: También es posible añadir o grabar sonidos y guardarlos para futuros usos.
- **Escenario** o ventana principal: Es el resultado de nuestro programa.
- **Objetos** y sprites: Distinguimos principalemente lso objetos de tipo Arduino y los sprites.
    - Los *objetos* de tipo arduino son aquellos que interactuán con Arduino.
    - Los *sprites* son similares al entorno de scratch y no interactúan con Arduino.

![Software Scratch 4 Arduino](Imágenes/Software Scratch 4 Arduino.png)


<br />


### Instalar Scratch 4 Arduino

Si el usuario se siente más cómodo con entornos de programación visuales, es posible programar arduino con una variante de Scratch, esta versión se llama Scratch 4 Arduino o S4A.
 
Para ello debemos tener instalado Arduino IDE en primer lugar y en segundo lugar descargar e instalar el software desde la página web [s4a.cat](http://s4a.cat), y seguir los pasos de instalación. Independientemente del sistema operativo que utilicemos, desde la web del proyecto está disponible para Windows, Linux y Mac, siendo la instalación similar.


<br />


### Cargar el Firmware

Para que Scratch 4 Arduino reconozca la tarjeta, debemos seguir los siguientes pasos:
1. Abrir el archivo [S4AFirmware16.ino](http://vps34736.ovh.net/S4A/S4AFirmware16.ino) con Arduino.
2. Cargar el firmware en la placa de Arduino habiendo comprobado que previamente que la placa de Arduino ha sido detectada por nuestro equipo y funciona correctamente.
3. Probar que detecta correctamente nuestra placa en Scratch 4 arduino.



***



#### Licencia

<img src="http://i.creativecommons.org/l/by-sa/4.0/88x31.png" /> Esta obra se distribuye bajo licencia [Reconocimiento-CompartirIgual 4.0 Internacional (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.es_ES).
