# cairo_v0.10_syntax
Vim Syntax for cairo v0.10

Just copy paste this in your ~/.vim/syntax/cairo.vim

Be sure you have this files in your .vimrc

```vim
"Add Cairo Support
au BufReadPost *.cairo set filetype=cairo
au Filetype cairo set syntax=cairo
```
