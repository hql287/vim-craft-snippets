# Craft CMS Snippets for Vim.
This repository contains most of frequently used code snippets during [Craft CMS](https://craftcms.com/) development. 
Since I use Neovim, this snippet is compatible with [neosnippet](https://github.com/Shougo/neosnippet.vim) with minimal configurations

![Demo](demo.gif)

### Installation

This repo is compatible with most Vim Plugins Manager. Since I use [Vim Plug](https://github.com/junegunn/vim-plug), my configurations look like this:

```
...
Plug 'Shougo/deoplete.nvim', { 'do': ':UpdateRemotePlugins' } " Completion framework for neovim
Plug 'Shougo/neosnippet'                                      " Snippets Engine
Plug 'Shougo/neosnippet-snippets'                             " Snippets Source
Plug 'hungle88/vim-craft-snippets'                            " Craft CMS snippet
...
```

### Configurations
Since Craft templates use `twig` which has its own snippets that come with neosnippet-snippets by default, we need to
tell neosnippet-snippets to look for `craft.snippets` when editing `*.twig` templates by adding these 2 lines
into your vimrc

```
...
" Load CraftCMS Snippets
let g:neosnippet#scope_aliases = {}
let g:neosnippet#scope_aliases['twig'] = 'twig,html,js,css,craft'
...
```

### License

MIT &copy; [Lê Quốc Hưng](https://github.com/hungle88)
