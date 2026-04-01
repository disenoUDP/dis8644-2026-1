# sesion-04a

- ## **apuntes clase!!!!1!**

  - ### **parte más teorica**
    - vimos en especéfico el número en dígito de las resistencias y lo que significaban las abreviaciones

| Abreviación | Nombre | Numero            | Potencia |
|-------------|--------|-------------------|----------|
| T           | Tera-  | 1.000.000.000.000 | 10^12    |
| G           | Giga-  | 1.000.000.000     | 10^9     |
| M           | Mega-  | 1.000.000         | 10^6     |
| k           | Kilo-  | 1000              | 10^3     |
| -           |        | 1                 | 1^1      |
| m           | Mili-  | 0.001             | 10^-3    |
| µ           | Micro- | 0.000.001         | 10^-6    |
| n           | Nano-  | 0.000.000.001     | 10^-9    |
| p           | Pico-  | 0.000.000.000.001 | 10^-12   |

  - los resistores se ubican aprx por los kilo y mega
  - los condensadores por los mili, micro y nano

  - esto me recordó a un meme de una zipbomb de supuestamente **55.4 YOTTABYTES**
    - que seria 10^24 (o 1.000.000.000.000.000.000.000.000) x 55.4 bytes
  - ![yottabyte zipbomb meme](./imagenes/zipbomb.png)
    - (esto es posible porque se crea un archivo comprimido que al descomprimir genera muchisimo contenido)
      - ejemplo de como lo explicaron en reddit

      
            - archivo normal: holaholahola
              - comprimido: hola{3}
                - entonces se puede hacer hola{9999999999999999999999999999999999999999999999999999999999999999999999}
              - el archivo ZIP funciona como un comando de lo que se va a hacer para descomprimir el contenido del archivo
                - o eso entendí quizas reddit me mintió

    - ### **hablamos sobre los pin del 555**
      - ![555 pinout](./imagenes/555-pinout.png)
        - 1: Va a tierra (GND)
        - 2: Activa el flip flop interno con una carga negativa
        - 3: Output
        - 4: Resetea el flip flip interno y controla en estado del output en el pin 3
        - 5: Controla el timer (suele no estar en uso e incluso se puede dejar solo)
        - 6: Resetea el flip flop haciendo que el output del switch cambie de alto a bajo cuando la corriente se excede del limite
        - 7: Descarga el "timing capacitor"
        - 8: Vcc/Carga positiva
       
      - (de esto entiendo parte pero hay algunos especificos que me confunden, pero no necesito saber para hacer funcionar el 555)
        - https://www.eimtechnology.com/blogs/articles/pin-configuration-of-555-timer?srsltid=AfmBOoq4Smml05Zj4L-xfwbBtgogC3tOMcc5SWqfCJOw-OGTBbpFC_1G

    - ### **atari punk console 2**
      - hicimos de a 2 la versión inversa del APC
        - con un monoestable conectado a un astable
          - para poder controlar mejor cuando producía sonido
          - además de añadir un LDR
   
      - primero hice yo el astable
        - ![astable LDR](./imagenes/foto-r2.jpg)
          - ![astable LDR gif](./imagenes/foto-r-gif.gif)
         
      - después teniamos que conectar un parlante
        - cambiaba un poco el circuito pero es muy parecido
        - ![astable parlante mal 1](./imagenes/parlante-1-fail1.jpg) ![astable parlante mal 2](./imagenes/parlante-1-fail2.jpg)
          - no me funcionó
            - ![cara triste](./imagenes/sad.png)
        - lo intenté denuevo con más orden en los colores de cable (gracias aaron)
          - ![astable parlante mal 3](./imagenes/parlante-2-fail1.jpg)
            - no me funcionó
              - ![cara triste](./imagenes/sad.png)
        - una vez más
          - ![astable parlante mal 4](./imagenes/parlante-3-fail1.jpg)
            - nuevamente no funcionó
              - ![cara triste](./imagenes/sad.png)
              - dudé del chip, pero efectivamente no era el problema
                - le cambié varios componentes para ver y nada cambiaba
        - le pregunté al misaa e inmediatamente me indicó que tenia mal conectado el parlante
          - #lol
        - ![mono-astable 1](./imagenes/mono-astable1.jpg) ![mono-astable 2](./imagenes/mono-astable2.jpg)
          - ahora si funcionó conectandolo con el de mi compañero
            - al apretar el botón se activaba el parlante y el LED
              - y con el LDR se cambiaba la frecuencia del sonido
             
      - ### **mini extra**
        - nuevamente musica electronica interesante
          - esta vez Jane Remover
          - ![jane remover](./imagenes/jane.jpg)
            - productora de musica electronica
              - también hace shoegaze, emo rock, *dariacore*, rage, pop rap etc...
            - lo que me interesó es que a los **18 años** crea este subgenero de musica electronica
              - el **dariacore** mezcla elementos del hyperpop con sonidos metalicos y digitales
                - y se caracteriza por lo complejo sonoramente, el uso de samples, la velocidad de las canciones y el humor
                - ![dariacore 3](./imagenes/dariacore.png)
                  - https://soundcloud.com/c0ncernn/sets/d-core (leroy es uno de los 13 proyectos/alias diferentes de Jane Remover)
                    - este es el tercer (y ultimo) "Dariacore" que ha sacado hasta ahora
                    - si lo escuchan, se darán cuenta que es muy hiperactivo y que samplea canciones pop como "Heads Will Roll - Yeah Yeah Yeahs" e incluso canciones de sus amigos como "Gunk - Underscores"
                    - por temas legales de copyright no puede estar en spotify/apple music
                   
                - proyectos importantes de Jane Remover fuera de lo que es su genero de "Dariacore"
                  - https://janeremover.bandcamp.com/album/ghostholding
                    - su proyecto "Venturing" es Slowcore
                  - https://janeremover.bandcamp.com/album/census-designated
                    - su segundo album "Census Designated" fue un cambio radical en su usual genero musical
                      - este es más Shoegaze
                  - https://janeremover.bandcamp.com/album/revengeseekerz
                    - su ultimo album bajo el alias de Jane Remover
                      - es más Rage pero sigue con su estilo maximalista
                - no se como lo hace pero saca una cantidad enorme de musica consistentemente
                  - albumes/ep's en distintos alias suyos
                  - NTS Radio mix
                  - Remixes muy buenos
                    - https://frostchildren.bandcamp.com/track/shake-it-like-a-jane-remover-remix
                      - uno de mis favoritos de JR
                     

          - ![hola](./imagenes/lol.png)
          
