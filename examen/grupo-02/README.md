# examen-grupo-02

## integrantes

- Isidora Alvarez / [isidoraalvarez](https://github.com/isidoraalvarez/dis8644-2026-1)
- Dayana Pañitrur / [dayanapanitrur](https://github.com/dayanapanitrur/dis8644-2026-1)
- Camila Ramírez / [Estrabismx](https://github.com/Estrabismx/dis8644-2026-1)
- Angel Sabogal / [angel-udp](https://github.com/angel-udp/dis8644-2026-1)
- Tomas Catrileo / [tomascatri](https://github.com/tomascatri/dis8644-2026-1)

# Avance Sábado 04 de Julio 

## Placas usadas

| Placas    | Categoría                                       | Diseñada por                                                        | Imagen                           |
| :-------- | :---------------------------------------------- | :------------------------------------------------------------------ | :-----------------------------   |
| 01        | **RELO** (Reloj)                                | Docentes                                                            | ![Placas](./imagenes/pcb01.jpeg) |
| 02        | **Secuenciador binario** (Secuenciador 02)         | Grupo 02                                                            | ![Placas](./imagenes/pcb02.jpeg) |
| 03        | **Barry Benson** (Percusión 02)                 | Grupo 06                                                            | ![Placas](./imagenes/pcb03.jpeg) |
| 04        | **Chirigüe mecanizado** (Oscilador 01)          | Grupo 04                                                            | ![Placas](./imagenes/pcb04.jpeg) |
| 05        | **Comunicaciones espaciales** (Oscilador 02)    | Grupo 04                                                            | ![Placas](./imagenes/pcb05.jpeg) |
| 06        | **Comando estelar** (Oscilador 01)              | Grupo 03                                                            | ![Placas](./imagenes/pcb06.jpeg) |
| 07        | **Resonancia** (Oscilador 02)                   | Grupo 03                                                            | ![Placas](./imagenes/pcb07.jpeg) |

<br>

## Explicación de flujo de señal de audio:

ordenado a grandes rasgos: gesto humano a fuentes de tiempo, a secuenciador, a osciladores, a filtros, a mezcladores, a parlante.

- La placa 01 corresponde al reloj. Desde ella salen dos señales hacia la placa 02 secuenciador: una entrega el voltaje de alimentación y la otra envía la señal de reloj (clock), que proporciona los pulsos necesarios para el conteo binario del secuenciador. 
- La placa 02 corresponde al secuenciador. Alimentado por el reloj, utiliza la señal de clock para realizar un conteo binario, avanzando un paso con cada pulso recibido. A partir de este conteo, sus salidas generan las señales de control que se distribuyen hacia los cuatro osciladores y la placa de percusión. Una de las salidas se deja sin conexión para incorporar un paso de silencio dentro de la secuencia.

- las placas: 03, 04, 05, 06 y 07 corresponden a fuentes sonoras, reemplazamos todas las conexiones que correspondían a potenciómetros por LDR para regular de forma gestual con luz los parámetros del sonido de cada una de las placas.

- la salida tanto de los cuatro osciladores como del percutor es audio que va a la siguiente placa de amplificador o amplificador comercial, lo cuál está aún en veremos debido a dudas sobre el funcionamiento de parla (placa docentes).

<br>

## Estado de construcción

| Placas    | Categoría       | Diseñada por | Estado de construcción          |
| :-------- | :-------------- | :----------- | :------------------------------ |
| 01        | **RELO** (Reloj)           | Docentes     | Funcional                       |
| 02        | **Secuenciador binario** (Secuenciador 02) | Grupo 02     | Funciona, pero estamos revisando la interconexión con otras PCB mediante el uso de relés |
| 03        | **Barry Benson** (Percusión 02)    | Grupo 06     | Funciona individualmente / Se deben cambiar conectores adaptados para la carcasa |
| 04        | **Chirigüe mecanizado** (Oscilador 01)    | Grupo 04     | Funciona individualmente / Se deben cambiar conectores adaptados para la carcasa |
| 05        | **Comunicaciones espaciales** (Oscilador 02)    | Grupo 04     | Funciona individualmente / Se deben cambiar conectores adaptados para la carcasa |
| 06        | **Comando estelar** (Oscilador 01)    | Grupo 03     | Funciona individualmente / Se deben cambiar conectores adaptados para la carcasa |
| 07        | **Resonancia** (Oscilador 02)    | Grupo 03     | Funciona individualmente / Se deben cambiar conectores adaptados para la carcasa |

<br>

## Resolucion de problemas

**Problema 1**

Queríamos utilizar relés para conectar el secuenciador con los osciladores y la placa de percusión.

Tras conversar con Misaa y revisar el funcionamiento del circuito, entendimos que la forma correcta de conectar los osciladores al secuenciador era mediante relés que actuaran como interruptores, encendiendo y apagando cada placa cuando el secuenciador lo indicara. Después de varios intentos, logramos hacer funcionar este sistema agregando un transistor **2N2222A**, que permitía aumentar el voltaje de salida de cada _step_ desde **4 V** hasta **9 V**.

Posteriormente, consultamos a Aaron para verificar si las conexiones estaban correctamente realizadas y si era posible optimizar y estandarizar el montaje de los relés y transistores.

**Resolución**

Aaron confirmó que el circuito estaba correctamente conectado y que no presentaba problemas de funcionamiento. Sin embargo, recomendó mejorar el orden y la seguridad del montaje utilizando una PCB de prototipado, con el objetivo de organizar mejor las conexiones y reducir la cantidad de cables sueltos.

Intentamos implementar esta solución, pero durante el montaje en la PCB de prototipado se produjeron falsos contactos que impedían el funcionamiento correcto del circuito. Por este motivo, decidimos volver a la configuración inicial, utilizando relés y transistores independientes, pero mejorando el aislamiento con cinta aislante y replicando esta solución en cada _step_.

---

**Problema 2**

La placa **Chirigüe mecanizado** presentaba un volumen considerablemente menor al esperado.

**Resolución**

A pesar de realizar distintas pruebas e intentos de reparación, no fue posible solucionar el problema. Concluimos que se trata de una falla interna de la placa.

---

**Problema 3**

El parlante producía una cantidad importante de estática durante su funcionamiento.

**Resolución**

Identificamos que el parlante estaba configurado para una entrada estéreo, mientras que nuestra salida de audio era mono. Esta incompatibilidad generaba la estática observada. Al utilizar un sistema de amplificación compatible con una señal mono, el problema quedó resuelto.

---

**Problema 4**

Necesitábamos conectar la salida de audio de todos los osciladores y la placa de percusión a un mezclador de audio.

**Resolución**

Utilizamos un **mixer** facilitado por el Laboratorio de Interacciones Digitales, lo que permitió integrar correctamente todas las salidas de audio del sistema.

---

**Problema 5**

Necesitábamos comprobar si la placa **Parla** funcionaba correctamente o si era necesario utilizar otro amplificador.

**Resolución**

Finalmente utilizamos un amplificador proporcionado por el Laboratorio de Interacciones Digitales, el cual cumplió correctamente la función de amplificación del sistema.

<br>

---

<br>

## Materiales faltantes:

- Ldr, tenemos todos conectados a las placas, pero en caso de que fallen, mejor que sobre a que falte.

- Es probable que necesitemos cable para conectar los LDR (Van a salir de la carcasa casi 60cm y disponemos de casi 20 de estos)

<br>

## Dudas GitHub

 - No tenemos claridad sobre cómo incluir este apartado (solicitud de avances por ayudas dia domingo) dentro del repo de examen. Además de saber si la estructura actual es correcta

---

<br>

## Actualización avances 

## criterios de diseño del sistema

inspiración para construir, desde donde partieron

contexto desde Chile, desde nuestra disponibilidad material

nombre de sistema/instrumento construido por medio de módulos

## placas soldadas

Secuenciador 01 / Grupo 2: *Secuenciador 4040*

**Principio de funcionamiento:** Recibe pulsos de un reloj y va cambiando sus salidas una por una, siguiendo una secuencia. Esto permite controlar el orden en que se activan las notas o sonidos del sintetizador. 

Oscilador 01 / Grupo 03: *Comando estelar*

**Principio de funcionamiento:** Genera un sonido cuya frecuencia cambia según el voltaje que recibe. Esto permite modificar el tono del sintetizador de forma continua mediante potenciómetros o señales de control.
 
Oscilador 02 / Grupo 03: *Resonancia*

**Principio de funcionamiento:** Genera un sonido cuya frecuencia puede variar y, al mismo tiempo, usa un secuenciador para activar diferentes pasos en orden. Así crea patrones y cambios de sonido de forma automática.

Oscilador 01 / Grupo 04: *Chirigüe mecanizado*

**Principio de funcionamiento:** Genera sonidos con un oscilador y modifica su tono mediante el circuito, permitiendo obtener diferentes efectos sonoros. 

Oscilador 02 / Grupo 04: *Comunicaciones espaciales*

**Principio de funcionamiento:** Genera una señal de sonido de forma continua y permite cambiar su tono mediante los potenciómetros, creando diferentes efectos y variaciones sonoras. 

Percusión 01 / Grupo 06: *Lub-dub*

 **Principio de funcionamiento:** Genera un golpe de sonido corto cada vez que recibe una señal de activación. Sus controles permiten cambiar el tono y la duración del golpe para crear distintos sonidos de percusión. 

Percusión 02 / Grupo 06: *Barry Benson*

**Principio de funcionamiento:** Genera sonidos de percusión al recibir una señal de activación. Sus controles permiten modificar el tono y el carácter del sonido para obtener diferentes tipos de golpes. 

## Tiempo de soldadura

| Proceso | Integrantes | Duración | Horas por integrante | Total equipo |
|----------|:-----------:|:--------:|----------------------:|-------------:|
| Soldadura, corrección de errores y soluciones de todas las PCB | 5 | 3 semanas | 120 hrs | 120 hrs × 5 = 600 h |

## BOM (Bill Of Materials)

### Reloj

| Componente     | Valor  | Cant | PCB         |
| -------------- | ------ | ---- | ----------- |
| C polarizado   | 47µF   |  1   | C1          |
| C polarizado   | 100µF  | 1    | C2          |  
| C polarizado   | 10µF   | 1    | C4          |
| C polarizado   | 220µF  | 1    | C5          |
| Capacitor      | 100nF  | 2    | C3 C6       |
| LED            | -----  | 2    | D2 D3       |
| Diodo          | 1N4007 | 1    | D1          |
| Resistencia    | 1kΩ    | 4    | R1 R2 R3 R4 |
| LDR            | ------ | 1    | RV1         |  
| Switch         | SPDT   | 1    |  SW1        |
| Chip           | 555    | 1    | U1          |
| Chip           | L7805  | 1    | U2          |
| Base Dip       | 8 pin  | 1    | U1          |
| Perno M3       |        | 4    | H1 H2 H3 H4 |
| Conector       | Barrel | 2    | J1 J2       |
| Conector       | Jack   | 1    | J3          |

<br>

### Secuenciador 1 / Grupo 02

| Componente     | Valor  | Cant | PCB         |
| -------------- | ------ | ---- | ----------- |
| C polarizado   | 100µF  |  1   | C4          |
| C polarizado   | 10µF   | 1    | C5          |
| Capacitor      | 100nF  | 1    | C6          |
| Led            |        | 7    | D8 D9 D10 D11 D12 D13 D14 |
| Diodo          | 1N4007 | 1    | D6          |
| Transistor     | 2N2222 | 6    | Q1 Q2 Q3 Q4 Q5 Q6 |
| Resistencia    | 1KΩ    | 19   | R7 R8 R9 R10 R11 R12 R13 R14 R15 R16 R17 R18 R19 R21 R22 R23 R24 R25 R26 |
| Resistencia    | 100KΩ  | 1    | R20         |
| Switch         | SPDT   | 1    | SW1         |
| Chip           | 4040   | 1    | U2          |
| Chip           | L7805  | 1    | U4          |
| Base Dip       | 16 pin | 1    | U2          |
| Perno M3       |        | 4    | H1 H2 H3 H4 |
| Conector       | Barrel | 2    | J2 J3       |
| Conector       | Jack   | 8    | J6 J7 J8 J9 10 J11 J12 |

<br>

### Oscilador 01 / Grupo 03

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

<br>

### Oscilador 02 / Grupo 03

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

<br>

### Oscilador 01 / Grupo 04

| Componente     | Valor  | Cant | PCB         |
| -------------- | ------ | ---- | ----------- |
| C. polarizado  | 10µF   | 3    | C2 C3 C10   |
| Capacitor      | 100nF  | 2    | C4 C11      |
| C. polarizado  | 100µF  | 1    | C9          |
| Diodo          | 1N4007 | 1    | D1          |
| LED            | -----  | 1    | D2 D8       |  
| Diodo          | 1N4148 | 4    | D3 D4 D5 D6 |
| Resistencia    | 1KΩ    | 7    | R2 R3 R4 R5 R6 R7 R8 |
| LDR            |        | 4    | RV1 RV2 RV3 RV4 |
| Switch         | SPDT   | 1    | SW1         |
| Chip           | 40106  | 1    | U1          |
| Chip           | L7805  | 1    | U2          |
| Chip           | LM324  | 1    | U3          |
| Base Dip       | 14 pin | 2    | U1 U3       |
| Perno M3       |        | 4    | H1 H2 H3 H4 |
| Conector       | Barrel | 2    | J1 J3       |
| Conector       | Jack   | 1    | J4          |

<br>

### Oscilador 02/ Grupo 04

| Componente     | Valor  | Cant | PCB         |
| -------------- | ------ | ---- | ----------- |
| C. polarizado  | 1µF    | 3    | C1 C2       |
| C. polarizado  | 10µF   | 2    | C3 C5       |
| C. polarizado  | 100µF  | 1    | C4          |
| Capacitor      | 100nF  | 1    | C6          |
| Diodo          | 1N4148 | 1    | D1          |
| Diodo          | 1N4007 | 1    | D2          |
| LED            | ------ | 1    | D8          |
| Resistencia    | 1KΩ    | 3    | R1 R2 R9    |
| LDR            |        | 2    | RV1 RV2     |
| Switch         | SPDT   | 1    | SW1         |
| Chip           | 40106  | 1    | U1          |
| Chip           | L7805  | 1    | U5          |
| Base Dip       | 14 pin | 1    | U1          |
| Perno M3       |        | 4    | H1 H2 H3 H4 |
| Conector       | Barrel | 2    | J1 J3       |
| Conector       | Jack   | 1    | J4          |

<br>

### Percusión 02 / Grupo 06

| Componente     | Valor  | Cant | PCB         |
| -------------- | ------ | ---- | ----------- |
| C. polarizado  | 10µF   | 3    | C1 C4 C6    |
| C. polarizado  | 100µF  | 2    | C2 C5       |
| C. polarizado  | 1µF    | 1    | C3          |
| Capacitor      | 100nF  | 1    | C7          |
| Diodo          | 1N4007 | 1    | D1          |
| Led            |        | 2    | D8 D9       |
| Resistencia    | 1KΩ    | 2    | R4 R5       |
| LDR            |        | 4    | RV1 RV2 RV3 RV4 |
| Switch         | SPDT   | 1    | SW3         |
| Chip           | 40106  | 1    | U1          |
| Chip           | L7805  | 1    | U8          |
| Chip           | 4070   | 1    | U9          |
| Base Dip       | 14 pin | 2    | U1 U9       |
| Perno M3       |        | 4    | H1 H2 H3 H4 |
| Conector       | Barrel | 2    | J2 J3       |
| Conector       | Jack   | 1    | J4          |


## BOM General

| Componente | Valor | Cantidad | Valor Unitario | Valor Total |
|------------|-------|---------:|---------------:|------------:|
| Capacitor Polarizado | 220µF | 1 | 100 | 100 |
| Capacitor Polarizado | 100µF | 9 | 100 | 900 |
| Capacitor Polarizado | 47µF | 1 | 100 | 100 |
| Capacitor Polarizado | 10µF | 14 | 100 | 1400 |
| Capacitor Polarizado | 4µF | 1 | 100 | 100 |
| Capacitor Polarizado | 1µF | 4 | 100 | 400 |
| Capacitor Polarizado | 0.22µF | 3 | 100 | 300 |
| Capacitor | 1µF | 2 | 740 | 1480 |
| Capacitor | 100nF | 10 | 100 | 1000 |
| Capacitor | 10nF | 1 | 100 | 100 |
| Diodo | 1N4007 | 7 | 200 | 1400 |
| Diodo | 1N4148 | 5 | 120 | 600 |
| LED | - | 16 | 100 | 1600 |
| LDR | - | 15 | 990 | 14850 |
| Resistencia | 220Ω | 10 | 100 | 1000 |
| Resistencia | 1kΩ | 37 | 100 | 3700 |
| Resistencia | 100kΩ | 2 | 100 | 200 |
| Resistencia | 330kΩ | 1 | 100 | 100 |
| Resistencia | 470kΩ | 2 | 100 | 200 |
| Transistor | 2N2222 | 13 | 390 | 5070 |
| Switch | SPDT | 7 | 300 | 2100 |
| Chip | NE555 | 1 | 490 | 490 |
| Chip | CD4017 | 1 | 890 | 890 |
| Chip | CD40106 | 5 | 750 | 3750 |
| Chip | CD4040 | 1 | 390 | 390 |
| Chip | CD4046 | 2 | 700 | 1400 |
| Chip | CD4070 | 1 | 2080 | 2080 |
| Chip | LM324 | 1 | 590 | 590 |
| Regulador de Voltaje | L7805 | 7 | 490 | 3430 |
| Base DIP | 8 pines | 1 | 450 | 450 |
| Base DIP | 14 pines | 6 | 600 | 3600 |
| Base DIP | 16 pines | 4 | 640 | 2560 |
| Conector | Barrel | 14 | 150 | 2100 |
| Conector | Jack | 14 | 180 | 2520 |
| Perno | M3 | 28 | 39,9 | 1117,2 |
| **TOTAL GENERAL** |  |  |  | **$61.597** |


## carcasa

decisiones materiales y formales de la carcasa

inspiración y referentes (con cita)

## Proceso

| Proceso 1 | Proceso 2 | Proceso 3 | Proceso 4 |
|---------|---------|---------|---------|
|  ![Proceso01](./imagenes/pr-01.jpeg) | ![Proceso02](./imagenes/pr-02.jpeg) |  ![Proceso03](./imagenes/pr-03.jpeg) | ![Proceso04](./imagenes/pr-04.jpeg) |

| Proceso 5 | Proceso 6 | Proceso 7 | Proceso 8 |
|---------|---------|---------|---------|
| ![Proceso05](./imagenes/pr-05.jpeg) | ![Proceso06](./imagenes/pr-06.jpeg) | ![Proceso07](./imagenes/pr-07.jpeg) | ![Proceso08](./imagenes/pr-08.jpeg) |

| Proceso 9 | Proceso 10 | Proceso 11 | Proceso 12 |
|---------|---------|---------|---------|
| ![Proceso09](./imagenes/pr-09.jpeg) | ![Proceso10](./imagenes/pr-10.jpeg) | ![Proceso11](./imagenes/pr-11.jpeg) |  ![Proceso12](./imagenes/pr-12.jpeg) |

| Proceso 13 | Proceso 14 | Proceso 15 | Proceso 16 |
|---------|---------|---------|---------|
| ![Proceso13](./imagenes/pr-13.jpeg) | ![Proceso16](./imagenes/pr-16.jpeg) | ![Proceso17](./imagenes/pr-17.jpeg) | ![Proceso08](./imagenes/pr-08.jpeg) |

| Proceso 17 | Proceso 18 | Proceso 19 | Proceso 20 |
|---------|---------|---------|---------|
| ![Proceso21](./imagenes/pr-21.jpeg) | ![Proceso22](./imagenes/pr-22.jpeg) | ![Proceso23](./imagenes/pr-23.jpeg) |  ![Proceso24](./imagenes/pr-24.jpeg) |

| Proceso 21 | Proceso 22 | Proceso 23 | Proceso 24 |
|---------|---------|---------|---------|
| ![Proceso21](./imagenes/placas-soldadas.jpeg) | ![Proceso22](./imagenes/parlante.jpeg) | ![Proceso17](./imagenes/pr-17.jpeg) | ![Proceso08](./imagenes/pr-08.jpeg) |

| Proceso 25 | Proceso 26 | Proceso 27 | Proceso 28 |
|---------|---------|---------|---------|
| ![Proceso21](./imagenes/placas-soldadas.jpeg) | ![Proceso22](./imagenes/parlante.jpeg) | ![Proceso17](./imagenes/pr-17.jpeg) | ![Proceso08](./imagenes/pr-08.jpeg) |


---


| Video 1 | Video 2 | Video 3 |
|:-------:|:-------:|:-------:|
| [![Video 1](https://img.youtube.com/vi/JmE9NbwjoMs/hqdefault.jpg)](https://youtube.com/shorts/JmE9NbwjoMs) | [![Video 2](https://img.youtube.com/vi/Sk7TLUBUIL0/hqdefault.jpg)](https://youtube.com/shorts/Sk7TLUBUIL0) | [![Video 3](https://img.youtube.com/vi/-w2bnB7ahFI/hqdefault.jpg)](https://youtube.com/shorts/-w2bnB7ahFI) |
| **Video 4** | **Video 5** | **Video 6** |
| [![Video 4](https://img.youtube.com/vi/Z8LjF2_bu-w/hqdefault.jpg)](https://youtube.com/shorts/Z8LjF2_bu-w) | [![Video 5](https://img.youtube.com/vi/l9U1S9-KGVk/hqdefault.jpg)](https://youtube.com/shorts/l9U1S9-KGVk) | [![Video 6](https://img.youtube.com/vi/rXEYtkrxyr4/hqdefault.jpg)](https://youtube.com/shorts/rXEYtkrxyr4) |
| **Video 7** | **Video 8** | **Video 9** |
| [![Video 7](https://img.youtube.com/vi/mTNN9lAFyIs/hqdefault.jpg)](https://youtube.com/shorts/mTNN9lAFyIs) | [![Video 8](https://img.youtube.com/vi/chz79BSDsxw/hqdefault.jpg)](https://youtube.com/shorts/chz79BSDsxw) | [![Video 9](https://img.youtube.com/vi/vpFVOLXRS30/hqdefault.jpg)](https://youtube.com/shorts/vpFVOLXRS30) |
| **Video 10** | **Video 11** | **Video 12** |
| [![Video 10](https://img.youtube.com/vi/bo8u3_Ju_fE/hqdefault.jpg)](https://youtube.com/shorts/bo8u3_Ju_fE) | [![Video 11](https://img.youtube.com/vi/CvPNiDL23gA/hqdefault.jpg)](https://youtube.com/shorts/CvPNiDL23gA) | [![Video 12](https://img.youtube.com/vi/T8TXoX9cu-E/hqdefault.jpg)](https://youtube.com/shorts/T8TXoX9cu-E) |

---

## composición

partitura e interpretación

detallar operación de la partitura, como se creó, cuales fueron los referentes (citando), cual es la simbología

---

## bibliografía

### REFERENTES

| Referencia | Imagen |
|------------|--------|
| https://www.lovehulten.com/ | ![Love Hultén](./imagenes/) |
| https://www.kickstarter.com/projects/oficinadesonido/my-first-modular | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |

### MATERIALIDAD

| Referencia | Imagen |
|------------------------|--------|
| https://www.acryl.cl/ | ![Acryl](./imagenes/) |
| https://abingraf.cl/collections/planchas-de-acrilico/products/acrilico-mgraf-blanco-fundido-3-mm-liner-plastico-1-22-x-2-44-mts | ![Acrílico](./imagenes/) |
| https://www.mundotransfer.cl/vinilo-de-corte-soft-cut-51-cm-ancho.html | ![Vinilo Soft Cut](./imagenes/) |
| https://abingraf.cl/products/vinilo-de-corte-brillante-metamark-m4-0-61-mts | ![Metamark M4](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |

### CONSTRUCTIVO

| Referencia | Imagen |
|------------|--------|
| https://www.matrixsynth.com/2013/04/folktek-feedscape-one-of-kind-hand-made.html?m=1 | ![Feedscape](./imagenes/) |
| https://www.yankodesign.com/2023/01/24/this-strange-looking-plant-box-uses-science-to-create-eerie-music/ | ![Plant Box](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |
|  | ![](./imagenes/) |


