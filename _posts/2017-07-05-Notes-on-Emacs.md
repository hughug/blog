---
title: Notes on Emacs
author: Baoyi Chen
Updated: 2017-07-05
---

This is a note on using [GNU Emacs](https://www.gnu.org/software/emacs/) on Mac OSX.  I used to be a  vim user.  I also used the [sublime text](https://www.sublimetext.com/) as the main editor,  sublime text + [skim](http://skim-app.sourceforge.net/) for LaTeX writing and [Typora](https://typora.io/) for Markdown.  After [Leo](http://duetosymmetry.com) showed me the efficiency of using Emacs, I decide to learn it and write down this note. This note will be updated whenever I have time.   



## Notations

 ``C-``    holding the <kbd>control</kbd> key or the META key  while typing other keys

 ``M-``    holding the Meta key ( <kbd>option</kbd> key on Mac) while typing other keys

``RET``   the  <kbd>return</kbd> key

``DEL``   the <kbd>backspace<kbd> key

``SPC``   the <kbd>space<kbd> bar

``ESC``   the <kbd>escape<kbd> key

``TAB``   the <kbd>tab<kbd> key	





## LaTeX

A good extension for writing LaTeX is [AUCTEX](https://www.gnu.org/software/auctex/). 



### Install AUCTEX

- In Emacs, `` M-x list-packages ``
- mark the auctex package for installation with`` i``
- hit ``x`` to execute the installation procedure.




### Compilation 

* open a tex file

  `` C-x C-f your_file_name.tex``


* compile in OS X EI Capitan or higher

  Since EI Capitan does not allow writing directly to */usr* so we need to reconfigure the path for MacTex. 

  - In terminal, use ``which latex`` to find out the location of your latex.  For example, on my mac it is */Library/Tex/texbin/latex*. 

  - then open *~/.emacs*, add the following to configure the path. Remember to change the path accordingly.

    ```
    (getenv "PATH")
    (setenv "PATH"(concat"/Library/Tex/texbin/" ":"(getenv "PATH")))           
    ```

  - now you can compile the .tex file by ``C-x C-a`` and see the generated pdf.




### Editing  

* formatting automatically

  ``C-c C-q C-s``

  ​



## Git

To be updated.



## Org-mode

To be updated.



## Miscellaneous

To be updated.