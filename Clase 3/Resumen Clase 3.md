# Clase 2: Javascript y la librería p5.js
## 22 de agosto 2023

### Links importantes
* [Documentación o referencia de la librería](https://p5js.org/es/reference/): Aquí está toda la información para entender cada "statement" o funciones de p5. 
* [Editor online](https://editor.p5js.org/): p5 puede funcionar en cualquier parte, pero en esta clase ocuparemos el editor web de p5. 📍**Deben iniciar sesión para poder guardar y recuperar sus sketch.**
* [Sketch](https://editor.p5js.org/karina.hyland/sketches/S6krjiMVL) con el que cerramos la tarde.


### Caracteres que vamos a ocupan

`()` paréntesis\
`{}` llaves\
`[]` corchetes\
`'` comilla simple y recta (no esta " ni \`)\
`;` punto y coma\
`//` doble slash para que el programa ignora la lína, también para hacer comentarios. 


### Funciones

La función `setup()` sucede **una vez al ejecutar el programa**. 
Aquí realizamos las acciones iniciales, como crear el lienzo `createCanvas` que necesita dos números: el ancho y el alto en pixeles.
```javascript
function setup() {
  createCanvas(400, 400);
}
```
La función `draw()` sucede **en un loop, 60 veces por segundo**.
Aquí podemos dibujar y ejecutar acciones que se repetirán. 

```javascript
function draw() {
    background(255);
}
```
🎨 La función `background()` recibe colores. 

Los colores podemos escribirlos en varios formatos como:
* (r, g, b) en números de 0 a 255
* (r, g, b, a) en números de 0 a 255 más el canal alpha (transparencia)
* (x) un sólo número entre 0 a 255 para escala de grises
* ('#FFFFFF') en código hexagesimal ocupando comillas. 


#### Dentro de `draw()` aprendimos las figuras primitivas:

📐 `rect(x, y, w, [h])` donde le indicamos su posición en los ejes x/y y el tamaño en ancho (**w**idth) y alto (**h**eight). Los valores son **pixeles** El alto es opcional, si no lo ponemos va a repetir el ancho y dibujar un cuadrado. 

📐 `ellipse(x, y, w, [h])` donde le indicamos su posición en los ejes x/y y el tamaño en ancho (**w**idth) y alto (**h**eight). El alto es opcional, si no lo ponemos va a repetir el ancho y dibujar un círculo.

> La función `draw()` irá dibujando en orden, de arriba hacia abajo. Por lo tanto si pongo una elipse primero que un cuadrado, la elipse quedará detrás.

🎨 `fill(x)` es una función de color del relleno de las figuras que estén después de que la escribo. 

◽️ `noFill()` quita el relleno a las figuras. No necesita ningún argumento entre sus paréntesis.

🎨 `stroke(x)` asigna el color del borde de las figuras que estén después de que la escribo. 

◽️ `noStroke()` le quita el borde. No necesita ningún argumento entre sus paréntesis.

`strokeWeight(x)` cambia el grosor del borde con un número que asigna el ancho en **pixeles**.

> Hay muchas más formas primitivas 2D que puedes probar buscando en la [referencia](https://p5js.org/es/reference/). 

### Variables

🐀 `mouseX` es un valor que indica la posición del mouse en pixeles dentro del canvas en el eje Y. 

🐀 `mouseY` es un valor que indica la posición del mouse en pixeles dentro del canvas en el eje Y. 

Se pueden poner en vez de un número fijo en cualquier función. 

> Para saber qué tipo o cómo son los valores que me entrega, puedo "imprimir" la variable en la consola. Para eso debo ponerla dentro de la función `print()`. 

### Otras funciones 

🐀 `mousePressed()` esta función se ejecuta solo cuando hacemos click en el mouse. Nos sirve para realizar una acción. 

🖼️ `saveCanvas()` descarga una imagen de nuestro lienzo. Podemos indicarle el nombre del archivo en comillas '' y el formato 'jpg' o 'png'. 

## Recomendaciones
Dentro del editor, pueden ir a Archivo > [Ejemplos](https://editor.p5js.org/p5/sketches) y explorar códigos creados por la comunidad. Abran los que les llamen la atención y reemplacen valores para entender cómo funciona. 

![Example page in the p5 web editor](image.png)

También pueden explorar el libro digital ["Generative Gestaltung"](http://www.generative-gestaltung.de/2/) y los ejemplos de arte generativo en p5 que trae. 