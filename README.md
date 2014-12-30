SPbAU-Cnzpkt
============

SPbAU MIT Lectures, written and supported by MIT bachelor students.

To read conspects, just download corresponding PDF.

Structure
=========

Every course has corresponding directory.

Templates
---------

In `.templates` directory are stored documents to create and test new document templates (checking new packages, solving technical issues with TeX).

* `XeLaTeX.tex`
  * LDVSOFT's document used for all conspects.

In every directory, there could be `template.tex`, which should be used as a base for writing new documents. They are slightly modified global templates.

Full-course conspect
--------------------

Full-course conspects are ones that have global course program and are written as a single document. This is recommened for maths courses.

* `theory.tex`
  * Main tex file, contains preauble, table of contents and includes other files with actual TeX.
  * All defines and settings should be placed here.
  * Typeset this file to get result.
* `theory.pdf`
  * Final, processed conspect.
  * If you don't want to have headache with editing conspect, look only this file!
  * DO NOT EDIT DIRECTLY.
* `theory-XX.tex`
  * Lectures themselves. Should contain only lectures.
  * Add new lecture as a new file.

Stanalone conspect
------------------

Standalone conspects are ones that have no sence as one document. This is very good for Advanced Algorithms, because every lecture has it's own theme.

* `theory-XX/theory-XX.tex`
  * TeX document for one lecture. It's standalone: preambule, settings and document itself.
* `theory-XX/theory-XX.pdf`
  * Lecture conspect itself.

Typesetting
===========

Documents probably will be typeset every so often on `LDVSOFT` machine. Anyone with Windows OS can install MikTeX and typeset easily, while Linux users are suffering from Tex Live for now. Main issues are:

* `minted`. I recommend using alpha version from [github](https://github.com/gpoore/minted) - install normal version, then download and overwrite with the new one.
* Russian fonts. Without XeTeX, install `PsCyr`. With XeTeX, install Computer Modern Unicode fonts. Any option is quite a headache. 
