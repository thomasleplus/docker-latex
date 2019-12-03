# LaTeX

A convenient way to run LaTeX on various platform using Docker.

## Example

Assuming that you have a file `foo.tex` in your current working directory that you want to convert into a PDF `foo.pdf`:

### Mac/Linux

```
$ docker run --rm -it --user="$(id -u):$(id -g)" --net=none -v "$(pwd):/tmp" thomasleplus/latex latexmk -outdir=/tmp -pdf /tmp/foo.tex
```

### Windows

In `cmd`:

```
$ docker run --rm -it --net=none -v "%cd%:/tmp" thomasleplus/latex latexmk -outdir=/tmp -pdf /tmp/foo.tex
```

In PowerShell:

```
$ docker run --rm -it --net=none -v "${PWD}:/tmp" thomasleplus/latex latexmk -outdir=/tmp -pdf /tmp/foo.tex
```

## Help

To know more command line options of `latexmk`:

```
$ docker run --rm -it --net=none thomasleplus/latex latexmk -h
```
