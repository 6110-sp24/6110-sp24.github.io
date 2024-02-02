---
title: Resources
nav_order: 40
---

This section contains a number of useful and/or interesting references selected by the staff. You are not expected to know most of the material on this page for the class; however, you may find it interesting and helpful.

## References

You will find those references useful in writing your compiler.

1. The complete [Intel x64 manual](https://www.intel.com/content/www/us/en/developer/articles/technical/intel-sdm.html) --- official PDFs with all the gory details
1. [x86 and amd64 instruction reference](https://www.felixcloutier.com/x86/) --- navigable reference by Félix Cloutier derived from the Intel manual
1. [x86 wiki](https://en.wikibooks.org/wiki/X86_Assembly/X86_Instructions) --- good primer on how x86 instructions work
1. [x64 cheat sheet](https://cs.brown.edu/courses/cs033/docs/guides/x64_cheatsheet.pdf) -- lists and tables detailing registers and assembly commands from Brown University's CS033

If you find interesting resources you think other students could benefit from, please consider sharing them on Piazza!


## Recommended textbooks

There is no required textbook for this class, but if you insist, we think this is a good reference textbook to have:

1. **Cooper, Keith D., and Torczon, Linda, _Engineering a Compiler_, 3rd ed., Morgan Kaufmann, 2022.**
  - A new reference textbook for understanding modern compilers. Covers many optimizations seen in this course (e.g. data-flow, instruction scheduling, register allocation) plus a few advanced ones found in modern compilers (e.g. [static single-assignment (SSA)][ssa]).

Other textbooks you may be interested in:

{:style="counter-reset:step-counter 1"}
1. **Robert Nystrom, [_Crafting Interpreters_](https://craftinginterpreters.com/), Genever Benning, 2021.**
  - Our default recommendation for people who want to learn about compilers in general (i.e. outside of this course).
  - This is an _amazing_ introduction to implementing a parser, an interpreter, and a bytecode virtual machine in Java and C.
  - The section on parsers may be useful for phase 1 of the project.
  - The rest of the book is arguably more relevant to 6.1120<sub>\[6.818\]</sub> Dynamic Computer Language Engineering.
1. **A. W. Appel and J. Palsberg, [_Modern Compiler Implementation in Java_][appel-java], Cambridge University Press, 2002.**
  - A classic book. Guides you through a compiler project with thoughtful code organization. Otherwise similar to _Cooper et al._ in content.
  - Also has a C version and ML version.
1. **Aho, Alfred V., et al. _Compilers: Principles, Techniques, & Tools_, 2nd ed., Pearson Addison-Wesley, 2007.**
  - A very, very, thick, classic reference on writing an optimizing compiler for C-like languages (e.g. Decaf).
  - Also called "the dragon book." Everyone has heard of this.
1. **Steven Muchnick, _Advanced Compiler Design and Implementation_, Morgan Kaufmann, 1997.**
  - Comprehensive coverage of advanced compiler optimizations.

Many of those textbooks are [available online through MIT Libraries][mitlib]. (For some books, you can borrow physical copies!) You can purchase those textbooks through traditional means (e.g. Amazon) or ask the TAs for advices on acquiring the textbooks.

[appel-java]: https://www.cs.princeton.edu/~appel/modern/java/
[ssa]: https://en.wikipedia.org/wiki/Static_single-assignment_form
[mitlib]: https://libraries.mit.edu/

## Other interesting blog posts, papers, etc.

1. Overviews
    1. [LLVM compiler architecture](http://www.aosabook.org/en/llvm.html)
    1. [GCC compiler architecture](http://en.wikibooks.org/wiki/GNU_C_Compiler_Internals/GNU_C_Compiler_Architecture)
1. Blogs
    1. [Russ Cox's Blog](http://research.swtch.com/) -- Russ is one of the developers of Google Go, a pretty interesting language.
    1. [Ian Wienand's Blog](http://www.technovelty.org/) -- Whoever he is, he writes about compiler and language internals, the magic black box that is the linker, and more
    1. [Matt Might's Blog](http://matt.might.net/articles/) -- Matt is a professor at the University of Utah and has written some very interesting articles (e.g. "Yacc is dead")
1. Papers
    1. [Register Allocation & Spilling via Graph Coloring](http://dl.acm.org/citation.cfm?id=806984) -- G.J. Chaitin / 1982. Great (short) paper on simple register allocation.
    1. [Linear Scan Register Allocation](https://dl.acm.org/citation.cfm?id=330250)
    1. [Iterated Register Coalescing](http://dl.acm.org/citation.cfm?id=229546) -- Lal George / 1996. Presents improvements/alternative to Chaitin's design. If Chaitin-style (+/-Briggs) register allocation isn't enough for you, this paper is a good read - actually, it's a good read anyway, to understand the tradeoffs
    1. [Superword Level Parallelism](http://dl.acm.org/citation.cfm?id=358438) combined with loop unrolling, a simple way to implement a vectorizing compiler
1. Miscellaneous
    1. [Carnegie Mellon's 15-411 Compiler Design course](https://www.cs.cmu.edu/~janh/courses/411/23/schedule.html)
    1. [Harvard's CS153 Compilers class](https://groups.seas.harvard.edu/courses/cs153/2019fa/schedule.html)
    1. [Cornell's self-guided, online Advanced Compilers course](https://www.cs.cornell.edu/courses/cs6120/2020fa/self-guided/)
    1. [Scala Patterns for Compiler Design](https://gist.github.com/rcoh/4992969)
    1. [Lecture notes from 6.5900<sub>\[6.823\]</sub> Advanced Computer Architecture](http://csg.csail.mit.edu/6.823)
    1. [The Missing Semester of Your CS Education](https://missing.csail.mit.edu/2020/)

