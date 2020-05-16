![LaTeX Logo](/latex.png)

A convenient way to run LaTeX on various platform using Docker (latexmk, pdflatex...).

![Docker Stars](https://img.shields.io/docker/stars/thomasleplus/latex.svg)
![Docker Pulls](https://img.shields.io/docker/pulls/thomasleplus/latex.svg)
![Docker Automated](https://img.shields.io/docker/automated/thomasleplus/latex.svg)
![Docker Build](https://img.shields.io/docker/build/thomasleplus/latex.svg)

## Example

Assuming that you have a file `foo.tex` in your current working directory that you want to convert into a PDF `foo.pdf`:

### Mac/Linux

```
docker run --rm -t --user="$(id -u):$(id -g)" --net=none -v "$(pwd):/tmp" thomasleplus/latex latexmk -outdir=/tmp -pdf /tmp/foo.tex
```

### Windows

In `cmd`:

```
docker run --rm -t --net=none -v "%cd%:/tmp" thomasleplus/latex latexmk -outdir=/tmp -pdf /tmp/foo.tex
```

In PowerShell:

```
docker run --rm -t --net=none -v "${PWD}:/tmp" thomasleplus/latex latexmk -outdir=/tmp -pdf /tmp/foo.tex
```

## Help

To know more command line options of `latexmk`:

```
docker run --rm --net=none thomasleplus/latex latexmk -h
```

## Request new tool

Please use [this link](https://github.com/thomasleplus/docker-latex/issues/new?assignees=thomasleplus&labels=enhancement&template=feature_request.md&title=%5BFEAT%5D) (GitHub account required) to request that a new tool be added to the image. I am always interested in adding new capabilities to these images.
