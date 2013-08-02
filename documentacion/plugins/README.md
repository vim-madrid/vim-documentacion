Plugins
=======

## Instalación ##

La mayoria de los plugins listan en sus README la forma de instalarlos, pero por lo general hay
un par de formas que simplifican en gran manera la instalación: Vundle y Pathogen

### Vundle ###

[Vundle](https://github.com/gmarik/vundle) tiene parecidos con el sistema de gestión de dependencias de ruby.
La idea es listar, dentro del propio .vimrc, los plugins que queremos usar:

```vim
set nocompatible               " be iMproved
filetype off                   " required!

set rtp+=~/.vim/bundle/vundle/
call vundle#rc()

" let Vundle manage Vundle
" required! 
Bundle 'gmarik/vundle'

" My Bundles here:
"
" original repos on github
Bundle 'tpope/vim-fugitive'
" vim-scripts repos
Bundle 'L9'
Bundle 'FuzzyFinder'
" non github repos
Bundle 'git://git.wincent.com/command-t.git'
" git repos on your local machine (ie. when working on your own plugin)
Bundle 'file:///Users/gmarik/path/to/plugin'
```

Una vez tenemos los plugins, ejecutamos `:BundleInstall` desde VIM, lo que nos clonará los proyectos
localmente

### Pathogen ###

[Pathogen](https://github.com/tpope/vim-pathogen) es un plugin para VIM desarrollado por el omnipresente tpope(su lenguaje más utilizado en
GitHub es VimL...). Funciona de manera muy similar a Vundle, con la excepción de que no hace falta
listar nada en el .vimrc. Además, si usas dotfiles(cosa que deberías), te permite añadir los plugins
como submodulos, lo que facilita bastante la gestión.

Para instalarlo, ejecuta esto en tu consola:

```shell
mkdir -p ~/.vim/autoload ~/.vim/bundle; \
curl -Sso ~/.vim/autoload/pathogen.vim \
  https://raw.github.com/tpope/vim-pathogen/master/autoload/pathogen.vim
```
Y añade esto a tu .vimrc:

```vim
execute pathogen#infect()
```

Debe estar en el fichero antes de activar la sintaxis y el autoindentado.
Una vez instalado, simplemente clona(o añade un submódulo si usas dotfiles) el plugin dentro de
`~/.vim/bundle`

### Listado ###

#### Gestión Ficheros ####

* [ctrlp-vim](https://github.com/kien/ctrlp.vim): Permite realizar busquedas usando lógica
  difusa sobre el directorio y abrir ficheros
* [nerdtree](https://github.com/scrooloose/nerdtree): Gestor del sistema de ficheros

#### Sintaxis ####

* [html5-syntax](https://github.com/othree/html5-syntax): Añade soporte para html5 en cuanto a
  sintaxis y demás
* [jade](https://github.com/digitaltoad/vim-jade): Añade soporte para jade
* [javascript](https://github.com/pangloss/vim-javascript): Mejora el soporte para trabajar con
  javascript
* [markdown](https://github.com/tpope/vim-markdown): Añade soporte de sintaxis e indentación
  para markdown
* [vim-haml](https://github.com/tpope/vim-haml): Añade soporte para HAML
* [vim-ruby](https://github.com/vim-ruby/vim-ruby): Añade soporte para sintaxis y coloreado de
  ruby
* [vim-slim](https://github.com/slim-template/vim-slim): Añade soporte para el lenguaje de markup
  slim

#### Git ####

* [gist-vim](https://github.com/mattn/gist-vim): Crea gists desde vim
* [vim-fugitive](https://github.com/tpope/vim-fugitive): Puedes gestionar git desde vim(ver diffs,
  rama actual, cambios...)

#### Manejo de Texto ####

* [ultisnips](https://github.com/SirVer/ultisnips): Permite almacenar snippets que uses con
  frecuencia
* [vim-surround](https://github.com/tpope/vim-surround): Súper útil para refactorizar(cambiar
  `'` por `¨`, cambiar tags html...)
* [zencoding](https://github.com/mattn/zencoding-vim): Añade soporte para crear html de manera mucho
  más rápida( `p>div.hola[disabled]` -> `<p><div class=¨hola¨ disabled >`)

#### Automatizacion ####

* [jshint](https://github.com/walm/jshint.vim): Añade un comando para ejecutar jshint desde vim
* [vim-rspec](https://github.com/thoughtbot/vim-rspec): Permite ejecutar los tests de RSpec desde
  vim

#### Otros ####

* [vim-rails](https://github.com/tpope/vim-rails): Añade una serie de comandos para poder moverse
  eficazmente sobre un proyecto rails(generadores, mover entre controladores/vista/modelo...)
* [webapi-vim](https://github.com/mattn/webapi-vim): Necesario para poder usar el plugin de Gist
