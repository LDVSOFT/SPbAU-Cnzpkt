# SPbAU-Cnzpkt

SPbAU MIT Lectures, written and supported by MIT bachelor students.

To read compendium, just download corresponding PDF.

## Structure

Every course has corresponding directory.

### Templates

In `.templates` directory are stored documents to create and test new document templates (checking new packages, solving technical issues with TeX).

* `XeLaTeX.tex`
  * LDVSOFT's document used for all compendia.

In every directory, there could be `template.tex`, which should be used as a base for writing new documents. They are slightly modified global templates.

### Full-course compendium

Full-course compendia are ones that have global course program and are written as a single document. This is recommened for maths courses.

* `theory.tex`
  * Main tex file, contains preauble, table of contents and includes other files with actual TeX.
  * All defines and settings should be placed here.
  * Typeset this file to get result.
* `theory.pdf`
  * Final, processed compendium.
  * If you don't want to have headache with editing compendium, look only this file!
  * DO NOT EDIT DIRECTLY.
* `theory-XX.tex`
  * Lectures themselves. Should contain lectures only.
  * Add new lecture as a new file.

### Standalone compendium

Standalone compendia are ones that have no sense as a single document. This is very good for Advanced Algorithms, because every lecture has its own theme.

* `theory-XX/theory-XX.tex`
  * TeX document for one lecture. It's standalone: preambule, settings and document itself.
* `theory-XX/theory-XX.pdf`
  * Lecture compendium itself.

## Typesetting

You can typeset using different tools, like manually from terminal, via TeXworks, etc.

### XeLaTeX

* Windows:
  * Install MikTeX
  * Install Computer Modern fonts from http://sourceforge.net/projects/cm-unicode/files/cm-unicode/0.7.0/cm-unicode-0.7.0-ttf.tar.xz/download
  * Install Latin Modern Math font from http://www.gust.org.pl/projects/e-foundry/lm-math/download/latinmodern-math-1959.zip
  * To typeset, execute once

    texify --pdf --engine=xetex --tex-option=--shell-escape --tex-option=-8bit <document>

  * MikTeX will automaticly download missing packages
* Linux: 
  * Install Tex Live (Download & Install as described [here](http://www.tug.org/texlive/debian.html))
  * To typeset, execute as many times as it will ask:

    xelatex -8bit -shell-escape <document>

  * If it misses packages, use `apt-get` if you installed Tex Live from it or `tlmgr install` if you installed it manually.

### Problems

* `minted` used for syntax highlighting. I recommend using alpha version from [github](https://github.com/gpoore/minted) - install normal version, then download and overwrite with the new one.
* Russian letters. Without XeTeX, install `PsCyr`. With XeTeX, install Computer Modern Unicode fonts (on Linux, they can be easily downloaded as `cm-unicode` TeX package). Any option is quite a headache. 
