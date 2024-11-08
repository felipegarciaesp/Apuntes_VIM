# Instalación de vim o neovim

Link de descarga de vim: https://www.vim.org/download.php

neovim pretende ser más extensible que vim, pero los dos funcinan exactamente igual. neovim es un fork de vim. Los dos editores son bastante livianos, da igual cual instales la verdad.

# Salir de vim o neovim

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

# Los modos

vim y neovim trabajan con modos. Los modos pensémoslos como capas en nuestro teclado. Las teclas en nuestro teclado muestran cosas distintas si tenemos apretados la techa shift o no, a eso se refieren los modos.

# Abrir un archivo en vim

Si quieres abrir un archivo en vim (por ejemplo, index.js) debes hacer lo siguiente en bash:

```
vim index.js
```

# Moviendo el cursor y entre palabras

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
b:lleva el cursos al comienzo del anterior objeto de texto.
e: lleva el cursos al final del siguiente objeto de texto.
```

# Insertar texto y agregarlo al final

Para insertar texto se debe teclear primero la letra "i" para dejar el curso como una barra vertical. Hecho esto, agregamos el texto. 

Una vez agregado lo que queremos agregar, presionamos la tecla "Esc" dos veces para salir del modo INSERTAR. Si lo apretas una vez, deja pasar un tiempo antes de cambiar de modo. 

Para ingresar al modo INSERTAR también podemos apretar la tecla "a". Esto para que deje el cursor justo depsués de la tecla donde se encontraba posicionado el cursor.

Si apreto "A" (a mayúscula, es decir shift + a), me va a dejar el cursor al final de la línea en el modo de INSERTAR.

# Eliminar texto

En el modo normal posicionate en el caracter que quieres eliminar. Luego apretas la tecla "x" y vas eliminando los caracteres que tienes por delante.

# Guardar los cambios

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

# Moverse entre archivos

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