# sesion-02a
# Bitácora – Análisis de Circuitos 

## Observación general
Los tres ejercicios trabajan la misma idea cómo cambia el comportamiento de los LEDS cuando se interrumpe una resistencia. La clave fue identificar qué está en serie, qué está en paralelo y desde dónde se alimenta cada rama.

---

## Ejercicio 1

El circuito tiene un nodo central del que salen tres ramas.

- Al quitar **R1**, se corta la alimentación completa → todo se apaga.
- **R2 y R5** afectan la rama derecha → se apagan D2 y D3.
- **R3 y R4** afectan la rama inferior → se apaga D4.
- D1 depende directamente del camino principal.

En este caso cada rama es bastante independiente, pero todas dependen de R1.

---

## Ejercicio 2

Aquí las ramas están más separadas desde el inicio

- **R5 → D1** (rama independiente)
- **R1–R4 → D2** (todo en serie)
- **R6 y R7 en paralelo → D3**, más **R8** en serie

Casos importantes:

- Quitar **R1–R4** → solo se apaga D2
- Quitar **R5** → solo se apaga D1
- Quitar **R6 o R7** → no pasa nada (hay camino alternativo)
- Quitar **R8** → se apaga D3

Este ejercicio deja claro que el paralelo da “respaldo”.

---

## Ejercicio 3

Este es el más mezclado Y complejo de realizar

- **R1 y R2** están en paralelo al inicio → no afectan mucho individualmente
- **R3** está en el camino principal → si se quita, se apaga todo
- **R4 y R5** están en paralelo → no pasa nada si falta uno
- **R6** alimenta solo a D4 → afecta solo esa rama

Además D3 cuelga directamente del nodo principal, así que depende del flujo general.

---

## Conclusión

En los tres ejercicios se repiten patrones claros:

- Si quitas algo en **serie clave**, cortas todo (ej: R1 en Ej1, R3 en Ej3).
- Si quitas algo en **paralelo**, casi nunca pasa nada porque hay otro camino.
- Si quitas algo en una **rama final**, solo afecta a ese LED.

Al final más que memorizar resultados, lo importante fue leer el circuito como caminos de corriente y no como piezas sueltas.
