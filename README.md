# Animación de laberinto con CSS

Práctica de animación con CSS puro (sin JavaScript): una figura resuelve un laberinto y vuelve a su punto de inicio en un ciclo infinito.

## Recorrido

1. Empieza como un **cuadrado** arriba de la entrada.
2. Se convierte en **círculo** y ajusta su tamaño para pasar por los pasillos sin tocar las paredes.
3. Recorre el laberinto con `@keyframes` usando coordenadas `left` y `top`.
4. Al salir se convierte en **estrella**, gira y cambia de color mientras recorre el borde.
5. Regresa exactamente al punto de inicio y vuelve a ser el cuadrado original.

## Técnicas

- `@keyframes` con porcentajes calculados según la distancia de cada tramo, para que la velocidad sea constante.
- `border-radius: 50%` para el círculo.
- `clip-path: polygon()` de 10 puntos tanto en el cuadrado como en la estrella, para que la transformación entre ambos sea fluida.
- `transform: rotate()` hasta 1440° (múltiplo de 360°), para que el ciclo cierre sin saltos.

## Verlo

Abre `index.html` en el navegador.

Autor: Maximilian Benjamin Christen Osuna
