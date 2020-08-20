To build locally
================

* Install [Sphinx](http://www.sphinx-doc.org/en/stable/install.html)
* Run the command ```sphinx-build -n . _build``` in this directory.
* Open the file _build/index.html in your browser to view.

To deploy:


To deploy
=========

* build the docs:
```sphinx-build -n . _build```
* check the build
* remove the cached build files
```rm -fr .doctrees```
* move the build out of the repo dir:
```rm -r /tmp/_build; mv _build /tmp```
* check out the gh-pages branch:
```git checkout gh-pages && git pull```
* remove previous files:
```rm -r *```
* move new files in:
```mv /tmp/_build/* .```
* commit and push:
```git add . && git commit -m 'Updated docs' && git push```
