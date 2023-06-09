# DOJO - A - Punto 3

![LOGO TINKERCAD](https://i.ibb.co/K08W9N9/Arduino-Tinkercad.jpg)

## INTEGRANTES
* Thomas Szymuda
* Guido Santillan
* Felipe Parache
* Federico Vivas
* Valentin Lloret


## PROYECTO: DOJO A punto 3

![IMAGEN DEL PROYECTO](https://i.im.ge/2023/05/21/hrXklq.Thomas-Szymuda-Primer-Parcial-1D.png)

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
  
  prender_rojo(LED_ROJO_1,LED_VERDE_2);
  titilar(LED_VERDE_2);
  
  prender_amarillo(LED_AMARILLO_2);
  titilar(LED_AMARILLO_2);
  titilar(LED_ROJO_1);
  
  
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



# DOJO - A - Punto 1 Subtes

![LOGO TINKERCAD](https://i.ibb.co/K08W9N9/Arduino-Tinkercad.jpg)

## INTEGRANTES
* Thomas Szymuda
* Guido Santillan
* Felipe Parache
* Federico Vivas
* Valentin Lloret


## PROYECTO: DOJO 2-A Punto 1 Subte

![IMAGEN DEL PROYECTO](https://i.im.ge/2023/05/15/URzxLY.Copy-of-Dojo-2-Thomas-Szymuda-1-D.png)

## DESCRIPCIÓN

El proyecto son varias estaciones de subte de las cuales un contador te va diciendo cuantas paradas quedan. <br/>
cada estacion para por 2 segundos<br/>
el total de estaciones son 4 <br/>

## FUNCIÓN PRINCIPAL

La función principal se encarga de prender un led en cada estacion en la que se encuentra y un contador diciendote cuantas estaciones quedan <br/>
Además, cuenta con un tiempo para poder bajar y poder subir <br/>

// Thomas Szymuda 1d 

void setup()
{
  //Leds;
  pinMode(LED_A, OUTPUT);
  pinMode(LED_B, OUTPUT);
  pinMode(LED_C, OUTPUT);
  pinMode(LED_D, OUTPUT);
  //CONTADOR
  pinMode(CON_G, OUTPUT);
  pinMode(CON_F, OUTPUT);
  pinMode(CON_A, OUTPUT);
  pinMode(CON_B, OUTPUT);
  pinMode(CON_C, OUTPUT);
  pinMode(CON_D, OUTPUT);
  pinMode(CON_E, OUTPUT);
  //Boton y serial
  pinMode(PULLOUT, INPUT);
  Serial.begin(9600);
}
void loop()
{
  prender_boton();
}


## LINK AL PROYECTO

* [proyecto](https://www.tinkercad.com/things/4DkkYQOdkuS-dojo-2-thomas-szymuda-1-d/editel?sharecode=aKnm-HJeyGQvlsoUp8ZKVgUxotN3fnz57JO7Rfc_YFg)



# DOJO - A - Punto 2 Subtes

![LOGO TINKERCAD](https://i.ibb.co/K08W9N9/Arduino-Tinkercad.jpg)

## INTEGRANTES
* Thomas Szymuda
* Guido Santillan
* Felipe Parache
* Federico Vivas
* Valentin Lloret


## PROYECTO: DOJO 2-A Punto 1 Subte

![IMAGEN DEL PROYECTO](https://i.im.ge/2023/05/15/URpJrG.Copy-of-Dojo-2-Thomas-Szymuda-1-D-1.png)

## DESCRIPCIÓN

El proyecto son varias estaciones de subte de las cuales un contador te va diciendo cuantas paradas quedan. avisando con un pitido para los no videntes <br/>
cada estacion para por 2 segundos<br/>
el total de estaciones son 4 <br/>

## FUNCIÓN PRINCIPAL

La función principal se encarga de prender un led en cada estacion en la que se encuentra y un contador diciendote cuantas estaciones quedan y su pitido para no videntes <br/>
Además, cuenta con un tiempo para poder bajar y poder subir <br/>

// Thomas Szymuda 1d 

void setup()
{
  //Leds;
  pinMode(LED_A, OUTPUT);
  pinMode(LED_B, OUTPUT);
  pinMode(LED_C, OUTPUT);
  pinMode(LED_D, OUTPUT);
  //CONTADOR
  pinMode(CON_G, OUTPUT);
  pinMode(CON_F, OUTPUT);
  pinMode(CON_A, OUTPUT);
  pinMode(CON_B, OUTPUT);
  pinMode(CON_C, OUTPUT);
  pinMode(CON_D, OUTPUT);
  pinMode(CON_E, OUTPUT);
  //Boton y serial
  pinMode(PULLOUT, INPUT);
  Serial.begin(9600);
  //Sonido No Videntes
  pinMode(sonido,OUTPUT);
}
void loop()
{
  prender_boton();
}

void prender_boton()
{
  prendido = digitalRead(PULLOUT);
  Serial.println(prendido);
  if(prendido == HIGH)
  {
      digitalWrite(LED_A, HIGH);
  //Contador estaciones
 	constitucion();
    sanjuan();
    independecia();
    moreno();
    
  } 
}

## LINK AL PROYECTO

* [proyecto](https://www.tinkercad.com/things/lfnRfQ6Yzo9-copy-of-dojo-2-thomas-szymuda-1-d/editel?sharecode=JvDMH-kYhNaWCDRwGjTnhi0qodbjYEzgdEq2j1wTOLo)

