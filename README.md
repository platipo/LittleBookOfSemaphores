
# LittleBookOfSemaphores

[![download](https://img.shields.io/badge/download-book-success.svg?style=popout-square&logo=github)](https://raw.githubusercontent.com/platipo/LittleBookOfSemaphores/master/book/LittleBookOfSemaphores.pdf)

LaTeX source and supporting code for The Little Book of Semaphores, by Allen Downey.

## Features

 - Informal presentation of classical and less classical problems

 - More than 20 problems solved with hints

 - Puzzle format for syncronization problems

![Problem format](https://github.com/platipo/LittleBookOfSemaphores/blob/master/problem-preview.jpg)

## Build

As easy as it gets: just clone the repo and type

```bash
cd LittleBookOfSemaphores/book
make
```

The book compilation takes advantage of `latexmk` automated document generation.

### Compact version
It's available a more compact version envisioned for printing, to get it switch comments on the conditonal expression `\ifnotcompact`:

```LaTeX
%\notcompacttrue
\notcompactfalse
```

and make the book.

### License
[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
