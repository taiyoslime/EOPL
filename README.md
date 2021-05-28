# EOPL 

Some codes from “Essentials of Programming Languages, Third Edition,” MIT Press, 2008. http://www.eopl3.com/

## Requirement

can work with [EoPL package of Racket v8.0](https://docs.racket-lang.org/eopl/)

## Installation
```bash
# Mac
$ brew install --cask racket

# Ubuntu
$ sudo add-apt-repository ppa:plt/racket
$ sudo apt-get update
$ sudo apt-get install racket
```
FYI: https://download.racket-lang.org/

Then, install package `eopl`.

```bash
$ raco pkg install eopl
```
It may take a litte longer.

## Usage

Accept the program from stdin.
```bash
$ racket letrec.rkt
"letrec even(odd) = proc(x) if zero?(x) then 1 else (odd -(x,1))
    in letrec odd(x) = if zero?(x) then 0 else ((even odd) -(x,1))
        in (odd 13)"
#(struct:num-val 1)
```