# LISP

A directory of resources I've collected and work I've done to teach myself LISP


## About

The books I've followed each have their own folder dedicated to them, in which are found PDFs of the books themselves as well as source code related to their contents. These books include:
- ANSI Common Lisp by Paul Graham


## Prerequisites and usage

In order to follow the books included in this repo, I used a regular old installation of `CLisp` on Ubuntu.

```shell
$ sudo apt install clisp
```

For each chapter I created a new file `c{N}.lsp`, and wrote down every line of code to run it and double check the output. I also did most of the exercises in a separate file `c{N}ex.lsp`.

In order to improve the output of these files, I created a file containing helper functions `headers.lsp`, which would print chaper/section/etc. headers. I also wrote the file `runner.lsp`, in order to see both the input and the output. The program takes any number of files of Lisp source code, and outputs each expression and the resulting output in a way to may it look like it was all typed in a REPL.

```shell
$ clisp runner.lsp c1.lsp c2.lsp c2ex.lsp
```

For easier viewing, it might be nice to pipe the output of the command above into `tail` while following the chapter. Or, for scrolling through the output of any number of chapters, use `less` instead.

```shell
$ clisp runner.lsp c3.lsp | tail -n 20
$ clisp runner.lsp c1.lsp c2.lsp c2ex.lsp | less
```
