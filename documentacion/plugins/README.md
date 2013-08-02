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
