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

Para moverse más rápido, ocupa las siguientes teclas:, ocupa la tecla "w". Esta llevará el cursor al comienzo del objeto de texto siguiente.

```
w: lleva el cursor al comienzo del siguiente objeto de texto.
b:lleva el cursos al comienzo del anterior objeto de texto.
```