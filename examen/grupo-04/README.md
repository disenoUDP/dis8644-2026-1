# examen-grupo-04

## Integrantes

- Antonella Kiara Aguilar Plate / [@antokiaraa](https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/01-antokiaraa)
- Santiago Cifuentes Vélez / [@santiagocifuvelez](https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/08-santiagocifuvelez)
- Paula Fuentes Mena / [@paulafuentesm](https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/12-paulafuentesm)
- Kristel Ladrón de Guevara Jara / [@kristelagj](https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/16-kristelagj)
- Catalina Antonia Oyanedel Sánchez / [@catalinaoyanedel-01](https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/22-catalinaoyanedel-01)
- Yaira Alexandra Ruiz Ossandón / [@yairaruiz](https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/28-yairaruiz)

## Criterios de diseño del sistema 

La inspiración para nuestro proyecto comienza desde el sonido que se produce a partir de uno de nuestros osciladores, el cual era parecido al del chirihue, ave nativa chilena. Además, como antecedente, integrantes de nuestro equipo en la entrega del primer proyecto realizaron un sintetizador que lleva como título “Naturalezas Interconectadas”, proponiendo que distintos tipos de naturalezas interactúan las unas con las otras, teniendo así un comienzo para nuestra investigación.

[Video Chirihue](https://www.youtube.com/shorts/mDQom4hty6A)

![naturalezas interconectadas](./imagenes/naturalezas.png)
_Naturalezas Interconectadas_

A partir de esto, nuestra conceptualización surge en base a las teorías de Donna Haraway. La autora propone el concepto de cyborg, planteando la interconexión entre diversos componentes y entornos —incluso componentes artificiales y tecnológicos—, como relaciones extensivas en el constructo de lo vivo.¹ En sus palabras, “un cyborg es un organismo cibernético, un híbrido de máquina y organismo, una criatura de realidad social y también de ficción.” ² 

Desde estas definiciones, entendemos que los componentes artificiales y tecnológicos pueden ser una parte más del cuerpo, una extensión del organismo y de lo vivo, desafiando los límites establecidos y volviéndolos más difusos.  Así, a través del concepto de unión, utilizamos diversos elementos: 

![elementos](./imagenes/elementos.png)

Finalmente, el concepto que engloba toda nuestra investigación es la **simpoiesis.** Este sostiene que ningún ser, sistema o creación se produce o se sostiene a sí mismo en solitario, sino mediante redes de colaboración mutua, por esto planteamos que nada trabaja de manera solitaria, todos los elementos tienen una relación y se retroalimentan mutuamente.

_“En el centro de este mundo que se deshilacha, la interdependencia permanece. Lo vivo y lo no vivo están tejidos en una trama que se modifica a cada instante.” Jorgelina Sannazzaro³_

## Contexto desde Chile, desde nuestra disponibilidad material

La historia de la música electroacústica en Chile se remonta a la década de 1950, dividiéndose en diversas etapas. Según Federico Schumacher, para llegar a consolidarse, la aparición del computador como una herramienta esencial en la composición electroacústica  facilitó enormemente esta nueva situación.⁴ 

Tenemos el computador como un principal antecedente en la música electroacústica generada en Chile, lo que nos permite tener como referencia a un gran exponente, José Vicente Asuar, músico e ingeniero, quien realizó _Comdasuar_ en 1977-78, un computador que funcionaba como herramienta compositiva e instrumental en tiempo real. Incluía editor de partitura y secuenciador, una herramienta de composición algorítmica, un programa de síntesis de sonido digital, una unidad analógica de proceso y enriquecimiento de la señal.

El desarrollo y la evolución de este mundo llevó a pasar de los generadores analógicos de onda y grabadores al computador, reemplazando a la gran mayoría de los antiguos equipos, si no a todos. 

A pesar de eso, en el contexto de este taller partimos desde la base de la historia, sin utilizar computadores, sino circuitos analógicos para producir nuestros propios sintetizadores. En ¿Qué es la música electrónica? de Gustavo Becerra (otro importante exponente) escrito en 1957, él responde ante las dudas de este nuevo fenómeno: quienes tocan este tipo de música pueden considerarse ejecutantes, pero éstos no tocan ningún instrumento tradicional en el cumplimiento de sus funciones. Operan osciladores de audiofrecuencia y equipos grabadores de cinta magnética.⁵ 

Por lo tanto, para encontrar los componentes para generar nuestros propios circuitos nos adentramos principalmente en la calle San Diego, que cuenta con una gran variedad de tiendas y disponibilidad de componentes electrónicos, siendo algunas de ellas Victronics, Orfali y Electrónica Ibarra.
_________________________________________________________________________

# Naturalezas Interconectadas: Pieza Final
## Placas soldadas

- **Piezo:** Maincra
- **Oscilador:** Chirihue mecanizado
- **Parlante:** Parla

### Principio de funcionamiento de cada una

**Maincra:**

El piezo es un componente que convierte la presión o vibración mecánica en señales eléctricas que luego alimentarán y afectarán el circuito complementario (las demás placas). En nuestro caso, lo conectamos a una viola para generar las vibraciones que luego convertirá. Este módulo nos permite transformar un sonido, convirtiéndolo en una señal que avanzará en nuestro oscilador.

**Chirihue Mecanizado:**

Su función es generar la forma de la onda que luego se convierte en sonido. Se caracteriza por repetir sonidos extremadamente cortos y agudos de manera continua, variando en la tonalidad y en el ritmo. 

**Parla:**

Convierte señales eléctricas en ondas de sonido enviadas desde el chirihue. Su función principal es transformar la información de audio proveniente de un dispositivo.

### Qué tipo de señal entrega a la salida, qué recibe

| Módulo | ¿Qué recibe? | ¿Qué entrega? |
| :--- | :--- | :--- |
| **Maincra (Piezo)** | Vibraciones mecánicas provenientes de la viola. Instrumento tocado por Kriss. | Una **señal eléctrica analógica** (resultado de tocar la viola) de bajo voltaje que representa esas vibraciones. Esta señal nos dará "la vida" para que el synthe funcione. |
| **Chirihue mecanizado (Oscilador)** | La señal eléctrica proveniente del piezo (o la alimentación, dependiendo de cómo esté conectado el circuito). | Una **señal eléctrica oscilante** (onda cuadrada que se transforma a medida que movemos los potenciómetros) que genera el sonido característico del sintetizador, es decir, el sonido del chirihue. |
| **Parla (Parlante)** | La señal eléctrica del oscilador. | **Ondas sonoras**, es decir, el sonido que finalmente escucha el espectador. |

**Maincra:**
Recibe las vibraciones mecánicas generadas por la viola y las transforma en una señal eléctrica analógica que alimenta el resto del sistema.

**Chirihue mecanizado:**
Recibe la señal eléctrica proveniente del piezo y la procesa para generar una señal eléctrica oscilante, produciendo el sonido característico del sintetizador, el cual es el canto del chirihue.

**Parla:**
Recibe la señal eléctrica enviada por el oscilador y la convierte en ondas sonoras, permitiendo escuchar el resultado de la interacción entre todos los módulos, que sería la melodía final.

## Lista de materiales y costos:

### BOM Maincra

| Componente | Cantidad | Valor unitario | Link |
| :--- | :---: | :---: | :--- |
| Chip NE555P | 1 | $490 | [victronics.cl](https://www.victronics.cl/circuitos-integrados/lm555cngeneralpurposebipolartimerdip8/) |
| Chip TL072CP | 1 | $990 | [victronics.cl](https://www.victronics.cl/circuitos-integrados/tl072cpdualjfetlowpoweropamplifierdip8/) |
| Regulador L7805CV | 1 | $350 | [victronics.cl](https://www.victronics.cl/reguladores/reguladorvoltl7805cv5v-15ato220/) |
| Diodo 1N4007 | 1 | $200 | [mechatronicstore.cl](https://www.mechatronicstore.cl/diodo-rectificador-in4007-1n4007-4007/) |
| Diodo 1N5819 | 2 | $586 | [cl.rsdelivers.com](https://cl.rsdelivers.com/product/nexperia/bat85113/nexperia-diodo-bat85113-diodo-schottky-200-ma-30-v/0300978) |
| Transistor 2N2222 | 1 | $200 | [mechatronicstore.cl](https://www.mechatronicstore.cl/transistor-2n2222/) |
| Potenciómetro B10K | 1 | $495 | [altronics.cl](https://altronics.cl/potenciometro-lineal-10k-b10k) |
| Potenciómetro B500K | 1 | $495 | [altronics.cl](https://altronics.cl/potenciometro-lineal-500k-b500k?search=b500k) |
| LED 3mm | 3 | $100 | [mechatronicstore.cl](https://www.mechatronicstore.cl/led-3mm-5mm/) |
| Resistencia 47 Ω | 1 | $90 | [electroardu.cl](https://www.electroardu.cl/resistencias-1-k-ohm?srsltid=AfmBOor81HKrzfoOTnLK3FU6ObPuf1EPUVMS0naCwqMNIzGt8LYDiUYt) |
| Resistencia 100 Ω | 1 | $90 | [electroardu.cl](https://www.electroardu.cl/resistencias-1-k-ohm?srsltid=AfmBOor81HKrzfoOTnLK3FU6ObPuf1EPUVMS0naCwqMNIzGt8LYDiUYt) |
| Resistencia 220 Ω | 1 | $90 | [electroardu.cl](https://www.electroardu.cl/resistencias-1-k-ohm?srsltid=AfmBOor81HKrzfoOTnLK3FU6ObPuf1EPUVMS0naCwqMNIzGt8LYDiUYt) |
| Resistencia 1 KΩ | 6 | $90 | [electroardu.cl](https://www.electroardu.cl/resistencias-1-k-ohm?srsltid=AfmBOor81HKrzfoOTnLK3FU6ObPuf1EPUVMS0naCwqMNIzGt8LYDiUYt) |
| Resistencia 2,2 KΩ | 1 | $90 | [electroardu.cl](https://www.electroardu.cl/resistencias-1-k-ohm?srsltid=AfmBOor81HKrzfoOTnLK3FU6ObPuf1EPUVMS0naCwqMNIzGt8LYDiUYt) |
| Resistencia 10 KΩ | 2 | $90 | [electroardu.cl](https://www.electroardu.cl/resistencias-1-k-ohm?srsltid=AfmBOor81HKrzfoOTnLK3FU6ObPuf1EPUVMS0naCwqMNIzGt8LYDiUYt) |
| Resistencia 100 KΩ | 3 | $90 | [electroardu.cl](https://www.electroardu.cl/resistencias-1-k-ohm?srsltid=AfmBOor81HKrzfoOTnLK3FU6ObPuf1EPUVMS0naCwqMNIzGt8LYDiUYt) |
| Resistencia 2,2 MΩ | 1 | $90 | [electroardu.cl](https://www.electroardu.cl/resistencias-1-k-ohm?srsltid=AfmBOor81HKrzfoOTnLK3FU6ObPuf1EPUVMS0naCwqMNIzGt8LYDiUYt) |
| Condensador cerámico 1 µF | 1 | $100 | [mechatronicstore.cl](https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/) |
| Condensador cerámico 4.7 nF | 1 | $100 | [mechatronicstore.cl](https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/) |
| Condensador cerámico 10 nF | 1 | $100 | [mechatronicstore.cl](https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/) |
| Condensador cerámico 100 nF | 3 | $100 | [mechatronicstore.cl](https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/) |
| Condensador polarizado 10 µF | 2 | $100 | [mechatronicstore.cl](https://www.mechatronicstore.cl/condensador-capacitorio-de-electrolitico-por-unidad-varios-valores/) |
| Condensador polarizado 100 µF | 3 | $100 | [mechatronicstore.cl](https://www.mechatronicstore.cl/condensador-capacitorio-de-electrolitico-por-unidad-varios-valores/) |
| Piezo | 1 | $990 | [mechatronicstore.cl](https://www.mechatronicstore.cl/sensor-piezoelectrico-27mm-con-cable/) |
| Cables dupont 40 uni. | 1 | $2.990 | [mcielectronics.cl](https://mcielectronics.cl/shop/product/cable-dupont-macho-macho-20cm-pack-40-unidades-2/) |
| Batería 9V recargable | 1 | $7.990 | [sodimac.cl](https://www.sodimac.cl/sodimac-cl/articulo/110251085/bateria-recargable-9v/110251089) |
| Interruptor Switch | 1 | $570 | [katode.cl](https://www.katode.cl/switches/1339-interruptor-switch-2-pines-on-off-corto.html?srsltid=AfmBOorJIleUySzAORFwXSattHKE4BKH2LmhhXZS_8fZ4MW-G6kwnxqA) |

### Bom Chirihue Mecanizado

| Componente | Cantidad | Valor unitario | Link |
| :--- | :---: | :---: | :--- |
| Chip 40106 | 1 | $1.200 | [electronicareal.cl](https://electronicareal.cl/producto/integrado-digital-cd-40106/?srsltid=AfmBOopGygR12K2_-zL_pf-RaOB5PvLmK7oy2TURaqkeA0zU1alOhJD-) |
| Chip LM324 | 1 | $590 | [mechatronicstore.cl](https://www.mechatronicstore.cl/amplificador-operacional-lm324/) |
| Condensador 10 µF | 3 | $330 | [victronics.cl](https://www.victronics.cl/condensadores/condensadorelectrolitico10uf50v/) |
| Condensador 100 nF | 2 | $100 | [mechatronicstore.cl](https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/) |
| Condensador 100 µF | 1 | $380 | [victronics.cl](https://www.victronics.cl/condensadores/cond-electrolitico-100uf-25v20105oc-6x12-p2-5mm-10u/) |
| Diodo 1N4148 | 4 | $100 | [mechatronicstore.cl](https://www.mechatronicstore.cl/diodo-rectificador-de-alta-frecuencia-1n4148-do35/) |
| Diodo 1N4007 | 1 | $200 | [mechatronicstore.cl](https://www.mechatronicstore.cl/diodo-rectificador-in4007-1n4007-4007/) |
| Resistencia 1 kΩ | 6 | $100 | [mechatronicstore.cl](https://www.mechatronicstore.cl/resistencia/) |
| Conector DC | 1 | $239 | AliExpress |
| Conector de audio | 1 | $51 | AliExpress |
| Conector de alimentación | 1 | $148 | AliExpress |

### Tiempo de trabajo y soldadura: 
Este proceso de soldadura, lo comenzamos el 16 de junio del 2026, a las 9:00 am durante la clase, la cual dura 4 horas, y así fueron nuestros días de reunión y el tiempo dedicado en ellos a soldar: 

- Martes 16 de junio: 9:00am - 13:00. **4 horas**
- Viernes 19 de junio (presentación pre-examen). No se soldó.
- Martes 23 de junio: 9:00am - 13:00. **4 horas**
- Viernes 26 de junio: 9:00 - 13:00. **4 horas**
- Martes 30 de junio: 10:00 - 13:30. **3 horas y media**
- Miércoles 01 de julio: 11:00  -  21:00. **10 horas.**
- Jueves 02 de julio: 11:00 - 18:00. **7 horas.**
- Viernes 03 de julio: 11:00 - 21:00. **10 horas**
- Domingo 05 de julio: 11:00 - 5:40.  **5 horas 40 min.**
- Lunes 06 de julio: 12:00 - 21:50

El tiempo de trabajo y soldadura fue de aproximadamente de **58 horas.** 

## Carcasa

### Decisiones materiales y formales de la carcasa

La carcasa está compuesta por alambre y acrílico, la planteamos como un accesorio que nos permite que el sintetizador actúe como una extensión del cuerpo. Esta decisión se vincula a la lógica  de Donna Haraway, donde la carcasa se ubica en una parte del cuerpo, permitiendo que el piezo también se conecte a la viola, generando un sistema cyborg bajo la idea de que humanos y máquinas se retroalimentan constantemente, mediante el concepto de la unión entre lo humano, la naturaleza, el instrumento y lo tecnológico (pcb).

### Inspiración y referentes

Formalmente funciona como un ornamento estructural que refuerza la unión entre lo híbrido: un cyborg inspirado en la naturaleza. 

Desde el imaginario colectivo que existe sobre el cyborg, tenemos como referente a Stelarc. Una de sus obras, The Third Hand _(Tokyo, Yokohama, Nagoya 1980)_, es descrita por él con las siguientes palabras: “Acoplado con la tecnología, el cuerpo ahora actúa más allá de los límites de su piel y más allá del espacio local que habita. El cuerpo es ahora un sistema operativo extendido. El cuerpo se ha vuelto obsoleto e invadido por la tecnología.” 

![Stelarc](./imagenes/referente.png)

Tuvimos en cuenta que la utilización de cables para las conexiones entre placas ya se acercaría a esta estética por el simple hecho de estar sobre el cuerpo, así que decidimos reforzar la idea de lo natural a través de una carcasa hecha con ornamentos. En cuanto a las decisiones materiales, utilizamos acrílico y alambre. Habíamos decidido en un principio hacerla completamente de alambre, pero no sabíamos con certeza si es que este podría interferir con el funcionamiento de las placas al ser conductor, por lo que decidimos incluir acrílico en la carcasa para evitar el posible contacto directo. Este material nos permitió la visibilidad de las placas, aportando al imaginario del cyborg y al soporte que necesitábamos para apoyarlas sobre el cuerpo, además, reforzamos la idea de lo natural con ornamentos tallados. Sobre esta base colocamos las formas creadas con alambre, material que nos sirvió gracias a su flexibilidad.

![carcasa](./imagenes/carcasa.png)

Dentro de la inspiración para la realización de estas formas tenemos como referencia la metalistería arquitectónica del Art Nouveau, la cual exhibía formas inspiradas en las curvas sinuosas de la naturaleza, como flores y tallos. Una de las expresiones características de este movimiento fue la utilización de hierro forjado en los edificios para la fabricación de vallas, rejas, balcones decorativos, barandas de escaleras y elementos metálicos en los trabajos de interiorismo. Podemos observar diversos tipos de abstracciones desde el auge del movimiento hasta formas más simples se han mantenido hasta el día de hoy.

![Art Nouveau](./imagenes/referente2.png)

Otros referentes que nos ayudaron en la composición del sistema e interacción son los siguientes:

- **Yonhosago:** banda conformada en 1999 por alumnos de la Universidad Católica donde podemos encontrar guitarras, eléctrica y clásica a la vez, era una banda vanguardista para la época, experimental para otros. 

- **Wave:** obra de Alexey Kochetkov (artista y violinista alemán) en su proyecto 5 String Theory que se inspira en los principios de la generación y procesamiento de sonido propios de los sintetizadores. Aquí el violín se presenta como un oscilador, modelado por capas de efectos para generar texturas electrónicas. [Wave](https://www.youtube.com/watch?v=-chFKYEPqYw&list=RD-chFKYEPqYw&start_radio=1 ) 

## Composición

Nuestra partitura se divide en dos:

- **Visual:** para el intérprete.
- **Escrita:** para el espectador.

Como referente para la primera, tenemos a Asuar, quien en la relación de sus obras utilizaba formas geométricas para representar el sonido que quería crear. Esta forma de observar la música nos da la posibilidad de que quien toque el instrumento pueda interpretar de mejor manera el ritmo que se quiere producir.

![Asuar](./imagenes/partituras.png)
_Documental Variaciones Espectrales – dereojo comunicaciones. (2016)_

**Partitura visual, para el intérprete:**

![visual](imagenes/partitura.png)

Respecto a la segunda, utilizamos como un marco referencial los libros recomendados: Pomelo de Yoko Ono y Anthology of Text Scores de Pauline Oliveros. Estas partituras experimentales nos hicieron ver la posibilidad de incluir relatos más poéticos e instrucciones dentro de la creación de lo musical. Además, referenciamos el poema de Violeta Parra musicalizado por diversos artistas, La Exiliada del Sur, siendo la versión más conocida la de Inti Illimani. 

**Partitura escrita, para el espectador:**

En un país, al sur del globo, existía un pequeño pájaro cuyo canto se convirtió en un hito, pues esta pequeña ave, muy grande de corazón, le hizo un concierto a Violeta Parra.

Es turno de devolver el impulso de fuerza y vida al chirihue mecanizado, quien sin cuerdas en la guitarra y sin hojas en el colihue, la escuchará y revivirá, nos escuchará, y revivirá.

1. Primero vamos a intentar ver la melodía de las cuerdas de la viola, y vamos a ser testigos de cómo cada señal emitida por esta, dará la vida al chirihue para que entone su canto.
2. El chirihue está cantando, ¡ESTÁ VIVO!, pero te necesita a ti, quien le escucha, pues él en su canto reconoce que hay más melodías por entonar…, pero no puede hacerlo sin ti:
Así que ahora acércate a la artista de las cuerdas, y vuélvanse uno; mueve las perillas de los potenciómetros, y escuchemos el cantó de aquel pequeño mecanizado volver a la vida.

3. Gracias a ti, y tu buena bondad, la voz de los más pequeños se hace grande. Escucha y sorpréndete.

4. Y así funcionan diversas naturalezas…, se entretejen y se convierten en una sola.

## Fotografías

![foto1](imagenes/foto1.png)
![foto 2](imagenes/foto2.png)
![foto 3](imagenes/foto3.png)
![foto 4](imagenes/foto4.png)
![foto 5](imagenes/foto5.png)
![foto 6](imagenes/foto6.png)

## Conclusión

Este proceso ha estado lleno de altos y bajos, partimos con una idea muy clara respecto a lo que queríamos hacer, pero nos fuimos topando con varios obstáculos en el camino, ya que nuestra placa principal del Chirihue Mecanizado tuvo bastantes problemas para que funcionara como esperábamos. A pesar de eso y el arduo trabajo en equipo, pudimos rescatar bastantes aprendizajes de esta experiencia. A partir de los conocimientos adquiridos en la clase, pudimos tener una segunda opción en la que utilizamos protoboards y para moder mostrar nuestra propuesta, teniendo una segunda opción, además de recordarnos que es la primera que vez que se realizan este tipo de proyectos en en la universidad. Nos sentimos orgullosos del progreso que tuvimos. 

![procesos](./imagenes/procesos.png)
![grupo](./imagenes/fotogrupo.png)

## Bibliografía

**Criterios de diseño del sistema**

1. ¿Qué es lo vivo y lo no vivo? – Revista endémico. (2025)
2. Manifiesto Ciborg – El sueño irónico de un lenguaje común para las mujeres en el circuito integrado por Donna Haraway. (1984) 
3. Interdependencias que nos sostienen en tiempos de cambio global – Jorgelina Sannazzaro. (2025)
- Ciencia, cyborgs y mujeres: La reinvención de la naturaleza. – Donna Haraway (1991)
- Hacia una filosofía de la fotografía. – Vilém Flusser (1983)

**Contexto desde Chile, desde nuestra disponibilidad material**   

4. 50 años de música electroacústica en Chile – Federico Schumacher Ratti. (2007)
5. ¿Qué es la música electrónica? – Gustavo Becerra. (1957)
- [Documental Variaciones Espectrales – dereojo comunicaciones. (2016)](https://www.youtube.com/watch?v=sJ9EZWBZee8)
- [José Vicente Asuar. (s. f.)| MusicaPopular.cl.](https://www.musicapopular.cl/artista/jose-vicente-asuar/) 
- [José Vicente Asuar: el legado del padre de la música electroacústica en Chile - Universidad de Chile. (s. f.)](https://uchile.cl/noticias/203484/jose-vicente-asuar-el-padre-de-la-musica-electroacustica-en-chile)

**Inspiración y referentes carcasa**

- [STELARC. (s. f.). STELARC, 2025.](https://stelarc.org/_.php#page/3)
- [La metalistería del Art Nouveau, delicados detalles arquitectónicos.](https://lalerou-com.translate.goog/metalwork-art-nouveau/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc) 
- [Melting Home Argentina](https://www.melting.com.ar) 

**Inspiración y referentes partitura**
- [Documental Variaciones Espectrales – dereojo comunicaciones. (2016)](https://www.youtube.com/watch?v=sJ9EZWBZee8)
- Anthology of Text Scores – Pauline Oliveros. (2013)
- Pomelo – Yoko Ono. (1964)


