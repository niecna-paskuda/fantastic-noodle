# Vim

## Todo

* [ ] [http://vimcasts.org/episodes/fugitive-vim-resolving-merge-conflicts-with-vimdiff/](http://vimcasts.org/episodes/fugitive-vim-resolving-merge-conflicts-with-vimdiff/) 
* [ ] [https://vim.works/2019/04/22/marks/](https://vim.works/2019/04/22/marks/)

## Python

There are a couple of plugins around, of course, which facilitate developing python in vim.

### Syntax

|  |  |
| :--- | :--- |
|  |  |

* [syntastic](https://github.com/vim-syntastic/syntastic) can be used with multiple checkers, such as:
  * [Flake8](https://pypi.org/project/flake8/),
  * [pylint](https://www.pylint.org/),
  * [pyflakes](https://pypi.org/project/pyflakes/).
* There is also a separate [plugin – vim-flake8](https://github.com/nvie/vim-flake8) which fires up the Flake8 executable, which itself is a wrapper around:
  * PEP8,
  * [pyflakes](https://pypi.org/project/pyflakes/),
  * [McCabe complexity checker](https://github.com/PyCQA/mccabe).

{% hint style="warning" %}
Having said that, is syntastic as slow as it is with [rubocop](https://github.com/rubocop-hq/rubocop) when large files are parsed?
{% endhint %}

