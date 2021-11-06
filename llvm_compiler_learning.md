LLVM Learning Tutorials
---

* General Theory / Introduction
  1. [AOSA book: LLVM](https://aosabook.org/en/llvm.html),This is a chapter from the [Architecture of Open Source Applications](https://aosabook.org/en/index.html) book. It is written by Chris Lattner and covers high-level LLVM design
  2. [Compilers](https://online.stanford.edu/courses/soe-ycscs1-compilers).The course is taught by Alex Aiken. In this course, you build a compiler for a real programming language from scratch. It covers the whole compilation pipeline: parsing, type-checking, optimizations, code generation. Besides practical parts, it also dives into the theory.
  3. [Automata Theory](https://online.stanford.edu/courses/soe-ycsautomata-automata-theory). The course is taught by Jeffrey Ullman. This one is pretty heavy on theory. It starts with relatively simple topics like state machines and finite automata (deterministic and otherwise). It gradually moves on to more complex things like Turing-machines, computational complexity, famous P vs. NP, etc.
  4. [Theory of Computation](https://ocw.mit.edu/courses/mathematics/18-404j-theory-of-computation-fall-2020/). This course is taught by Michael Sipser. It is similar to the one above but delivered in a different style. It goes into more detail on specific topics.

* Front-end
  - The compiler front-end is where the interaction with the actual source code happens. The compiler parses the source code into an Abstract Syntax Tree (AST), does semantic analysis and type-checking, and converts it into the intermediate representation (IR).
  - The Compilers course from the above covers the general parts. Here are some links specific to Clang:
    1. [Understanding the Clang AST](https://jonasdevlieghere.com/understanding-the-clang-ast/). his article is written by Jonas Devlieghere. It goes into detail and touches implementation details of Clang’s AST. It also has a lot of excellent links to dive deeper into the subject.
    2. [clang-tour](https://github.com/banach-space/clang-tutor/). This repository maintained by Andrzej Warzyński. It contains several Clang plugins covering various topics, from simple AST traversals to more involved subjects such as automatic refactoring and obfuscation.
  
* Middle-end
  - The middle-end is a place where various optimizations happen. Typically, the middle-ends use some intermediate representation. The intermediate representation of LLVM is usually referred to as LLVM IR or LLVM Bitcode. In a nutshell, it is a human-readable assembly language for a pseudo-machine (i.e., the IR does not target any specific CPU). The LLVM IR maintains certain properties: it is in a Static Single Assignment (SSA) form organized as a Control-Flow Graph (CFG).
    1. [LLVM IR Tutorial - Phis, GEPs and other things, oh my!](https://www.youtube.com/watch?v=m8G_S5LwlTo). This is a great talk by Vince Bridgers and Felipe de Azevedo Piovezan.
    2. [Introduction to LLVM](https://www.youtube.com/watch?v=J5xExRGaIIY). A one-hour-long talk/tutorial from LLVM Developers meeting given by Eric Christopher and Johannes Doerfert. Another great tutorial that better builds on top of the previous video.
    3. [CS 6120: Advanced Compilers](https://www.cs.cornell.edu/courses/cs6120/2020fa/self-guided/). The course is taught by Adrian Sampson. The title says “advanced,” but it covers what one would expect in a modern production-grade compiler: SSA, CFG, optimizations, various analyses.
    4. [Bitcode Demystified](https://lowlevelbits.org/bitcode-demystified/). This one is from me. It gives a high-level description of what’s the LLVM Bitcode is.
    5. [llvm-tutor](https://github.com/banach-space/llvm-tutor). This one is also from Andrzej Warzyński. It covers LLVM plugins (so-called passes) that allow one to analyze and transform the programs in the LLVM IR form.

* Back-end
  - The last phase of the compilation is a back-end. This phase aims to convert the intermediate representation into a machine code (zeros and ones). The zeros and ones later can be run on the CPU. Therefore, to understand the back-end, you need to understand the machine code and how CPUs work.
    1. [Build a Modern Computer from First Principles: From Nand to Tetris](https://www.coursera.org/learn/build-a-computer). Taught by Shimon Schocken and Noam Nisan. This course starts backward: first, you build the logic gates (and, or, xor, etc.), then use the logic gates to construct Arithmetic-Logic Unit (ALU), and then use the ALU to build the CPU. Then you learn how to control the CPU with zeros and ones (machine code), and eventually, you develop your assembler to convert the human-readable assembly into the machine code.
    2. [Parsing Mach-O files](https://lowlevelbits.org/parsing-mach-o-files/). This is a short article written by me. It shows how to parse object files on macOS (Mach-O). If you are on Linux or Windows, search for similar articles on elf and PE/COFF files, respectively
    3. [Performance Analysis and Tuning on Modern CPUs](https://book.easyperf.net/perf_book). The book by Denis Bakhvalov. While it is about performance, it gives an excellent introduction to how CPUs work.
  
* Bonus points
  - Here are some more LLVM related channels I recommend looking at:
    1. [LLVM’s YouTube channel](https://www.youtube.com/channel/UCv2_41bSAa5Y_8BacJUZfjQ). Here you can find a lot of talks from developer meetings.
    2. [LLVM Weekly](https://llvmweekly.org/). A weekly newsletter run by Alex Bradbury. This is the single newsletter I am aware of that doesn’t have ads!
    3. [LLVM Tutorials](https://llvm.org/docs/tutorial/). Good starting points, even if you know nothing about compilers.
    4. [LLVM Blog](https://blog.llvm.org/). This is, well, LLVM’s blog.
    5. [Embedded in academia](https://blog.regehr.org/archives/category/compilers). John Regehr’s blog has lots of goodies when it comes to LLVM and compilers!
