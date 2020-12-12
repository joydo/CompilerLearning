# CompilerLearning

## Online Resources

* Compilers books: I'd start with "Engineering a Compiler" by Keith Cooper and Linda Torczon. http://craftinginterpreters.com/ is also a pretty great, programming-oriented intro, which may be good to work through alongside. For more on the analysis & compiler optimization side, "SSA-based Compiler Design" (http://ssabook.gforge.inria.fr/latest/; GitHub Mirror: https://github.com/pfalcon/ssabook) is a good follow-up.

* Further readings: Book recommendations in https://github.com/MattPD/cpplinks/blob/master/compilers.md#... as well as program analysis resources (in particular lattice theory, type systems and programming languages theory, related notation): https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678dd...

* Courses: I can recommend the following: https://github.com/MattPD/cpplinks/blob/master/compilers.md#...

## Online Curriculums
- IU P423/P523: Compilers (Programming Language Implementation) - Jeremy Siek, with the course book "Essentials of Compilation: An Incremental Approach" (pretty interesting approach, with programming language features developed incrementally having a fully working compiler at each step, cf. http://scheme2006.cs.uchicago.edu/11-ghuloum.pdf; implementation language Racket),

- KAIST CS420: Compiler Design - Jeehoon Kang (good modern treatment of SSA representation itself, including the use of block arguments, https://mlir.llvm.org/docs/Rationale/Rationale/#block-argume..., as well as SSA-based analysis and optimization; Rust as an implementation language),

- UCSD CSE 131: Compiler Construction - Joseph Gibbs Politz, Ranjit Jhala (great lecturers, both Haskell and OCaml edition were interesting; fun extra: one of the Fall 2019 lectures (11/26) has an interesting discussion of the trade-offs between traditional OOP and FP compiler implementation),

- UCSD CSE 231: Advanced Compiler Design - Sorin Lerner (after UCSD CSE 131: for more on analysis & optimization--data flow analysis, lattice theory, SSA, optimization; fun extra: the final Winter 2018 lecture highlighted one of my favorite papers, https://pldi15.sigplan.org/details/pldi2015-papers/31/Provab...),

- UW CSE CSEP 501: Compilers - Hal Perkins (nice balanced introduction, including x86-64 assembly code generation, with the aforementioned "Engineering a Compiler" used as the course textbook). 

- https://course.ccs.neu.edu/cs4410/

- CS 6120: Advanced Compilers: The Self-Guided Online Course
  https://www.cs.cornell.edu/courses/cs6120/2020fa/self-guided/
  
