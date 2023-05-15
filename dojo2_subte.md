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
