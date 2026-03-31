# sesion-04a 31.03

Izquierda afinaciones <- -> Derecha salidas

![555](./imagenes/chiprepaso.jpg)

* 0,000.000.000.001 pico
* 0,000.000.001 nano           
* 0,000.001 M (micro)
* 0,001 mili
  
} (C)ondensador
  
* 1 -> Unidad
* 1.000 -> kilo (ohm)
* 1.000.000 -> Mega            
* 1.000.000.000 -> Giga
* 1.000.000.000.000 -> Tera

} (R)esistencia
10.000 picoF -> 100 nanoF -> 0,1 microF

(F)araday: según gemini: Representa la cantidad de electricidad transportada por 1 mol de electrones, derivada de la carga de un solo electrón multiplicada por el número de Avogadro.

## Falstad
<https://www.falstad.com/circuit/>

![555](./imagenes/555pinout.webp)

Mi circuito:

``` mermaid 
graph TD
    VCC["Vcc (9V)"]
    GND["GND"]

    %% Componentes
    R10K["R 10kΩ"]
    LDR["LDR"]
    R1K["R 1kΩ"]
    LED["LED"]
    C1["C 10µF"]
    C2["C 100nF"]

    %% Timer 555 con pines
    subgraph TIMER["Timer 555"]
        P1["Pin 1: GND"]
        P2["Pin 2: TRIG"]
        P3["Pin 3: OUT"]
        P4["Pin 4: RESET"]
        P5["Pin 5: CTRL"]
        P6["Pin 6: THR"]
        P7["Pin 7: DIS"]
        P8["Pin 8: VCC"]
    end

    %% Alimentación
    VCC --> P8
    VCC --> P4
    VCC --> C2
    C2 --> GND

    %% Tierra
    P1 --> GND

    %% Sensor de luz (entrada)
    VCC --> R10K
    R10K --> LDR
    LDR --> P2

    %% Temporización
    P6 --> C1
    P7 --> C1
    C1 --> GND

    %% Salida
    P3 --> R1K
    R1K --> LED
    LED --> GND
```

### Ejercicio en clase

![555](./imagenes/monoyastable.HEIC)
![555](./imagenes/fotoresistor.HEIC)

No nos funcionó a la primera porque no conectamos las tierras (tood el circuito tiene solo una tierra (GND)

Cambiamos el fotoresistor por un potenciometro para probar cosas ;))))
![555](./imagenes/potenciometro.HEIC)

Luego conectamos un potenciometro para controlar el volumen:
![555](./imagenes/volumenpot.HEIC)
