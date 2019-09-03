# Vim

## Todo

* [ ] [http://vimcasts.org/episodes/fugitive-vim-resolving-merge-conflicts-with-vimdiff/](http://vimcasts.org/episodes/fugitive-vim-resolving-merge-conflicts-with-vimdiff/) 
* [ ] [https://vim.works/2019/04/22/marks/](https://vim.works/2019/04/22/marks/)

## Python

There are a couple of plugins around, of course.

### Syntax
* [syntastic](https://github.com/vim-syntastic/syntastic) can be used with:
  * [Flake8](https://pypi.org/project/flake8/),
  * [pylint](https://www.pylint.org/),
  * [pyflakes](https://pypi.org/project/pyflakes/).
* There is also a separate [vim plugin](https://github.com/nvie/vim-flake8) which fires up the Flake8 executable. It is a wrapper around:
  * pep8,
  * pyflakes,
  * [McCabe complexity checker](https://github.com/PyCQA/mccabe).

Having said that, is it as slow as it is with [rubocop](https://github.com/rubocop-hq/rubocop) when large files are parsed?
