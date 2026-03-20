# sesion-02a

## Clase 170326

### pre-clase (teloneo Aaron)

Referentes entregados

1. Kraftwerk
2. LCD Soundsystem
3. Pierre Shaeffer: Tratado de los objetos musicales (1966)
4. Hainboch
5. Oficina de la nada (Felipe Cussen)

Fabricar androides es la música electrónica.

El sonido comienza y decae. 

### clase

- Primera parte: Aaron 

Primero observamos y analizamos cada elemento que se nos otorgó en cada caja

**Potenciómetro:** Existen los A y B. Los B son económicos, en cambio los A son caros y se utilizan en audio. 

Existen dos tipos de cables dupont: Dupont dupont y dupont caimán.

**CHIP IC:** Se colocan sobre el surco de la podroboard. Contienen un circuito interno. Nos ayuda a realizar secuencias con ritmo. Esta pieza en las “patitas” externas tienen un surco el cual nos ayuda a saber dónde comienza.

Se crearon primero las luces verdes y en la actualidad recién podemos ver luces azules ya que son más difíciles de realizar. 

Los parlantes de bajo son mucho más grandes ya que el oído humano es más susceptible a ello, en cambio los agudos no y cada vez los escuchas menos. 

- Segunda parte: Misaa

**Resistencia electrónica:** están realizadas con carbón por su alta cantidad de OHM

El cobre tiene 0,075 Ω de resistencia, le cuesta más que al oro pasar los electrones y el oro tiene 0,022 Ω de resistencia.

La resistencia debe estar conectado a 2 lugares distintos de la protoboard

No existe ningún material que no tenga resistencia. Los científicos han realizado experimentos para bajar la resistencia, pero están adulterando los elementos. 

Las resistencias tienen un codigo de color ya que a traves de este metodo podemos saber cuanta resistenbcia tiene. Nosotros en nuestro caso tenemos de 220 Ω y 1k

1. Los dos primeros colores son digitos (estos entregados a partir de una tabla que contiene estos datos) 
2.  La tercera barrita son la cantidad de 0 que tiene
3.  El color dorado es el margen de error o tolerancia.

![tabla](imagenes/tabla_de_resistencia.jpg)
![tabla](imagenes/resistencia_colores.jpeg)

Calculadora de resistencia https://www.digikey.com/es/resources/conversion-calculators/conversion-calculator-resistor-color-code 

**Electrodos:** aplicación para teléfono

**Esquemático:** Representan de manera gráfica y abstracta el circuito

![esquematico](imagenes/ejemplo_esquematico.jpeg)

**Circuito paralelo:** son independientes

**Circuito:** Lazo cerrado con elementos resistivos Fluye la electricidad mediante elementos

**VCC:** voltaje de corriente cotidiana

**GND:** ground, 0V, tierra, voltaje negativo

Read me es un archivo, no una carpeta

Mucho de las cosas que hacemos es por sentir algo (aaron)

### imagenes de proceso
![cajas](imagenes/cajas.jpeg)
![materiales](imagenes/materiales.jpeg)
![ejercicio](imagenes/ejercicio.jpeg)
![dibujo](imagenes/circuito_dibujo.jpeg).

### post-clase

1. Cada resistencia debe existir un cable
2. La resistencia debe ir en la misma línea que el cable y el lado positivo del led en vertical
3. Todo debe ir en la misma linea
4. Coloque otro circuito, pero de manera equivocada y la luz del primer circuito fallaba

- Analisis artistas

LCD Soundsystem.


Cuando comenzamos a escucharlos en clases quedé impresionada con ellos, escuché con mucha atención todo, al principio pensé que eran británicos, pero no. Tienen un poco de esa impronta de la música británica de los 80 que me gusta. Me recuerdo a varias cosas, por ejemplo la música que se ocupa en la serie Heartstopper que me encanta, cuando llegue a mi casa a escucharlos, me recordó a una pieza que tuve la oportunidad de escuchar en vivo que se llama “Short Ride in a Fast Machine” la cual cada instrumento de la orquesta es un sonido distinto. Cada que avanza, se van incorporando y generando nuevos sonidos y al album de Phil Collins “face Value” con su canción “ In the Air Tonight”

