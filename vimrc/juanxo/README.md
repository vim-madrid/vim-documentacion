Configuración de Juanxo
======================

Juan Guerrero ([juan.guerrero.lozano@gmail.com](mailto:juan.guerrero.lozano@gmail.com)/ 
[@jguerrero_](https://twitter.com/jguerrero_))

## Particularidades ##

* Uso la `,` en vez de `:`
* Tema slate sobre fondo oscuro
* Statusline un poco especial: `script.js[js][utf-8][Git(mybranch)][+]     40,30/90 30%`
* Resalto los carácteres inválidos (tabuladores y espacios al final de línea)
* Cuando autocompleto en modo comando aparece una lista abajo con todas las opciones, en vez de ir
  iterando sobre todas las posibles
* En modo inserción, `jk` se comporta como `ESC`(esto se lo he robado a yamila xD)
* `F5` elimina todos los caracteres no deseados (tabs y espacios al final)
* El comando `Bclose` elimina el buffer actual pero sin cerrar la ventana(atajo `bd`)
* Las teclas de dirección derecha e izquierda van iterando sobre los buffers abiertos
* Un movimiento entre ventanas simple (`Ctrl + dirección)
* Bundle para gestion de plugins


## Plugins ##

* [ctrlp-vim](https://github.com/kien/ctrlp.vim.git): Permite realizar busquedas sobre el directorio
  y abrir ficheros
* [gist-vim](https://github.com/mattn/gist-vim.git): Crea gists desde vim
* [html5-syntax](https://github.com/othree/html5-syntax.vim): Añade soporte para html5 en cuanto a
  sintaxis y demás
* [jade](https://github.com/digitaltoad/vim-jade): Añade soporte para jade
* [javascript](https://github.com/pangloss/vim-javascript): Mejora el soporte para trabajar con
  javascript
* [jshint](https://github.com/walm/jshint.vim): Añade un comando para ejecutar jshint desde vim
* [markdown](https://github.com/tpope/vim-markdown.git): Añade soporte de sintaxis e indentación
  para markdown
* [nerdtree](https://github.com/scrooloose/nerdtree): Gestor del sistema de ficheros
* [ultisnips](https://github.com/SirVer/ultisnips.git): Permite almacenar snippets que uses con
  frecuencia
* [vim-fugitive](https://github.com/tpope/vim-fugitive): Puedes gestionar git desde vim(ver diffs,
  rama actual, cambios...)
* [vim-haml](https://github.com/tpope/vim-haml): Añade soporte para HAML
* [vim-rails](https://github.com/tpope/vim-rails): Añade una serie de comandos para poder moverse
  eficazmente sobre un proyecto rails(generadores, mover entre controladores/vista/modelo...)
* [vim-rspec](https://github.com/thoughtbot/vim-rspec): Permite ejecutar los tests de RSpec desde
  vim
* [vim-ruby](https://github.com/vim-ruby/vim-ruby.git): Añade soporte para sintaxis y coloreado de
  ruby
* [vim-slim](https://github.com/slim-template/vim-slim): Añade soporte para el lenguaje de markup
  slim
* [vim-surround](https://github.com/tpope/vim-surround.git): Súper útil para refactorizar(cambiar
  `'` por `¨`, cambiar tags html...)
* [webapi-vim](https://github.com/mattn/webapi-vim): Necesario para poder usar el plugin de Gist
* [zencoding](https://github.com/mattn/zencoding-vim): Añade soporte para crear html de manera mucho
  más rápida( `p>div.hola[disabled]` -> `<p><div class=¨hola¨ disabled >`)
