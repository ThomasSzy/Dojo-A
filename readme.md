# DOJO - A - Punto 3

![LOGO TINKERCAD](https://i.ibb.co/K08W9N9/Arduino-Tinkercad.jpg)

## INTEGRANTES
* Thomas Szymuda
* Guido Santillan
* Felipe Parache
* Federico Vivas
* Valentin Lloret


## PROYECTO: DOJO A punto 3

![IMAGEN DEL PROYECTO](https://i.ibb.co/P5StJQ8/Captura.jpg)

## DESCRIPCIÓN

El proyecto es un semáforo con 2 lámparas led (de cada color). <br/>
El verde dura 5 segundos. <br/>
El amarillo dura 3 segundos. <br/>
Rojo dura 5 segundos.<br/>
El mismo tiene una funcion para personas no videntes la cual suenda una alerta cuando esta en rojo, amarillo o verde

## FUNCIÓN PRINCIPAL

La función principal se encarga de prender y apagar los leds del semáforo, se utilizando de las funciones encender y apagar, respectivamente. <br/>
Además, mientras el rojo está prendido, suena el piezo durante 5 segundos por una cancion.  <br/>
El amarillo dura 2 segundos con una alerta de doble pitido. <br/>
El verde dura 5 segundos los cuales suena una alerta como el rojo. <br/>
Todos los leds antes de apagarse titilan <br/>
Los leds y el piezo son asignados a través del hashtag define a los pines a los cuales están conectados.

C++ 
void loop()
{
  //PRENDE VERDE ROJO Y TITILA VERDE PARA CAMBIO
  //PRENDE ROJO NUEVAMENTE PARA QUEDAR PARADO
  prender_rojo(LED_ROJO_1,LED_VERDE_2);
  titilar(LED_VERDE_2);
   
  //PRENDE AMARILLO TITILA AMARILLO Y ROJO Y SE CAMBIA SEMAFORO
  prender_amarillo(LED_AMARILLO_2);
  titilar(LED_AMARILLO_2);
  titilar(LED_ROJO_1);
  
  //PRENDE ROJO 2 Y VERDE 1, APAGA ROJO 1 Y PRENDE AMARILL
  prender_rojo(LED_ROJO_2);
  apagar_rojo(LED_ROJO_1);
  //
  prender_amarillo(LED_AMARILLO_1);
  titilar(LED_AMARILLO_1);
  //
  prender_rojo(LED_ROJO_2,LED_VERDE_1);
  titilar(LED_VERDE_1);
  //
  prender_rojo(LED_ROJO_2);
  prender_amarillo(LED_AMARILLO_1);
  titilar(LED_AMARILLO_1);
  apagar_rojo(LED_ROJO_2);
  //
  prender_rojo(LED_ROJO_1);
  prender_amarillo(LED_AMARILLO_2);
  titilar(LED_AMARILLO_2);
  prender_rojo(LED_ROJO_1,LED_VERDE_2);
}


## LINK AL PROYECTO

* [proyecto](https://www.tinkercad.com/things/0osME5HITdC-thomas-szymuda-1d-tercer-nivel/editel)
