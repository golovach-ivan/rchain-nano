# Rho-Lang Infrastructure

                          +-----+ = lexer/tokenizer/scanner generator
                *.flex -> |JFlex|
                          +-----+
                             |
                             v
                +-------------------------+
                |Lexer.java               |
      Reader -> |LEXER/TOKENIZER/SCANNER  | -> Stream<Token>
                |import java_cup.runtime.*|
                +-------------------------+
                - based on DFA (deterministic finite automata)
                - *.java    



    +-----------------+      +===========================+ 
    |lang-lex-def.flex|  ->  ||java -jar jflex-1.6.1.jar||
    +-----------------+      +===========================+
                             |
                             v
                    +----------+ 
                    |Lexer.java|
                    +----------+
 
     +---+ -> parser.java            +=============+
     |CUP|                           || javac.exe ||
     +---+ -> sym.java               +=============+
  
### Command line point of view
```shell
# run CUP
java -jar ../../dist/java-cup-11b.jar -interface -parser Parser calc.cup
# compile ???
javac -cp ../../dist/java-cup-11b-runtime.jar:. *.java
# run ???
java -cp ../../dist/java-cup-11b-runtime.jar:. Main
```
  
## JFlex

## CUP
- [http://www2.cs.tum.edu/projects/cup/examples.php](Learning CUP by example)
- [http://www2.cs.tum.edu/projects/cup/docs.php](CUP User's Manual)

## What is CUP?
[CUP 0.11b]()

### CUP2

[http://www2.in.tum.de/~petter/cup2](http://www2.in.tum.de/~petter/cup2/)
> CUP2 is a system for generating parsers from concise specifications. CUP2 is completely written in Java and combines the algorithmic ideas from its predecessor CUP with the features of modern Java.
> While CUP supports 
> - **LALR(1)** only, 

> CUP2 includes 
> - **LR(0)**, 
> - **LR(1)** and 
> - **LALR(1)** 

> out of the box and allows easy extensions for other grammar classes.

> Unlike many other traditional parser generators (also including CUP) CUP2 does not create parser source code based on a separate grammar definition language, but uses Java API calls combined with data structures to represent grammar-related information. This means, there is no special language to define grammars and semantic actions, but everything is done in pure Java. Even more, CUP2 disclaims of generating a parser as a source code file, but rather produces a stream of serialised Java code, which can then be loaded by the CUP2 runtime classes.

## Links
- [Aho, Sethi and Ullmann's "Compilers: principles, techniques, and tools"](http://books.google.de/books?id=n3eVQgAACAAJ)
- [Andrew W. Appel's "Modern compiler implementation in Java"](http://books.google.de/books?id=JNs6fWkJZbAC)
- [Wikipedia: "Context-free grammars"](http://en.wikipedia.org/wiki/Context_free_grammars)
- [Wikipedia: Compiler-Compilers](http://en.wikipedia.org/wiki/Compiler-compiler)
- [Wilhelm, Seidl, Hack, "Compiler Design: Syntactic and Semantic Analysis"](https://www.springer.com/gp/book/9783642175398)
