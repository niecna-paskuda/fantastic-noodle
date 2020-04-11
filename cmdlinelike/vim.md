# Vim

## Todo

* [ ] [http://vimcasts.org/episodes/fugitive-vim-resolving-merge-conflicts-with-vimdiff/](http://vimcasts.org/episodes/fugitive-vim-resolving-merge-conflicts-with-vimdiff/) 
* [ ] [https://vim.works/2019/04/22/marks/](https://vim.works/2019/04/22/marks/)
* [ ] [https://github.com/davidhalter/jedi-vim](https://github.com/davidhalter/jedi-vim)
* [ ] [https://github.com/python-mode/python-mode](https://github.com/python-mode/python-mode)
* [ ] [https://github.com/jeetsukumaran/vim-pythonsense](https://github.com/jeetsukumaran/vim-pythonsense)

## Python

There are a couple of plugins around, of course, which facilitate developing python in vim.

### Syntax, linters, checkers

Easily having the code checked regarding the:

* syntax,
* code smells,
* complexity,
* best practises.

Getting around this we could chose either way:

1. Using a plugin to automatically fire tools and display errors inside the editor \(e.g. on writing a file and display errors in the gutter/separate window\):
   * [syntastic](https://github.com/vim-syntastic/syntastic): can be used with [multiple checkers](https://github.com/vim-syntastic/syntastic/tree/master/syntax_checkers/python). Synchronous. 

     ❓ Is syntastic as slow as it is with [rubocop](https://github.com/rubocop-hq/rubocop) when large files are parsed?

   * [ale](https://github.com/dense-analysis/ale): can be used with [multiple checkers](https://github.com/dense-analysis/ale/blob/master/supported-tools.md) \(see Python\). Asynchronous.
   * [vim-flake8](https://github.com/nvie/vim-flake8): fires up the Flake8 executable in the currently open file. Not as flexible as the more generic syntastic and ale.
2. Using a plugin to delegate the checking to a separate tmux/terminal pane. Among others [vimux](https://github.com/benmills/vimux) \(which I'm currently using in Ruby development\) could be considered.

### Debugging

All of the plugins basically allow you to set and clear breakpoints from vim buffer and then the debugger is fired.

#### VimPDB

{% embed url="https://github.com/gotcha/vimpdb" caption="" %}

Did not try it since it does not support Python 3.0 or higher.

#### vim-pudb

{% embed url="https://github.com/KangOl/vim-pudb" %}

#### pudb.vim

{% embed url="https://github.com/SkyLeach/pudb.vim" %}

Did not have any luck firing it in vim8, seems only NeoVim is supported.

#### Vdebug

{% embed url="https://github.com/vim-vdebug/vdebug" %}

Requirement is to install third party software from Komodo, I'd rather find something without such requirements.

### Moving around the code

* using motions which are python-language friendly \(word as well as method/module/class etc\),
* enabling \(for local as well as library entities\):
  * go to definition,
  * find references,
  * auto-completion.

After a quick search it turned out that the \(exuberant\) ctags for python[ have problems when it comes to module names](https://stackoverflow.com/questions/23915741/navigating-python-modules-with-ctags-in-vim). There are scripts around which supposedly \(did not test it!\) fix these issues as well as an alternative \(and still maintained\) implementation – [universal ctags](https://github.com/universal-ctags/ctags).

Another way would be using a [Language Server Protocol](https://langserver.org/) implementation. In other words the client \(vim equipped with an appropriate plugin\) would be fed with smart information from the provider \(an LSP server implementation for python\). 

This solution seems to be flexible, because the configuration ends on having the vim plugin + the LSP server installed for the language of interest. Since my current ctags affair is turning out to be much more dramatic, I will be unchastely switching to the LSP for the time being.

The tools of choice:

* appropriate vim plugin: [ale](https://github.com/dense-analysis/ale),
* LSP server: [palantir](https://github.com/palantir/python-language-server).

{% hint style="info" %}
There are other LSPs servers available, e.g. [Microsoft python LSP](https://github.com/Microsoft/python-language-server)
{% endhint %}

## Javascript

### Syntax, linters, checkers

* [ale](https://github.com/dense-analysis/ale)
* [https://github.com/microsoft/TypeScript](https://github.com/microsoft/TypeScript) + [https://github.com/theia-ide/typescript-language-server](https://github.com/theia-ide/typescript-language-server)



