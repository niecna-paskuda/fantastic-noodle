# Vim

## Todo

* [ ] [http://vimcasts.org/episodes/fugitive-vim-resolving-merge-conflicts-with-vimdiff/](http://vimcasts.org/episodes/fugitive-vim-resolving-merge-conflicts-with-vimdiff/) 
* [ ] [https://vim.works/2019/04/22/marks/](https://vim.works/2019/04/22/marks/)
* [ ] [https://github.com/davidhalter/jedi-vim](https://github.com/davidhalter/jedi-vim)
* [ ] [https://github.com/python-mode/python-mode](https://github.com/python-mode/python-mode)

## Python

There are a couple of plugins around, of course, which facilitate developing python in vim.

### Syntax, linters, checkers

Using a plugin to automatically fire tools and display errors inside the editor \(e.g. on writing a file and display errors in the gutter/separate window\):

* [syntastic](https://github.com/vim-syntastic/syntastic): can be used with [multiple checkers](https://github.com/vim-syntastic/syntastic/tree/master/syntax_checkers/python). Synchronous. 

  ❓ Is syntastic as slow as it is with [rubocop](https://github.com/rubocop-hq/rubocop) when large files are parsed?

* [ale](https://github.com/dense-analysis/ale): can be used with [multiple checkers](https://github.com/dense-analysis/ale/blob/master/supported-tools.md) \(see Python\). Asynchronous.
* [vim-flake8](https://github.com/nvie/vim-flake8): fires up the Flake8 executable in currently open file. Not as flexible as the more generic syntastic and ale.

Using a plugin to delegate the checking to a separate tmux/terminal pane. Among others [vimux](https://github.com/benmills/vimux) could be considered.

