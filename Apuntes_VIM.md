# Sección 1: Introducción
## Instalación de vim o neovim

Link de descarga de vim: https://www.vim.org/download.php

neovim pretende ser más extensible que vim, pero los dos funcinan exactamente igual. neovim es un fork de vim. Los dos editores son bastante livianos, da igual cual instales la verdad.

## Salir de vim o neovim

Para entrar a vim basta con teclear "vim" en bash.

Para salir de vim hay que teclear Esc dos veces, aparecerán los ":" abajo y debemos teclear la letra "q". 

```
:q
```

Si modificaste el archivo, te podría pasar que te aparezca el siguiente mensaje:

```
E37: No write since last change (add ! to override)
```

Eso es porque no hemos guardado los cambios. Ssi aún así quieres cerrar el archivo, debemos forzar la salida de la sigueinte forma:

```
:q!
```

## Los modos

vim y neovim trabajan con modos. Los modos pensémoslos como capas en nuestro teclado. Las teclas en nuestro teclado muestran cosas distintas si tenemos apretados la techa shift o no, a eso se refieren los modos.

# Abrir un archivo en vim

Si quieres abrir un archivo en vim (por ejemplo, index.js) debes hacer lo siguiente en bash:

```
vim index.js
```

# Sección 2: Lección 1
## Moviendo el cursor y entre palabras

Con las siguientes teclas nos movemos en vim:

```
h: izquierda
l:derecha
k: arriba
j: abajo
```

Para moverse más rápido, ocupa las siguientes teclas:

```
w: lleva el cursor al comienzo del siguiente objeto de texto.
b:lleva el cursor al comienzo del anterior objeto de texto.
e: lleva el cursor al final del siguiente objeto de texto.
```

## Insertar texto y agregarlo al final

Para insertar texto se debe teclear primero la letra "i" para dejar el curso como una barra vertical. Hecho esto, agregamos el texto. 

Una vez agregado lo que queremos agregar, presionamos la tecla "Esc" dos veces para salir del modo INSERTAR. Si lo apretas una vez, deja pasar un tiempo antes de cambiar de modo. 

Para ingresar al modo INSERTAR también podemos apretar la tecla "a". Esto para que deje el cursor justo depsués de la tecla donde se encontraba posicionado el cursor.

Si apreto "A" (a mayúscula, es decir shift + a), me va a dejar el cursor al final de la línea en el modo de INSERTAR.

## Eliminar texto

En el modo normal posicionate en el caracter que quieres eliminar. Luego apretas la tecla "x" y vas eliminando los caracteres que tienes por delante.

## Guardar los cambios

Lo primero es asegurarse de que estás en el modo normal. Luego tecleas lo siguiente:

```
:w
```

Luego de apretar ENTER te debiese aparecer un mensaje de que tu archivo fue guardado con éxito. En el caso del ejemplo que estamos trabajando a mí me ha aparecido lo siguiente:

```
"index.js" [unix] 27L, 646B written
```

Otra forma es teclar lo siguiente:

```
:wq
```

De esta última forma se guardará y se cerrará el archivo.

## Moverse entre archivos

Vamos a aprender a movernos entre archivos dentro del mismo editor.

Si en alguna parte del editor tienes una función, puedes ponerte sobre esta función y teclar "gd" para ir a su definición.

Si haces esto mismo para otro archivo que se está llamando, lo que tienes que hacer es utilizar "gf" en vez de "gd".

Estando en el otro archivo puedes devolverte en el historial presionando "Ctrl + O". Es importante que el cursor se encuentre por sobre el nombre de la función. Si tienes dudas, puedes consultar el video de la clase en el siguiente link: https://www.udemy.com/course/vim-aumenta-tu-velocidad-de-desarrollo/learn/lecture/15495844#overview

Si quieres ir hacia adelante en el historial, presiona "Ctrl + i"

En resumen:

```
gd -> para ir a la definición de una función dentro del código.
gf -> para ir a la definición de un código que se está requiriendo.
Ctrl + o -> para devolverme en el historial.
Ctrl + i -> para ir hacia adelante en el historial. 
```

# Sección 3: Comandos y pegar
## Comandos para eliminar: un-do y re-do

```
dw -> Va borrando las palabras que están por delante del cursor. Hay que estar en el modo normal.
u -> Corresponde a la tecla deshacer. A medida que la vamos presionando, vamos a recuperar lo eliminado (simil a Ctrl + Z)
Ctrl + r -> Va rehaciendo los cambios hechos. En otras palabras, va a rehacer los cambios que habíamos eliminado con la tecla "u".
d$ -> Va a eliminar desde la posición del cursor hasta el final de la línea sin eliminar la linea.
```

## Operadores y movimientos

Vamos a aprender a combinar operadores con movimientos

Puedes combinar la tecla "d" junto con los operadores de movimeinto (e, w, b) para eliminar texto de distintas maneras.

También podemos utilizar números. Por ejemplo, puedes teclar "d3w" para borrar los 3 caracteres que se encuentran por delante de la posición del cursor. Esto es equivalente a teclar "dw" 3 veces.

Puedes ocupar la misma lógica si solamente te quieres mover por el código. Por ejemplo, teclear "3w" va a ser lo mismo que teclear 3 veces w.

Estas combinaciones las puedes ocupar con todas las teclas de movimiento.

## Eliminando lineas, pegar y reordenar listas.

Vamos a aprender a eliminar y a mantener lo eliminado dentro del clipboard (clipboard: lo que mantiene lo que va a ser pegado en otro momento o programa).

Si te posicionas al principio de una línea y aprietas la tecla "d" dos veces (es decir, "dd"), borrarás toda la línea.

Para pegar lo que acabas de eliminar, debes apretas la tecla "p". Esto va a pegar el texto en la línea siguiente en la que se encuentra el cursor.

Si tecleas "P" (p mayúscula), vas a pegar lo eliminado en la linea que se encuentra por sobre la linea donde se encuentra el cursor.

En vim no existe el eliminar, solamente existe el cortar.

Si con la tecla "x" empiezas a eliminar caracteres, al momento de volver a pegar lo eliminado vas a recuperar solamente el último caracter eliminado.

Esta forma de copiar y pegar lineas es la forma más rápida para reordenar lineas.

```
También se puede eliminar con números: 2dd, 8dd, etc.
```

# Sección 4: Reemplazar y cambiar

## Operador de cambio

Comando para reemplazar un caracter: te posicionas sobre el caracter que quieres cambiar debes presionar "r" seguido del caracter que quieres poner.

Operador de cambio: si quieres cambiar una cadena de texto, posiciona el curso al inicio de esta cadena y teclea "cw". La cadena se eliminará por completo y podrás reemplazarla por otra cadena. El comando "cw" va a eliminar todo lo que tengas por delante del cursor en una cadena de texto. Con el comando "ciw" vas a poder borrar toda una cadena de texto independiente de la posición del cursor en esta cadena.

Resumen:

```
r -> Borra el caracter que quieres eliminar. Debes posicionar el cursor a la izquierda del caracter (o sobre este, dependiendo de como se vea tu cursor).
cw -> Borra toda la cadena de texto que haya por delante del cursor. Si posicionas el cursor al inicio de la cadena, borras toda la cadena. Si pones el cursor en la mitad, borrarás la mitad.
ciw -> Vas a poder borrar toda la cadena de texto independiente de la posición del cursor en esta cadena.
```