---
title: Schedule
nav_order: 20
---

{% include toc.html %}

## Calendar

<details markdown="block">
<summary>Google Calendar</summary>
{: .text-delta }
<center>
<iframe src="https://calendar.google.com/calendar/embed?height=600&wkst=1&bgcolor=%2333B679&ctz=America%2FNew_York&src=NWY0MjhkNmM1Y2JhZTEzMTgwZTRjODRhYTRhZTU2NTJkYmYwZTE5NGYxZTYyZmUyOGI1MGE0YjQ2MzEyNDJjYUBncm91cC5jYWxlbmRhci5nb29nbGUuY29t&color=%2333B679" style="border:solid 1px #777" width="1000" height="750" frameborder="0" scrolling="no"></iframe>
</center>
</details>

The lectures and recitations are one hour long and take place at [32-124][bldg] at the following times:
- At 11 a.m. on Mondays, Wednesdays, and Fridays.
- At 12 p.m. (noon) on Tuesdays and Thursdays. (While these are listed officially as "recitations," we treat them the same as lectures.)

[bldg]: http://whereis.mit.edu/map-jpg?mapterms=32

|     | Monday | Tuesday | Wednesday | Thursday | Friday |
| :-: | :----: | :-----: | :-------: | :------: | :----: |
| 02/05 - 02/09 | _First day of classes_ <br/> [L1: Intro][lecs], [R0: Info][recs] | [L2: Regex][lecs] | [L2: Regex][lecs] | [L3: Parsing][lecs] | Phase 1 released <br/> [R1: Phase 1][recs] |
| 02/12 - 02/16 | [L4: IR][lecs] | | [L5: Semantics][lecs] <br/> [Re-lecture 1][relecs] | | [R2: Phase 1 demo][recs] |
| 02/19 - 02/23 | _Presidents' Day Holiday_ | _Monday schedule_  <br/> [L6: Codegen][lecs] | [L6: Codegen][lecs] <br/> [Re-lecture 2][relecs] | | **Phase 1 due** <br/> Phase 2 released <br/> [R3: Phase 2][recs] |
| 02/26 - 03/01 | | | **Team submission** | | [R4: x86][recs] |
| 03/04 - 03/08 | | [L6: Codegen][lecs] | [L6: Codegen][lecs] <br/> [Re-lecture 3][relecs] | [L6: Codegen][lecs] | _Add date_ <br/> **Phase 2 due** <br/> Phase 3 released <br/> [R5: Phase 3][recs] |
| 03/11 - 03/15 | | | [Quiz 1 review][reviews] | | **Quiz 1** |
| 03/18 - 03/22 | [L7: Optimization][lecs] | | [L8: Dataflow][lecs] | [L8: Dataflow][lecs] | [R6: SSA][recs] |
| 03/25 - 03/29 | _Spring Break_ | _Spring Break_ | _Spring Break_ | _Spring Break_ | _Spring Break_ |
| 04/01 - 04/05 | [L9: Loop Opt][lecs] | | [L10: Regalloc][lecs] <br/> [Re-lecture 4][relecs] | [L11: Parallel][lecs] | **Phase 3 due** <br/> Phase 4 released <br/> [R7: Phase 4][recs] |
| 04/08 - 04/12 | [L12: Foundations][lecs] | [L12: Foundations][lecs] | [L12: Foundations][lecs] | _CPW_ | _CPW_ |
| 04/15 - 04/19 | _Patriots' Day Holiday_ | | [Re-lecture 5][relecs] | | **Phase 4 due** <br/> Phase 5 released <br/> [R8: Phase 5][recs] |
| 04/22 - 04/26 | | _Drop Date_ | [Re-lecture 6][relecs] | | |
| 04/29 - 05/03 | | | [Quiz 2 review][reviews] | | **Quiz 2** |
| 05/06 - 05/10 | | | | | |
| 05/13 - 05/17 | **Phase 5 due** | _Last day of classes_ <br/> Complier Derby | | | |

[lecs]: {% link _pages/lecture-notes.md %}#lectures
[recs]: {% link _pages/lecture-notes.md %}#recitations
[relecs]: {% link _pages/lecture-notes.md %}#re-lectures
[reviews]: {% link _pages/lecture-notes.md %}#quiz-reviews

## List of topics

- Parsing
  - Regular expressions
  - Deterministic and non-deterministic finite automata
  - Context-free grammars
  - Parse trees
  - Recursive descent parser
  - Shift-reduce parsing
  - Parser construction
- Intermediate representations
  - Object-oriented programming
  - Symbol tables
  - Semantic analysis
- Unoptimized code generation
  - Control flow graph
  - Linearizing
  - Short circuiting
  - Assembly code
  - Procedure calls and stack management
  - Peephole optimizations
- Program analysis and optimizations
  - Value numbering
  - Common sub-expression elimination
  - Copy propagation
  - Constant propagation
  - Dead code elimination
  - Strength reduction
  - Algebraic simplification
- Register allocation
  - Def-use chains
  - Web-based register allocation
  - Interference graphs
  - Liveness analysis
  - Graph coloring with Chaitin's Algorithm
  - Spilling and splitting
- Parallelization
  - Data dependence analysis
  - Induction variables
- Data-flow analysis foundations
  - Order theory and lattices
  - Fixed point iteration
