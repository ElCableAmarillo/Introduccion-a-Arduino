# Introducción a Arduino

<img src="ElCableAmarillo.png" /><br>
*Fondo Europeo de Desarrollo Regional - Una manera de hacer Europa*



=============



En este apartado explicamos las principales características de Arduino, y como instalar el software que utilizaremos para programar una placa de Arduino.

- [Qué es Arduino](#qué-es-arduino)
- [Instalar Arduino](#instalar-arduino)
	- [Instalación en Linux](#instalación-en-linux)
	- [Instalación en Windows](#instalación-en-windows)
	- [Instalación en Mac](#instalación-en-mac)
	- [Acceder a Arduino](#acceder-a-arduino)
- [Instalar S4A](#resistencias)




=============



## Qué es Arduino

**Arduino** es una plataforma para prototipado de electrónica basada en hardware y software libre y fácil de utilizar. Podemos construir circuitos electrónicos y programarlos para:
- iniciarnos en el mundo de la electrónica y robótica.
- construir componentes electrónicos a nuestro gusto.
- crear nuestros propio modelo de negocio.

![Arduino UNO Rev3](Imágenes/Arduino UNO Rev3.png)


Arduino se apoya en 2 pilares fundamentales; *hardware* (placa de Arduino) y *software* (entorno de programación).

### Hardware

Las principales características que podemos encontrar en nuestra placa de Arduino UNO Rev3, son las siguientes:
- El microcontrolador es un *circuito integrado programable* capaz de realizar operaciones matemáticas complejas a gran velocidad.
- Normalmente el modo de alimentación de una placa de Arduino es mediante el puerto USB mientras se está programando, pero hay ocasiones en la que necesitamos que el código de nuestra placa se siga ejecutándose sin estar conectado al equipo. Probablemente la forma más habitual de alimentar Arduino (sin utilizar tu equipo) es mediante una fuente de alimentación o pila de 9V. 
- Arduino dispone de un *regulador de voltaje interno* que actúa para que la tensión de alimentación no supere los 12V, ya que en caso contrario podemos dañar el regulador y con ello la placa de Arduino. Por otro lado, para tensiones inferiores a 7V en la alimentación, es probable que la placa no llegue a encenderse. La mayoría de los componentes electrónicos de Arduino utilizan una tensión operativa de 5V (ya regulada).
- Tanto las *entradas* como las *salidas* dotan al sistema de información y realizan diferentes actuaciones.

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


![Pines Arduino UNO Rev3](Imágenes/Pines Arduino UNO Rev3.png)

Arduino contiene la siguiente distribución de pines:
- Disponemos de *14 pines digitales* que pueden ser configurados como entradas o salidas, 6 de los cuales (serigrafiadas con el símbolo ~) pueden ser utilizados como señales digitales PWM.
- Igualmente diponemos de *6 pines analógicos* serigrafiadas desde A0 hasta A5 para las entradas analógicas.
- También disponemos de *3 pines GND* para conectar a tierra nuestros circuitos.
- Y por último *2 pines de alimentación* de 5V y 3.3V respectivamente.

| Pines Arduino UNO Rev3  |           |
| ----------------------- | --------- |
| Entradas digitales      | 14        |
| Salidas digitales       | 14        |
| Salidas PWM       	  | 6         |
| Entradas analógicas     | 6         |
| GND (tierra)            | 3         |
| VCC 3.3V                | 1         |
| VCC 5V                  | 1         |




=============





#### Licencia

<img src="http://i.creativecommons.org/l/by-sa/4.0/88x31.png" /> Esta obra se distribuye bajo licencia [Reconocimiento-CompartirIgual 4.0 Internacional (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.es_ES).
