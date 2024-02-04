# Cairo Vim
Vim Syntax for cairo v0.10

## Deprecated ⚠️

Just copy paste this in your ~/.vim/syntax/cairo.vim

Be sure you have this lines in your .vimrc

```vim
"Add Cairo Support
au BufReadPost *.cairo set filetype=cairo
au Filetype cairo set syntax=cairo
```

# Install Coc

Go to 
``https://github.com/neoclide/coc.nvim``

install Coc with your favorite plugin manager, I personaly use Vundle.
In my case I need to do in my .vimrc

``Plugin 'neoclide/coc.nvim', {'branch': 'release'}``

Run :PluginInstall and noramlly at the end you should have a message saying

```shell
build/index.js not found, please install dependencies and compile coc.nvim by: ayrn install
```

Before doing the following command you need to be sure that you have yarn installed on your pc.

We need need to go where coc.nvim is installed to install dependencies.

For that we do ``cd ~/.vim/bundle/coc.nvim && yarn install``

Congrats you finish to install coc but it's not finish we still need to customize it for cairo

Open vim and tap ``:CocInstall coc-cairo`` wait for the download to be finish
and boom You have Coc for cairo

# Useful line to have in your vimrc 

```vim
" This snippet will help you to have a autocomplete workflow like in vscode or intellij

inoremap <silent><expr> <tab> coc#pum#visible() ? coc#pum#next(1) : "\<C-n>"
inoremap <silent><expr> <down> coc#pum#visible() ? coc#pum#next(0) : "\<down>"
inoremap <silent><expr> <up> coc#pum#visible() ? coc#pum#prev(0) : "\<up>"

inoremap <silent><expr> <CR> coc#pum#visible() ? coc#pum#confirm() : "\<CR>"
```
