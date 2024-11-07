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

vim y neovim trabajan con modos. Los modos pensémoslos como capas que están encima del teclado.
