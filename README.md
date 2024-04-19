# About

Generate PDF CV from Markdown file.

## Build locally

Tested the build on Ubuntu.

### Install pandoc and other packages

```sh
sudo apt-get update
sudo apt install \
  pandoc \
  texlive-latex-base \
  texlive-fonts-recommended \
  texlive-extra-utils \
  texlive-latex-extra \
  texlive-xetex \
  fonts-ubuntu
```

### Build

```sh
pandoc cv.md -o cv.pdf --pdf-engine=xelatex
```
