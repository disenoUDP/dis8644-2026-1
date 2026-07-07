# examen-grupo-03

## integrantes

+ Antonia Loch - [cuenta-github](https://github.com/bla)
+ Narely Riquelme - [cuenta-github](https://github.com/bla)
+ Ariel Orozco - [cuenta-github](https://github.com/bla)
+ Vanessa García - [cuenta-github](https://github.com/bla)
+ Carla Nuñez - [cuenta-github](https://github.com/bla)


# Vitrina Sónica 
![imagenes](./imagenes/portada.jpg)

Vitrina Sónica es un sintetizador modular construido a partir de la integración de distintos módulos desarrollados de manera colaborativa durante el taller. Cada grupo fue responsable del diseño, fabricación y prueba de una placa específica, en nuestro caso, desarrollamos el módulo oscilador, encargado de generar las señales que constituyen la base sonora del instrumento.

El objetivo del proyecto consistía en comprender la lógica de los sintetizadores modulares, donde cada circuito cumple una función determinada y puede conectarse con otros para crear sistemas sonoros más complejos. A partir de esta metodología, diseñamos un instrumento compuesto por módulos independientes que se comunican mediante conexiones externas, permitiendo experimentar con diferentes configuraciones y comportamientos del sonido.

Inicialmente nuestra propuesta contemplaba integrar un oscilador, un secuenciador y un módulo de salida de audio. Sin embargo, el proceso de desarrollo estuvo marcado por múltiples iteraciones, pruebas y ajustes. Durante el ensamblaje surgieron dificultades relacionadas con la compatibilidad entre algunas placas y con el funcionamiento de ciertos circuitos, lo que nos llevó a replantear la configuración del sistema. Finalmente, optamos por construir un sintetizador conformado por dos módulos osciladores y un mixer, logrando un sistema estable que permitía explorar la mezcla y superposición de señales para obtener distintas texturas sonoras.
La construcción del proyecto estuvo profundamente vinculada al contexto material en el que fue desarrollado. Gran parte de los componentes electrónicos fueron adquiridos en el tradicional barrio San Diego, en Santiago, un lugar reconocido por concentrar tiendas especializadas en electrónica y más. Esta búsqueda y recolección de materiales formó parte del proceso de diseño, ya que las decisiones técnicas estuvieron condicionadas por la disponibilidad real de componentes, obligándonos en varias ocasiones a adaptar el circuito, reemplazar piezas o modificar soluciones para mantener la funcionalidad del sistema.

Del mismo modo, la estructura del sintetizador responde a una decisión tanto funcional como estética. En lugar de ocultar la electrónica, decidimos exhibirla mediante una carcasa construida con malla de acero, acrílico de color y placas PCB visibles, dejando expuestas las conexiones, los cables y los distintos módulos que conforman el instrumento. Esta transparencia permite comprender cómo circulan las señales entre las placas y convierte el funcionamiento interno en parte de la experiencia visual del proyecto.

El nombre Vitrina Sónica nace precisamente de esta intención: transformar el sintetizador en una vitrina donde la electrónica se presenta como protagonista. El sistema invita a observar la relación entre sonido, circuitos y materialidad, haciendo visible el proceso de construcción y el carácter modular del instrumento.

# Placas soldadas

Durante el desarrollo del proyecto fabricamos dos módulos, ambos diseñados para formar parte de un sistema. Cada placa cumple una función específica dentro del sintetizador modular y fue ensamblada mediante soldadura manual de componentes. Antes del montaje definitivo, cada circuito fue probado en protoboard para verificar su funcionamiento y posteriormente fue diseñado en KiCad para fabricar la PCB.

## Comando Estelar 

Comando Estelar es el módulo principal de generación sonora del sintetizador. Esta placa fue diseñada para producir una señal periódica estable que sirve como base para la construcción del sonido dentro del sistema modular.
Su funcionamiento se basa en la combinación de dos circuitos integrados: el CD4046, utilizado como oscilador controlado por voltaje (VCO), y el CD40106, compuesto por inversores Schmitt Trigger que permiten acondicionar y estabilizar la señal generada por el oscilador.
La integración de ambos circuitos entrega un comportamiento estable y permite modificar la frecuencia mediante controles manuales, generando distintas alturas tonales y variaciones sonoras que posteriormente son enviadas al módulo de mezcla.

![imagenes](./imagenes/pcbcomando.png)
![imagenes](./imagenes/esq.comando.png)

---

**¿Cómo funciona?:**

El circuito recibe una alimentación externa de 12 V, la cual pasa primero por un diodo de protección y luego por un regulador 7805, encargado de entregar una tensión constante de 5 V para alimentar los circuitos integrados.

El CD4046 funciona como un oscilador controlado por voltaje. Su frecuencia depende de una red RC formada por resistencias, capacitores y potenciómetros, permitiendo modificar manualmente la velocidad de oscilación.
Posteriormente, la señal es enviada al CD40106, el cual utiliza compuertas Schmitt Trigger para regenerar la onda y producir una señal cuadrada con transiciones más limpias y estables. Este acondicionamiento disminuye el ruido presente en la señal y mejora la calidad del audio obtenido.
Finalmente, la señal es conducida hacia el jack de salida, desde donde puede conectarse a un mixer, amplificador u otros módulos del sintetizador.

**Entrada**
La placa recibe:

+ Alimentación DC de 12 V.
+ Ajustes manuales mediante dos potenciómetros de 100 kΩ.
+ Conexión a tierra común con el resto del sistema.

**Salida**
Entrega una:

+ Onda cuadrada (Square Wave).
+ Señal digital de aproximadamente 5 V.
+ Frecuencia variable controlada por el usuario.
+ Salida mediante jack mono de audio.

Esta señal constituye la fuente sonora principal del sintetizador.

**Rol dentro del sistema:**

Dentro de Vitrina Sónica, Comando Estelar actúa como uno de los módulos encargados de producir el material sonoro base. Gracias a su capacidad de modificar la frecuencia mediante controles físicos, permite obtener diferentes alturas y texturas que posteriormente pueden combinarse con otros módulos del sistema.

## BOM Comando Estelar

| Componente     | Valor  | Cant | PCB         |
| -------------- | ------ | ---- | ----------- |
| Capacitor      | 10nF   | 1    | C1          |
| Capacitor      | 100nF  | 1    | C5          |
| C. polarizado  | 100µF  | 3    | C2 C6 C7    |
| C. polarizado  | 10µF   | 2    | C3 C4       |
| Diodo          | 1N4007 | 1    | D1          |
| LED            | ------ | 1    | D2          |
| Resistencia    | 100KΩ  | 1    | R1          |
| Resistencia    | 1KΩ    | 1    | R2          |
| LDR            | ------ | 2    | RV1 RV2     |
| Switch         | SPDT   | 1    | SW1         |
| Chip           | 4046   | 1    | U1          |
| Chip           | L7805  | 1    | U2          |
| Chip           | 40106  | 1    | U3          |
| Base Dip       | 16 pin | 1    | U1          |
| Base Dip       | 14 pin | 1    | U3          |
| Perno M3       |        | 4    | H1 H2 H3 H4 |
| Conector       | Barrel | 2    | J2 J3       |
| Conector       | Jack   | 1    | J1          |


## Resonancia 

Resonancia corresponde al segundo módulo generador del sintetizador. Aunque comparte la misma arquitectura base del primer oscilador, incorpora un CD4017, contador decimal que introduce un comportamiento secuencial dentro del circuito.
Este módulo no solo genera una señal sonora, sino que además agrega variaciones rítmicas y cambios periódicos, permitiendo enriquecer la composición del sintetizador mediante la interacción entre el oscilador y la lógica secuencial.

![imagenes](./imagenes/pbcresonancia.png)
![imagenes](./imagenes/esq.resonancia.png)

---

**¿Cómo funciona?**

Al igual que la primera placa, la alimentación de 12 V es regulada mediante un 7805, obteniendo una tensión estable de 5 V.

El CD4046 genera la frecuencia principal del sistema. Posteriormente, la señal es acondicionada mediante el CD40106, obteniendo una onda cuadrada limpia y estable.
La principal diferencia de este módulo es la incorporación del CD4017, un contador Johnson que utiliza la señal del oscilador como reloj (Clock). Cada pulso recibido hace avanzar el contador hacia una salida distinta, permitiendo crear secuencias temporales y modificaciones periódicas del comportamiento del circuito.
Este mecanismo introduce una dimensión rítmica dentro del sintetizador, haciendo que la señal evolucione de manera automática en lugar de mantenerse constante.

**Entrada**
La placa recibe:

+ Alimentación DC de 12 V.
+ Señal de reloj generada por el oscilador.
+ Ajustes mediante potenciómetros.
+ Tierra común con el resto de los módulos.

**Salida**
Entrega:

+ Onda cuadrada.
+ Señales secuenciales controladas por el CD4017.
+ Variaciones periódicas de frecuencia.
+ Señal de audio mediante jack.

**Rol dentro del sistema:**

Resonancia complementa el funcionamiento de Comando Estelar incorporando una lógica de secuenciación. En lugar de producir únicamente un tono continuo, añade cambios temporales que enriquecen el comportamiento del sintetizador y permiten obtener una mayor diversidad de sonidos al combinar ambos módulos dentro del mixer.

## BOM Resonancia 

| Componente     | Valor  | Cant | PCB         |
| -------------- | ------ | ---- | ----------- |
| Capacitor      | 1µF    | 2    | C2 C7       |
| C. polarizado  | 4µF    | 1    | C3          |
| C. polarizado  | 100µF  | 1    | C4          |
| C. polarizado  | 10µF   | 2    | C5 C8       |
| Capacitor      | 100nF  | 1    | C6          |
| Led            | -----  | 2    | D1 D3       |
| Diodo          | 1N4007 | 1    | D2          |
| Resistencia    | 470KΩ  | 2    | R1 R2       |
| Resistencia    | 330KΩ  | 1    | R3          |
| Resistencia    | 1KΩ    | 1    | R4          |
| LDR            | ------ | 2    | RV1 RV2     |
| Switch         | SPDT   | 1    | SW1         |
| Chip           | 4017   | 1    | U1          |
| Chip           | 4046   | 1    | U2          |
| Chip           | 40106  | 1    | U3          |
| Chip           | L7805  | 1    | U4          |
| Base Dip       | 16 pin | 2    | U1 U2       |
| Base Dip       | 14 pin | 1    | U3          |
| Perno M3       |        | 4    | H1 H2 H3 H4 |
| Conector       | Barrel | 2    | J1 J3       |
| Conector       | Jack   | 1    | J4          |

## Proceso 

En el proceso de ensamblaje de las placas surgieron diversas dificultades. El cable utilizado para las conexiones se desoldaba con facilidad al manipular los módulos, por lo que fue reemplazado por un cable de mayor grosor, reduciendo considerablemente este problema. Durante las pruebas también identificamos errores de soldadura que nos permitieron mejorar la precisión del montaje.
Al finalizar la placa Comando Estelar, realizamos las primeras pruebas y detectamos que no encendía. Mediante el uso del multímetro descubrimos que las polaridades del barrel jack estaban invertidas. Tras corregir ese error, encontramos además soldaduras que se encontraban en contacto entre sí, generando interferencias en las señales del circuito. Como el problema persistía, reemplazamos los circuitos integrados CD4046, CD40106 y el regulador L7805, comprobando que algunos componentes no estaban recibiendo correctamente la alimentación. Después de estos cambios, la placa comenzó a funcionar correctamente. La experiencia adquirida permitió ensamblar las siguientes placas de manera mucho más rápida y precisa.

La placa Relo funcionó correctamente de forma independiente; sin embargo, no fue posible establecer una comunicación funcional con las demás placas, ya que únicamente compartían alimentación, sin lograr una interacción entre sus señales. Finalmente, la placa Parla no alcanzó un funcionamiento estable, por lo que fue descartada como parte del sintetizador final.

![imagenes](./imagenes/procesos-1.png)
![imagenes](./imagenes/procesos-2.png)


## Carcasa

![imagenes](./imagenes/carcasa.png)

La carcasa surge de la decisión de entender la electrónica como parte fundamental del lenguaje del objeto, en lugar de ocultarla bajo un contenedor. Mientras muchos productos tecnológicos esconden sus circuitos detrás de superficies limpias y cerradas, nuestra propuesta busca invertir esa lógica: hacer visibles los componentes, las conexiones y los procesos de fabricación para que el funcionamiento del sintetizador también pueda ser observado.

La estructura fue concebida como un sistema abierto que permite leer visualmente el recorrido de la señal entre los distintos módulos. Cada cable, circuito y punto de conexión permanece expuesto, permitiendo comprender la naturaleza modular del instrumento y evidenciando la relación entre cada placa electrónica.
La elección de materiales responde tanto a criterios funcionales como conceptuales. El alambre de acero constituye el esqueleto principal del sistema, conformando una estructura ligera pero resistente que sostiene todos los módulos sin bloquear su visibilidad. Su construcción manual mantiene una apariencia cercana al boceto tridimensional, haciendo visible el proceso de fabricación y reforzando el carácter experimental del proyecto.

La malla metálica aporta estabilidad estructural y funciona como un plano de soporte donde pueden fijarse las placas mediante amarras plásticas. Al mismo tiempo, genera transparencias que permiten observar el interior del objeto desde múltiples ángulos, produciendo distintas lecturas visuales dependiendo de la posición del espectador.
El acrílico de color fue utilizado como soporte para los módulos electrónicos, los potenciómetros y los conectores de audio. Además de aportar rigidez al montaje, permite diferenciar visualmente cada módulo del sintetizador, facilitando la identificación de sus funciones y organizando la composición general del sistema.

Las placas PCB, lejos de permanecer ocultas, se convierten en uno de los principales elementos visuales del proyecto. Sus pistas de cobre, componentes soldados y conexiones forman parte de la composición estética del instrumento, haciendo visible el trabajo de diseño electrónico y el proceso de fabricación desarrollado durante el taller.
En conjunto, estos materiales construyen una carcasa que no busca disimular la tecnología, sino transformarla en el principal recurso expresivo del proyecto. La estructura deja de ser un simple contenedor para convertirse en una interfaz que comunica cómo el sintetizador está construido, cómo funciona y cómo los distintos módulos interactúan entre sí.

## composición

Como parte del proceso de exploración sonora del proyecto, desarrollamos dos partituras gráficas inspiradas en los sonidos generados por nuestros módulos electrónicos. Más que representar las señales de manera convencional, buscamos traducir la experiencia de escucharlas a un lenguaje visual propio, entendiendo la partitura como una herramienta de interpretación y no como un sistema de notación musical tradicional.

El proceso consistió en reunirnos con papel y lápiz mientras el sintetizador permanecía en funcionamiento. Escuchamos atentamente las variaciones de frecuencia, las repeticiones, las pausas y los cambios de ritmo que producían las placas, registrando de manera espontánea las formas, recorridos y patrones que cada sonido evocaba. No existieron reglas previas ni una intención de representar fielmente la estructura musical; el objetivo fue transformar la percepción auditiva en una composición gráfica construida desde la intuición y la observación colectiva.

## Partitura Comando Estelar 

La partitura propone un lenguaje más gestual y dinámico. A través de líneas continuas, curvas, oscilaciones y variaciones en el grosor del trazo, representa los cambios de frecuencia, las pausas y el movimiento percibido durante la escucha, enfatizando el carácter variable e impredecible del comportamiento sonoro de las placas.
Más que documentar el funcionamiento técnico del sistema, estas partituras constituyen una interpretación sensible del instrumento y de la experiencia de interactuar con él. Son el resultado de un proceso colaborativo en el que cada integrante aportó su propia percepción, convirtiendo señales electrónicas en composiciones visuales que evidencian la estrecha relación entre sonido, dibujo y experimentación.

![imagenes](./imagenes/comandoestelar.jpeg)

## Referentes 

![imagenes](./imagenes/partituras.png) 

> Gerhard Rühm: escritor, compositor y artista visual austriaco.


> George Crumb: compositor estadounidense de música vanguardista.

## Registro audiovisual 

<https://youtu.be/Xt1jPtpacEU>
<https://youtu.be/X4vuv-FdAHY>
<https://youtube.com/shorts/Ci4jNXiDuag?feature=share>​

## bibliografía

+ Crumb, G. (1973). Makrokosmos: Vol. II. Twelve piece-pieces after the Zodiac for amplified piano [Partitura]. C. F. Peters Corporation.
+ Rühm, G. (s.f.). Da hilft kein Winken [Poema visual manuscrito].steirischerherbst Retrospective  VISUELLE POESIE VISUELLE MUSIK - steirischer herbst Archiv
+ Crumb, G. (1972). Spiral Galaxy 

