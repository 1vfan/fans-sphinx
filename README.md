# sphinx.doc

Publishing sphinx-generated docs on github or Hosting in [readthedocs](https://readthedocs.org).

## Why sphinx-doc

[sphinx-doc](http://www.sphinx-doc.org/en/master/) is a tool that makes it easy to create intelligent and beautiful documentation.

sphinx-doc use [reStructuredText](http://www.pythondoc.com/sphinx/contents.html) as its markup language, it was originally created for the ``Python`` documentation.

## Quick start

- Confirm ``Python`` has installed.

```bash
Stefan-Mac:~ stefan$ python3 --version
Python 3.7.2
```

- Install sphinx and for help.

```bash
$ pip3 install sphinx
$ sphinx-build -h
```

- Create working directory and quickstart.

```bash
$ sphinx-quickstart ~/Sphinx
$ ls -l ~/Sphinx
-rw-r--r--@  1 stefan  Makefile
-rw-r--r--   1 stefan  make.bat
drwxr-xr-x  11 stefan  source
drwxr-xr-x   2 stefan  build
```

- Make html and open ``~/Sphinx/build/html/index.html``

```bash
$ cd ~/Sphinx
$ make html
```

## Custom config

- Adopt a third party theme ``sphinx_rtd_theme`` and config ``conf.py``.

```bash
$ pip3 install sphinx_rtd_theme
$ sed 's/alabaster/sphinx_rtd_theme/g' ~/Sphinx/source/conf.py > ~/Sphinx/source/conf1.py
$ cp ~/Sphinx/source/conf1.py > ~/Sphinx/source/conf.py
$ rm -f ~/Sphinx/source/conf1.py
```

- Change output path(eg.github repository) for generated html.

```bash
$ vi ~/Sphinx/Makefile
#BUILDDIR    = build
BUILDDIR     = ~/Github/sphinx.doc
```

when ``make html`` generated html and git push to [sphinx.doc](https://github.com/1vfan/sphinx.doc).

## Elegant access

Building GitHub Pages site `https://1vfan.github.io/sphinx.doc` for [sphinx.doc](https://github.com/1vfan/sphinx.doc) from the master branch. 

Custom domains [sphinx.doc](doc.lvfan.me) allow you to serve your site from a domain.
