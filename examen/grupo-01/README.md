# examen-grupo-01
 
## Integrantes 
 
- Benjamín Alonso Álvarez Pavez / [benjaminalvarez21](<https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/03-benjaminalvarez21>)
- Anays Valentina Cornejo Candia / [Anaysval](<https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/09-Anaysval>)
- Bruno Ferrari Meyer / [chknngttts](<https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/11-chknngttts>)
- Lucas Ignacio Ortiz Aguirre / [ryukivol](<https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/21-ryukivol>)
- Nicolás Elías Valdés Greve / [nicolasvaldesgreve](<https://github.com/disenoUDP/dis8644-2026-1-procesos-2/tree/main/31-nicolasvaldesgreve>)
 
## Criterios de diseño del sistema 
Nuestra propuesta nace de la idea de que las vibraciones, aunque muchas veces pasan desapercibidas, contienen información capaz de generar nuevas formas de interacción.

Aunque las vibraciones pueden parecer un caos, al prestarles atención pueden adquirir un nuevo significado. Por eso buscamos que dejara de ser algo que pasa desapercibido y se convirtiera en la principal forma de interactuar con el sintetizador.

La interacción invita al usuario a explorar el sonido a través del movimiento y contacto directo con el sintetizador, utilizando las vibraciones como un nuevo lenguaje de expresión.

Elegimos ocupar acrilico transparente para romper con la idea de la caja negra, donde el funcionamiento de los objetos permanece oculto. En lugar de esconder su interior, buscamos mostrarlo y poner en valor el diseño de las PCB y de cada uno de sus componentes. De esta manera, la construcción del sistema también pasa a ser parte de la experiencia, invitando a observar cómo estos elementos se relacionan entre sí.


### ¿De dónde partimos? 

No teníamos conocimiento previo antes de entrar al taller, fue nuestra primera vez trabajando con y soldando componentes electrónicos a placas. Aparte de las clases que dieron los profesores buscamos inspiración en páginas web como foros y canales de YouTube que mostraban cómo hacer partes de sintetizadores (ej. filtros, amplificadores, reguladores etc..). 
 
Todo este proceso ha sido prueba y error, si no funciona, se cambia y se vuelve a intentar. Gran parte de la ayuda fue entre compañeros, nos apoyamos para arreglar problemas comunes, compartimos datos de lugares de compra y páginas web para buscar circuitos interesantes. 
 
------------
 
## Referentes 
 
### WhiteSample
 
Ignacio Dacio es un artista chileno dedicado a la música electrónica, diseño de sonido y media art. Estudió Programación Musical en Ircam *(Institut de Recherche et Coordination Acoustique/Musique)* ubicado en Francia, Paris y fue un artista en residencia en el Centro Ars Electronica en Austria, Linz. (Resident Advisor, n.d.)
 
El proyecto musical de Ignacio llamado _White Sample_ nace como algo ligado a la electrónica artesanal, razón por la cual al inicio solo usaba protoboards con circuitos hechos por él mismo. Este proyecto partió principalmente por el interés que tenía Ignacio en construir sus propios componentes electrónicos, manipular sonidos y su participación continua en la escena del DIY.
 
Su sonido está basado en el uso de circuitos analógicos y sistemas modulares, mientras que su estilo híbrido viaja por el techno, ambiente y glitch sin cerrarse a otros subgéneros. (White Sample, 2011)
 
Ha participado en Lollapalooza con estructuras interactivas *(WhiteSample, 2014)* 
 
![whitesample](./imagenes/whitesample-2.jpg)
 
> (WhiteSample & Cargo Collective, 2012)
 
-------------
 
### anthony1
 
anthony1 es un DJ y productor de música chileno. Es parte del underground electrónico más ecléctico con géneros musicales como HexD, Trance y Freeform Hardcore. También forma parte de Team Mekano, un grupo de música electrónica centrada en destacar con sonidos agresivos e intensos.
 
Lograron éxito mundial con su álbum “𝙲𝚕𝚊𝚜𝚜𝚒𝚌_𝙿𝚛𝚘𝚓𝚎𝚌𝚝_𝟸000​.​𝟹𝚐𝚙 [Deluxe Edition]” llegando a más de 6 millones de reproducciones en total.
 
Hace poco anthony1 empezó a experimentar con sets ambientales usando sintetizadores analógicos con efectos de audio digitales para crear paisajes sonoros grandes y conmovedores. Sus sets son improvisados sin partituras a seguir, se toma su tiempo haciendo decisiones importantes como qué efecto usar cuando, sí dejar un loop y por cuánto.
 
Últimamente se ha interesado en el mundo del rock lento 
 
![anthony1](./imagenes/anthony1.png) 
 
> (Anthony1, 2022)
 
----------------
 
## Disponibilidad material 
 
En cuanto a la disponibilidad material en Chile nos ubicamos principalmente en 2 lugares/tiendas; San Diego y Victronics. En San Diego se encuentran varias tiendas de electrónicos que ofrecen distintos componentes, la gracia es los distintos lugares y sus especialidades. 
 
Victronics es una tienda online, por eso pueden ofrecer precios más bajos, además tienen accesorios como espaciadores y pernos para armar las carcasas. 
 
### BOM PCB MAINCRA
 
Este módulo te permite interactuar con el sintetizador mediante vibraciones en el piezo, mediante golpes en el mismo. Estas vibraciones serán captadas por el piezo, lo cual lo tomará como señal para avanzar en el secuenciador. 
 
La idea detrás de esta propuesta nace de la posibilidad de sentir y ver las vibraciones. Aquello que parece caótico o insignificante puede contener señales que, al prestar suficiente atención, adquieren un significado propio. Siguiendo esa lógica, el piezo actúa como un medio para captar esas vibraciones y convertirlas en acciones dentro del sintetizador, permitiendo que elementos normalmente invisibles se vuelvan parte de la interacción. 
 
| Componente | Cantidad | PCB | Valor unitario | Link | ¿Hay stock en LID? |
| --- | --- | --- | --- | --- | --- |
| Chip NE555P | 1 | U1 | $490 | <https://www.victronics.cl/circuitos-integrados/lm555cngeneralpurposebipolartimerdip8/> | Sí |
| Chip TL072CP | 1 | U4 | $990 | <https://www.victronics.cl/circuitos-integrados/tl072cpdualjfetlowpoweropamplifierdip8/> | No |
| Regulador L7805CV | 1 | U3 | $350 | <https://www.victronics.cl/reguladores/reguladorvoltl7805cv5v-15ato220/> | No |
| Diodo 1N4007 | 1 | D5 | $200 | <https://www.mechatronicstore.cl/diodo-rectificador-in4007-1n4007-4007/> | Sí |
| Diodo 1N5819 | 2 | D6, D7 | $586 | <https://cl.rsdelivers.com/product/nexperia/bat85113/nexperia-diodo-bat85113-diodo-schottky-200-ma-30-v/0300978> | No |
| Transistor 2N2222 | 1 | Q1 | $200 | <https://www.mechatronicstore.cl/transistor-2n2222/> | Sí |
| Potenciómetro B10K | 1 | RV1 | $495 | <https://altronics.cl/potenciometro-lineal-10k-b10k> | No |
| Potenciómetro B500K | 1 | RV2 | $495 | <https://altronics.cl/potenciometro-lineal-500k-b500k> | Sí |
| LED 3mm | 3 | D1, D2, D8 | $100 | <https://www.mechatronicstore.cl/led-3mm-5mm/> | Sí |
| Resistencia 47 Ω | 1 | R12 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm> | No |
| Resistencia 100 Ω | 1 | R18 |  $90 | <https://www.electroardu.cl/resistencias-1k-ohm> | Sí |
| Resistencia 220 Ω | 1 | R14 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm> | Sí |
| Resistencia 1 KΩ | 6 | R1, R3, R6, R7, R8, R11 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm> | Sí |
| Resistencia 2,2 KΩ | 1 | R13 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm> | No |
| Resistencia 10 KΩ | 2 | R4, R5 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm> | Sí |
| Resistencia 100 KΩ | 3 | R2, R16, R17 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm> | Sí |
| Resistencia 2,2 MΩ | 1 | R15 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | No |
| Condensador cerámico 1 µF | 1 | C9 | $100 | <https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/> | No |
| Condensador cerámico 4.7 nF | 1 | C12 | $100 | <https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/> | No |
| Condensador cerámico 10 nF | 1 | C13 | $100 | <https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/> | No |
| Condensador cerámico 100 nF | 3 | C1, C7, C10 | $100 | <https://www.mechatronicstore.cl/condensadores-ceramicos-distintos-valores/> | Sí |
| Condensador polarizado 10 µF | 2 | C9, C11 | $100 | <https://www.mechatronicstore.cl/condensador-capacitorio-de-electrolitico-por-unidad-varios-valores/> | Sí |
| Condensador polarizado 100 µF | 3 | C2, C3, C5 | $100 | <https://www.mechatronicstore.cl/condensador-capacitorio-de-electrolitico-por-unidad-varios-valores/> | Sí |
| Piezo | 1 | J8 | $990 | <https://www.mechatronicstore.cl/sensor-piezoelectrico-27mm-con-cable/> | Sí |
| Cables dupont 40 uni. | 1 | - | $2.990 | <https://mcielectronics.cl/shop/product/cable-dupont-macho-macho-20cm-pack-40-unidades-2/> | Sí |
| Batería 9V recargable | 1 | BT1 | $7.990 | <https://www.sodimac.cl/sodimac-cl/articulo/110251085/bateria-recargable-9v/110251089> | Sí |
| Interruptor Switch | 1 | SW3 | $570 | <https://www.katode.cl/switches/1339-interruptor-switch-2-pines-on-off-corto.html> | No |
 
### BOM NANDITTO
 
NANDITTO llegó como solución en un momento de caos. Un circuito simple que permite la conexión de varias señales a un solo chip, unificándolas para tener una sola salida.
Es un circuito integrado con cuatro compuertas NAND, estas compuertas tienen dos entradas y una salida cada una. En nuestro caso estamos solo usando la primera compuerta para conectar el piezo y osciladores.

| Componente | Cantidad | Valor unitario | Link | ¿Hay stock en LID? |
| --- | --- | --- | --- | --- |
| Chip 4093 | 1 | $1.400 | <https://www.cabezacuadrada.cl/product/cd4093b/> | No |
| Resistencia 1 KΩ | 18 | $90 | <https://www.electroardu.cl/resistencias-1k-ohm?> | Sí |
| Potenciometro 100K | 1 | $90 | <https://afel.cl/products/potenciometro-100k-ohm> | Sí |
| Audio Jack | 3 | $200 | <https://es.aliexpress.com/item/1005010713461264.html> | Sí |
| Barrel Jack | 1 | $100 | <https://es.aliexpress.com/item/1005007870346260.html> | Sí |
| Condensador polarizado 1 µF | 1 | $100 | <https://www.victronics.cl/condensadores/cond-electrolitico-1uf-50v-20-105oc-511-p2-5mm-10u/> | Sí |
 
### BOM PCB 03, GRUPO 03: COMANDO ESTELAR
 
Un voltaje entra al chip CD4046, el centro del circuito, que convierte una corriente en una oscilación cuya velocidad varía según el voltaje que le llega. Esa señal pasa luego por dos inversores en el CD40106 que la limpian y estabilizan, hasta llegar al conector de audio jack (el output del módulo). Termina con una señal oscilante limpia y lista para ser procesada por los demás módulos del sintetizador.
 
| Componente | Cantidad | PCB | Valor unitario | Link | ¿Hay stock en LID? |
| --- | --- | --- | --- | --- | --- |
| Chip CD4046 | 1 | U1 | $700 | <https://electronicareal.cl/producto/integrado-digital-cmos-4046/> | No |
| Chip CD40106 | 1 | U4 | $1200 | <https://electronicareal.cl/producto/integrado-digital-cd-40106/> | No |
| L7805 | 1 | U2 | $350 | <https://www.victronics.cl/reguladores/reguladorvoltl7805cv5v-15ato220/> | Sí |
| Diodo 1N4007 | 1 | D1 | $790 | <https://www.victronics.cl/diodos/diodo-rectif-1n4007-1000v-1a-vfd-1-1v-50u/> | Sí |
| LED | 1 | D2 | $300 | <https://electronicareal.cl/producto/led-difuso-blanco-10mm/> | Sí |
| Resistencia 100kΩ | 1 | R1 | $890 | <https://electronicareal.cl/producto/resistencia-1-4-w-100-k-ohm/> | Sí |
| Resistencia 1kΩ | 1 | R2 | $890 | <https://electronicareal.cl/producto/resistencia-1-4-w-1-k-ohm/> | Sí |
| Potenciómetro 100Ω | 2 | RV1, RV2 | $500 | Afel a Ingeniería | Sí |
| Condensador polarizado 10nF | 1 | C1 | $520 | <https://www.victronics.cl/condensadores/condensador-mlcc-10nf-0-01uf-50v-x7r-10-p0-2-10u/> | No |
| Condensador polarizado 100nF | 1 | C5 | $500 | <https://www.victronics.cl/condensadores/condensador-mlcc-0-1uf-50v-x7r-10-p0-1-10u/> | Sí |
| Condensador polarizado 100uF | 2 | C2, C6 | $670 | <https://www.victronics.cl/condensadores/cond-electrolitico-100uf-50v20-105oc-812-p4mm-10u/> | Sí |
| Condensador polarizado 10uF | 2 | C3, C4  | $330 | <https://www.victronics.cl/condensadores/condensadorelectrolitico10uf50v/> | Sí |
| Jack DC | 2 | J2, J3 | $150 | Electrónica Real | Sí |
| Jack de audio | 1 | J1 | $150-$300 | Victronics | Sí |
 
### Carcasas
 
| Componente | Cantidad | Valor unitario | Link/Lugar | ¿Hay stock en LID? |
|----------|-----------|--------|-------------|-------------|
| Interruptor de palanca SPST ON-OFF | 5 | $590 | Electrónica Hobby (Página en remodelado) | No |
| Separador (M3*30mm) | 52 | $1490 x 4 | <https://www.victronics.cl/hardware/separador-niquelado-m330mm-4u/> | No |
| Tuerca (M3) | 20 | $1190 | Pernos alameda | No |
| Golilla (M3) | 40 | $400 | <https://www.victronics.cl/hardware/k3-d218-golilla-m3-ranurada-inox-a2-50u/> | No |
 
### Tiempos trabajo
 
| Proceso | Integrantes | Duración | Total equipo |
|----------|-----------|--------|-------------|
| Procesos y solución de errores | 5 | 3 semanas | 240h |
 
| Proceso | Integrantes | Duración | Total equipo |
|----------|-----------|--------|-------------|
| Soldadura | 5 | 3 semanas | 54h |




----------------
 
# K-dena Lateral 
 
Nuestro sintetizador está formado de 3 módulos: 
 
## Maincra (Piezo/Entrada) 
 
*Un micrófono de contacto detecta vibraciones, manda señales a un amplificador e inversor de señales. Estos convierten la corriente la cual entra a un reloj interno que lo cambia a pasos para que un secuenciador pueda funcionar.*
 
## Comando estelar (Oscilador) 
 
*Esta placa utiliza 2 chip para general oscilaciones que alteran a través de potenciómetros que permiten cambiar tanto la frecuencia como la modulación del sonido.*
 
## NANDITTO (Mixer)
 
*En este circuito se conectan ambos módulos anteriores, y permite la conexión al parlante.*
 
-------------
 
## Procesos 
 
![imagen-procesos](./imagenes/img-larga-final.png)
 
![test gif-1](./imagenes/corte-laser-1.gif) ㅤㅤㅤㅤㅤㅤ ![test gif-2](./imagenes/grito-test-medio.gif)
 
ㅤㅤㅤㅤㅤㅤ![test gif-3](./imagenes/ping-pong.gif)
 
### Para tener un flujo de trabajo más ordenado pusimos todos los componentes necesarios para armar una placa de lado. 
 
**1era dificultad:**
 
- Tuvimos problemas con la organización en la compra de componentes, listas incompletas.
 
### Soldamos los componentes por tamaño (de más pequeño a más grande) y cables para los que van montados en la carcasa. 
 
**2da dificultad:**
 
- También tuvimos problemas con el corte del acrílico para la carcasa.
 
  - **1er corte:** Falta de agujeros para componentes y tamaño equivocado.
 
  - **2do corte:** Formato no compatible de archivo.
 
  - **3er/4to/5to corte:** Parámetros erróneos y líneas de corte extra.
 
  - **6to corte:** Por falta de material usamos los restantes de cortes anteriores.
 
### Armamos las carcasas con los separadores.
 
**3era dificultad:**
 
- Falta de separadores para las carcasas por modificaciones en tamaño.
 
### Se empezó a armar la cubierta de acrílico con los separadores *(gracias al grupo 04 por darnos sus separadores restantes)*. 
 
### Pusimos los potenciómetros, entradas/salidas de audio y switch conectados con los cables.
 
**4ta dificultad:**
 
- Funcionamiento correcto de las PCB, soldamos varias veces las placas, cambiamos los componentes y reemplazamos los cables, pero no funcionaban. 
 
<https://www.youtube.com/watch?v=cKlresqLtPU> *(video reg-1)*
 
<https://www.youtube.com/watch?v=mNxq8Y0R0UI> *(video reg-2)*
 
**5ta dificultad:**
 
- Se nos hizo complicado mantener el funcionamiento de los circuitos, de un momento a otro sonaba distinto y no entendíamos por qué. 
 
----------------
 
# Carcasa 
 
> Escogimos trabajar con acrílico ya que éramos familiares con el material. Es fácil de trabajar por su compatibilidad con el corte láser que nos permitía cortar varias carcasas al mismo tiempo, grabar y lograr un buen oficio. El material es firme, perfecto para lo que teníamos en mente, además es económico.
> 
> Una cualidad del acrílico que utilizamos es la transparencia. Buscamos celebrar el diseño de las PCB a través de la transparencia de este, rompiendo la caja negra e invitando a la apreciación integral de cada placa y sus distintos componentes.
 
### Referentes carcasa 
 
*Para la carcasa usamos estos 3 ejemplos:*
 
> ### **CMF Phone - Nothing (Nothing, 2024)**
> 
> Este dispositivo también utiliza módulos al igual que nuestro sistema.
> 
> ![nothing](./imagenes/phone-1.png)
> 
> ### **microKorg Crystal - Korg (KORG, 2022)**
> 
> Siendo un sintetizador nos llamó la atención que también use carcasa transparente.
> 
> ![korg](./imagenes/korg-1.png)
> 
> ### **Gameboy transparente - Nintendo (Amo, 2011)**
> 
> Al igual que el microKorg Crystal, utiliza una carcasa transparente, permitiendo observar el interior.
> 
> ![gameboy](./imagenes/gameboy-1.png)
> 
> *Utilizamos estos referentes como inspiración para llegar al resultado de las placas, combinando las características que se reflejan en nuestros conceptos.*
> 
 
## Composición 
 
### Referentes
 
- **Yoko Ono:**
 
> ### **"PIEZA DE ESCONDITE"**
> 
> *"Esconderse hasta que todos se vayan a sus casas."*
> 
> *"Esconderse hasta que todos se olviden de uno."*
> 
> *"Esconderse hasta que todos se mueran."*
> *(Ono, 1964, 25)*
 
---
 
### Integración a la vida diaria
 
Al hacer brainstorming de que podríamos hacer como partitura nos dimos cuenta de que nuestras ideas eran actividades que independientes de nuestra partitura se llevan a cabo. Nosotros nos introducimos a está creando una composición nueva cada vez que se toca. 
 
Descubrimos que nuestra partitura calzaba con el principio del Sitio específico, un tipo de obra específica planeada para un lugar concreto. En nuestro caso siendo la mesa de Ping Pong en la FAAD. (Kolodynski, n.d.) 
 
---
 
### Ping Pong
 
*(ver. literal 2)* **Como grupo-01 vamos a ir a República 180, Santiago de Chile con “Maincra” (piezo-01), el parlante, “NANDITTO” (mixer) y "Comando estelar" (oscilador-01). Pedir las paletas y pelotas donde los guardias. Pondremos un piezo en cada paleta de Ping Pong con masking tape. Situar el sintetizador bajo la mesa, asegurar que los cables no se enreden entre sí. Jugar una partida completa de Ping Pong de 21 puntos, con el impacto de la pelota en las paletas el piezo interviene, haciendo que el sonido del oscilador varíe. Al terminar la partida devolver las paletas y la pelota a los guardias.**
 
*(ver. poética)*
 
>**Ve a República 180 y ubica el piezo en la mesa de ping pong**
> 
>**Invita a alguien a jugar**
> 
>**Jueguen durante 5 minutos o hasta que se aburran**
 
------------------
 
## Bibliografía
 
Amo, E. (2011, 02 10). Game Boy Color [A Game Boy Color, shown in clear atomic purple color.]. WikiPedia. <https://upload.wikimedia.org/wikipedia/commons/f/f9/Game-Boy-Color-Purple.jpg?uselang=es>

Anthony1. (2022, 05 12). (ノ^_^)ノƪ(‾.‾“)┐(ノ^_^)ノƪ(‾.‾“)┐. Santiago, Chile. <https://www.instagram.com/anthony1.one/p/CdfBOJiutpF/>

Kolodynski, M. (n.d.). Site-specific | IDIS. Proyecto Idis. <https://proyectoidis.org/site-specific/>

KORG. (2022). microKORG Crystal. KORG. <https://www.korg.com/cl/products/synthesizers/microkorg_crystal/>

Nothing. (2024). CMF Phone 1. NOTHING. <https://cl.nothing.tech/products/cmf-phone-1?Colour=Black&Capacity=8%2B128GB>

Ono, Y. (1964). Pomelo: Un libro de instrucciones de Yoko Ono. <https://monoskop.org/images/8/83/Ono_Yoko_Pomelo_Un_libro_de_instrucciones_de_Yoko_Ono.pdf>

Resident Advisor. (n.d.). White Sample. Resident Advisor. <https://es.ra.co/dj/whitesample/biography>

white sample. (2011, 09 15). white sample. <https://soundcloud.com/white-sample>

WhiteSample. (2014). SpeakerSampler. SpeakerSampler. <https://cargocollective.com/whitesample/SpeakerSampler>

WhiteSample, & Cargo Collective. (2012, 01 04). Live at Mutek_CL. <https://vimeo.com/34586254?fl=pl&fe=ti>

