# asparser
Asparser (Answer Sets parser) is a flex/bison parser that encodes [clingo](https://github.com/potassco/clingo) (or [asprin](https://github.com/potassco/asprin)) output into JSON format. It produces one JSON for each answer.

## Compiling

To compile the asparser executable, run the following command:

``` bash
	make asparser
```

Compiling will generate some temporal files,

 * lex.yy.c
 * y.output
 * y.tab.c
 * y.tab.h
 
that can be removed running `make clean`.

## Usage example

It can be used to encode a file containing a raw clingo/asprin output:

``` bash
	asparser < examples/clingo_satisfiable.txt
```

If the output of clingo/asprin is sent to asparser directly through a pipe, the answers will be encoded (and the JSONs will be printed) "at real-time".

``` bash
	clingo 0 program.lp | asparser
```

- - -

[![twitter][1.1]][1]     [![github][2.2]][2]     [![linkedin][3.3]][3] *Contact*

[1]:https://twitter.com/b_munizcastro
[1.1]:https://cdn4.iconfinder.com/data/icons/iconsimple-logotypes/512/twitter-24.png

[2]:https://github.com/bramucas
[2.2]:https://cdn4.iconfinder.com/data/icons/iconsimple-logotypes/512/github-24.png

[3]:https://www.linkedin.com/in/brais-mu%C3%B1iz-castro-93279115a/
[3.3]:https://cdn4.iconfinder.com/data/icons/iconsimple-logotypes/512/linkedin-24.png

