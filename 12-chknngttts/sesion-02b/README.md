# sesion-02b

- ## circuitos 555 trabajos clase y variaciónes
- ![chip 555](./imagenes/555.jpg)
  - ![esquema 555 wiki](./imagenes/555astable.png)
    - https://en.wikipedia.org/wiki/555_timer_IC#/media/File:555_Astable_Diagram.svg
      - timer chip 555
      - cada pin (8) tiene una función
        - se enumeran de abajo a la izquierda (del sacado) a contra reloj
       
- FALTAN DATOS DE ESQUEMAS Y COMPONENTES!!!! 

  - ### **ejercicios pin 555**
    - base
      - ![base 555 esquema1](./imagenes/circuito-1.png)
  - ### **en protoboard y encendido** 
    - ![base 555 irl1](./imagenes/img-circuito1.jpg) ![base 555 irl2](./imagenes/img-circuito2.jpg)
    - ![base 555 irl en movimiento 1uf](./imagenes/video-luz3.gif) (este con capacitor de 1uf)
    - ![base 555 irl en movimiento 10uf](./imagenes/video-luz1.gif) (este con capacitor de 10uf)
    - ![base 555 irl en movimiento 100uf](./imagenes/video-luz8.gif) (este con capacitor de 100uf)
   
      - aqui se ve la diferencia de velocidad intermitente del LED dependiendo del capacitor
        - en el ejemplo de 1uf a traves del ojo humano se ve normal prendida
          - pero al verlo con la camara del celular se notan más los mini impulsos del LED
            - esto se debe a la velocidad de obturación de la camara que es distinta a la del ojo humano
              - si uno cambia el frame rate del video se ve un parpadeo distinto
                - buen video que explica esto
                  - https://www.youtube.com/watch?v=ft2Al-kpc4E
    - cambio tiempo real de capacitores en protoboard
      - ![base 555 irl en movimiento 2 capacitores](./imagenes/video-luz4.gif)
        - si no mal recuerdo los electrones son flojos por lo que van más lento si hay mas espacio por el que puedan pasar
       
    - ### **potenciómetro en protoboard**
      - ![base 555 esquema potenciómetro](./imagenes/circuito-2.png)
      - ![base 555 irl en movimiento potenciómetro](./imagenes/video-luz5.gif)
        - el potenciómetro que usamos es el B100K
          - tiene 3 pins y 100k Ω de resistencia
          - al girar la perilla se permite controlar el voltaje
    - ### **fotorresistencia en protoboard**
      - ![base 555 esquema fotorresistencia](./imagenes/circuito-3.png)
      - ![base 555 irl en movimiento fotorresistencia](./imagenes/video-luz6.gif)
        - este aparato reaccióna a la luz que le llega
          - taparlo cambia el voltaje
            - cambiando el ritmo del LED
    - ### **mezcla fotorresistencia y potenciómetro**
      - ![base 555 irl en movimiento fotorresistencia y potenciómetro](./imagenes/video-luz7.gif)
        - tenia la duda de que ocurriria si se conectaran ambos
          - ambos controlaban el voltaje pero el fotoresistor solo hacia cambios notables con el potenciómetro en un nivel bajo
          - me falta conectar 2 o más fotoresistores para ver que se puede hacer
         
    - ### **3 LED ** ![lol](./imagenes/lol.png)
      - ![protoboard con 3 LED](./imagenes/video-luz2.gif)
            
            
