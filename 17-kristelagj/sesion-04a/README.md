# sesion-04a
## Clase310326

### pre-clase (teloneo Aaron)

Comenzamos la clase hablando sobre lo que sucedió y opinamos sobre sokio y el trabajo de misaa, además se leyeron todos los feedbacks sobre cómo nos sentíamos e íbamos durante marzo (hoy termino marzo)

Se nos mencionó que tenemos 1 semana para poder rellenar después de dados los encargos

### clase

- Misaa

A Partir de las sugerencias, vimos algunas cosas un poco más lento como el circuito astable y monoestable que hemos visto (falta el biestable)  

(foto)

Misaa nos comentó que el ejercicio que vimos la semana pasada era poco académico porque las probabilidades de que fallara eran muy altas, entonces ahora hicimos una variante de esta y nos funcionó (atari punk console)

(hacer tabla de notación científica de resistencias y condensadores)

Para los condensadores no polarizados el último dígito es equivalente a 0; Por ejemplo, 104 equivale a 10.000 pF

- https://www.falstad.com/circuit/
- axidraw
- evil mad scientist
- meneología
- Aniquilar 555

Si el pin 4 del 555 está conectado a tierra nunca va a tener reseteo 

(foto)

### imagenes de proceso

### post-clase

https://learn.sparkfun.com/tutorials/how-to-use-a-breadboard/all

**Diferencia entre condesadores y resistencias:** las resistencias limitan el flujo de corriente disipando energía en calor, por eso son de carbón, ya que el flujo de electrones no es rapido, mientras que los condensadores almacenan energía temporalmente en un campo eléctrico y la liberan.

### tarea

En mi caso estoy desmantelando un equipo que me prestó mi papá, me enseo sus equipos de audio, sus conexiones y de esa conversación él me enseñó el equipo que tengo en mis manos (a la hora de escribir esto no he investigado aún que es para poder hacer un análisis sin ninguna percepción y cuando termine, investigare y dejaré registro)

Este se llama “Active line drive ALD-1”, el cual tiene un ruido que aún no han podido arreglar para poder escuchar música. 

![active line](imagenes/mccormak-ald1-dna1.jpg)

![Active line drive ALD-1](imagenes/active_line_drive_adl1.jpeg)

Es muy fácil de desarmar, solo tenia 8 tornillos de cruz y listo (es hermoso poder reconocer cosas que antes no tenia pensado en saber. Este ramo me ha ayudado a poder hablar más con mi papá)

Dividi en 4 secciones la PCBA

1. Sección A

Resistencias:

| # | Banda 1 | Banda 2 | Banda 3 | Banda 4 | Banda 5 | Banda 6 |
|---|--------|--------|--------|--------|--------|--------|
| 1 | rojo   | café   | dorado | negro  | negro  | café   |
| 2 | rojo   | café   | café   | café   | rojo   | rojo   |
| 3 | rojo   | café   | naranja| negro  | negro  | café   |
| 4 | rojo   | café   | dorado | verde  | violeta| amarillo |

Condensadores:

| # | Capacitancia | Voltaje |
|---|-------------|--------|
| 1 | 2200 µF     | 50 V   |
| 2 | 100 µF      | 35 V   |
| 3 | 220 µF      | 63 V   |

2. Sección B

| # | Banda 1 | Banda 2 | Banda 3 | Banda 4 | Banda 5 | Banda 6 |
|---|--------|--------|--------|--------|--------|--------|
| 1 | rojo   | café   | café   | amarillo | amarillo | rojo   |
| 2 | rojo   | café   | negro  | blanco   | amarillo | rojo   |
| 3 | rojo   | café   | café   | rojo     | negro    | amarillo |
| 4 | rojo   | café   | café   | amarillo | verde    | café   |
| 5 | rojo   | café   | negro  | celeste  | celeste  | gris   |
| 6 | rojo   | café   | negro  | celeste  | celeste  | celeste|
| 7 | rojo   | café   | café   | café     | rojo     | rojo   |
| 8 | rojo   | café   | café   | amarillo | morado   | rojo   |

| # | Capacitancia | Voltaje |
|---|-------------|--------|
| 1 | 1000 µF     | 35 V   |
| 2 | 10 µF       | 63 V   |
| 3 | 100 µF      | 35 V   |
| 4 | 100 µF      | 16 V   |
