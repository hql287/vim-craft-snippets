# Craft CMS Snippets for Vim.

This repository contains most of frequently used code snippets during [Craft CMS](https://craftcms.com/) development.
It is compatible with [Utilsnips](https://github.com/SirVer/ultisnips) and [neosnippet](https://github.com/Shougo/neosnippet.vim) (with minimal configuration).

![Demo](demo.gif)

### Installation
This repo is compatible with most Vim Plugins Manager. Since I use [Vim Plug](https://github.com/junegunn/vim-plug), my configuration looks like this:

**Utilsnips**

```
...
Plug 'Shougo/deoplete.nvim', { 'do': ':UpdateRemotePlugins' } " Completion framework for neovim
Plug 'SirVer/ultisnips'                                       " Snippet Engine
Plug 'honza/vim-snippets'                                     " Default Snippets Source
Plug 'hungle88/vim-craft-snippets'                            " Craft CMS snippets
...
```

**Neosnippet**

```
...
Plug 'Shougo/deoplete.nvim', { 'do': ':UpdateRemotePlugins' } " Completion framework for neovim
Plug 'Shougo/neosnippet'                                      " Snippets Engine
Plug 'Shougo/neosnippet-snippets'                             " Default Snippets Source
Plug 'hungle88/vim-craft-snippets'                            " Craft CMS snippet
...
```
### Configurations
Since Craft templates use `twig` which has its own snippets that come with neosnippet-snippets and vim-snippets by default, we need to
tell vim to look for `craft.snippets` when editing `*.twig` templates by adding these lines to your vimrc

**Utilsnips**
```
...

" Load CraftCMS Snippets
autocmd FileType twig UltiSnipsAddFiletypes craft
...
```

**Neosnippet**

```
...
" Load CraftCMS Snippets
let g:neosnippet#scope_aliases = {}
let g:neosnippet#scope_aliases['twig'] = 'twig,html,js,css,craft'
...
```

### Roadmap
Don't really have one but I'll be adding new snippets as I will be continue working with Craft. 
Any PR is welcome!

### License
MIT