Entonces comencé a pensar: ¿qué los hace parecidos y porque me gustan tanto? respondiendo así la pregunta que me llama la atención. Me encanta la recepción de sonidos y con ellos la creación de nuevos. Me gusta escucharlos en momentos en donde necesito mayor relajación, algo que sea constante al igual que mi concentración.

Elegí el álbum “american dream” (loco igual, ya que la pieza que mencioné anteriormente fue del programa “americano en parís”) ya que contiene mi canción favorita “oh baby”. Este álbum los reúne tras 5 años de separación. Este se tomó una cantidad de 18 meses aproximadamente de su grabación teniendo que cancelar fechas en Asia para poder completarlo. Musicalmente, American Dream ha sido descrito como dance-punk, new wave , post-punk, synth-pop, art rock y dance-rock (esto explica porque me gusta mucho este álbum). Los críticos señalaron que el álbum era similar a la trilogía berlinesa de David Bowie (al igual que esto).

Al igual que las críticas, no es de mi interés y gusto su portada (me gusta hablar de esto ya que yo me dedico a realizar este trabajo)

- Ejercicios

En clases, junto a mi compañera Paula realizamos el ejercicio número 1, pero quedamos con dudas a pesar de que nos prendieron las luces. (después me di cuenta que confundimos algunas residencias) 

Después de eso, yo intente hacer por mi parte los circuitos vistos en clases y ninguno me funciono lo cual me frustro y sentía que ya pasar al siguiente nivel no me iba a funcionar, tampoco queria ver videos en youtube porque queria tener un poco de razonamiento descifrando lo que se nos entregó. 

Ejercicio 1

Como mencione, a pesar de haberlo realizado, me costó entenderlo nuevamente
1. Si quiero que la luz se encienda debo procurar que ambos lados (+ y -) estén conectados en el lugar que corresponde ósea ++ y - -
2. La resistencia limita la corriente para no quemar el led
3. Todo debe ir como se presenta el el esquemático, por ejemplo si a D1 le sigue una resistencia de 1k colocarla después de ello
4. El nodo es un punto donde se conectan 2 o más componentes en el circuito

| loquitoportilocoloco  | D1    | D2    | D3    | D4    |
| ---                   | ---   | ---   | ---   | ---   |
| R1                    |    0  |    0  |     0 |     0 |
| R3                    |    1  |    1  |     1 |     0 |
| R4                    |    1  |    1  |     1 |     0 |
| R2                    |    0  |    0  |     0 |     1 |
| R5                    |    0  |   0   |     0 |     1 |             

| resistencias  | posiciones   |
| ---           | ---          | 
| R1            |    I2,I5     |   
| R2            |    I6,I11    |   
| R3            |    C5,C9     |    
| R4            |    G5,D5     |  
| R5            |    G12,G14   | 

![ejercicio 1](imagenes/ejercicio1_c.jpeg) 

Ejercicio 2

1. Primero realice el circuito central y funciono solo.
2. La gracia de este ejercicio es que las resistencias vayan una tras la otra
3. Después no se que paso que no prendian las luces al conectarlo todo (se me quemaron 2)
4. Es tan sensible que con solo posicionar las resistencias por encima de donde deben ir se encienden los LED

| loquitoportilocoloco | D1 | D2 | D3 |
| -------------------- | -- | -- | -- |
| R1                   |  1 |  0 |  0 |
| R2                   |  1 |  0 |  0 |
| R3                   |  1 |  0 |  0 |
| R4                   |  1 |  0 |  0 |
| R5                   |  0 |  1 |  1 |
| R6                   |  1 |  1 |  0 |
| R7                   |  1 |  1 |  0 |
| R8                   |  1 |  1 |  0 |

| resistencias  | posiciones   |
| ---           | ---          | 
| R1            |    I14,I16   |   
| R2            |    I16,I18   |    
| R3            |    I18,I20   |    
| R4            |    I20,I24   |  
| R5            |    I11,14    |
| R6            |    I22,I26   |    
| R7            |    I26,I28   |  
| R8            |    G29,E29   | 

![ejercicio 2](imagenes/ejercicio_2.jpg)



