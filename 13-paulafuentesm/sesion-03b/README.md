# sesion-03b

**Apuntes**

***Observar:***

Make ( Revista )

***Circuito Astable (AS)***

![astable](https://github.com/paulafuentesm/dis8644-2026-1/blob/7e0e9e0b14f45db9646087e0710d0ef2030692e5/13-paulafuentesm/sesion-03b/imagenes/astable.jpg)

***Circuito monoastable (MS)***

![monostable](https://github.com/paulafuentesm/dis8644-2026-1/blob/7e0e9e0b14f45db9646087e0710d0ef2030692e5/13-paulafuentesm/sesion-03b/imagenes/monostable.jpg)

-----

Ejercicio: 

+ Cuando no hay un punto entre los cables ( lineas verdes ) es porque no se conectan.
  
+ Se puede verificar si esta bien, conectando una led o el parlaten a cada circuto independiente, la cúal, tiene que prender o sononar según corresponda
  
![atari-punk](https://github.com/paulafuentesm/dis8644-2026-1/blob/1e14e17b2a8a12e9556a65dedefd7213f161788c/13-paulafuentesm/sesion-03b/imagenes/atari-punk.png)

Anotaciones Misa:

R1 va a ser un pote
R4 va a ser un LDR
C1 va ser de 100n

***Error 1:***

Se intentó realizar el ejercicio de diferentes maneras, pero al conectar ambos circuitos el parlante hacía ningún sonido. Se observo que el primer problema estaba en el circuito monoestable, donde algunos cables estaban conectados directamente al negativo.

***Error 2:***

En el circuito astable también hubo un error de conexión. Los cables 7 y 6 fueron conectados directamente al positivo, cuando en realidad debían ir conectados al capacitor según el del circuito.

***Error 3:***

En el sistema monoestable se instaló un potenciómetro en lugar de un fotoresistor, que era el boton indicado en el ejercicio.

***Resultado***

Después de corregir las conexiones y caer es una desespracion por rearmar el circuito 3 veces, quemando 2 chip 555. Reemplazar los componentes correspondientes, el circuito comenzó a funcionar correctamente. Se pudo observar que el parlante que generaba vibraciones de mayor o menor intensidad dependiendo de cómo se ajuste el potenciómetro y de la cantidad de luz que recibe el fotoresistor.

![ej_protoboard](https://github.com/paulafuentesm/dis8644-2026-1/blob/5ca99eb5340841b60a328c223eb91253a3d05c16/13-paulafuentesm/sesion-03b/imagenes/protoboard/ej_protoboard.jpg)

Imagen: Los 2 cirucitos conectados ( AS y MS ) hacen sonar el parlante.

![as_protoboard](https://github.com/paulafuentesm/dis8644-2026-1/blob/553886ab3621213eb3288c898db86632be35f3f8/13-paulafuentesm/sesion-03b/imagenes/protoboard/astable_proto.jpg)

Imagen: Circuito Astable con Potenciador.

![ms_protoboard](https://github.com/paulafuentesm/dis8644-2026-1/blob/553886ab3621213eb3288c898db86632be35f3f8/13-paulafuentesm/sesion-03b/imagenes/protoboard/monostable_proto.jpg)

Imagen: Circuito Monostable con Fotoresistor.
