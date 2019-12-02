# docker-latex

A convenient way to run LaTeX on various platform using Docker.

## Example

Assuming that you have a file `foo.tex` in your current working directory that you want to convert into a PDF `foo.pdf`:

### Mac/Linux

```
$ docker run -it -v "$(pwd):/tmp" thomasleplus/docker-latex latexmk -pdf foo.tex
```

### Windows

In `cmd`:

```
$ docker run -it -v "%cd%:/tmp" thomasleplus/docker-latex latexmk -pdf foo.tex
```

In PowerShell:

```
$ docker run -it -v "${PWD}:/tmp" thomasleplus/docker-latex latexmk -pdf foo.tex
```

## Help

To know more command line options of `latexmk`:

```
$ docker run -it thomasleplus/docker-latex latexmk -h
```
