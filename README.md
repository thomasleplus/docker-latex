# docker-latex

A convenient way to run LaTeX on various platform using Docker.

## Example

Assuming that you have a file `foo.tex` in your current working directory that you want to convert into a PDF `foo.pdf`:

### Mac/Linux

```
$ docker run --rm -it --user="$(id -u):$(id -g)" -v "$(pwd):/tmp" thomasleplus/docker-latex latexmk -outdir=/tmp -pdf /tmp/foo.tex
```

### Windows

In `cmd`:

```
$ docker run --rm -it -v "%cd%:/tmp" thomasleplus/docker-latex latexmk -outdir=/tmp -pdf /tmp/foo.tex
```

In PowerShell:

```
$ docker run --rm -it -v "${PWD}:/tmp" thomasleplus/docker-latex latexmk -outdir=/tmp -pdf /tmp/foo.tex
```

## Help

To know more command line options of `latexmk`:

```
$ docker run --rm -it thomasleplus/docker-latex latexmk -h
```
