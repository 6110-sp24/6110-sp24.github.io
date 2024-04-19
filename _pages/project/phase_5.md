---
title: Phase 5
parent: Compiler Project
nav_order: 6
---

In this final open-ended phase, your goal is to reduce the execution time of your generated code while maintaining correct semantics.

{: .announcement }
> There are two deliverables at the end of this phase, both of which are due at **11:59 PM on Monday, May 13**.
> 1. The final version of your Decaf compiler, which must include a working register allocator.
> 2. A [Project Design Document](#design-document) describing all components of your compiler.
>
> See the [Evaluation section](#evaluation) for details on grading.
>
> Only one submission is needed for each team --- please use Gradescope's feature to add multiple people to a single submission.

This due date is also posted on the [Class Schedule]({% link _pages/project.md %}).

{% include toc.html %}
## Overview

In this final open-ended phase, your goal is to reduce the execution time of your generated code while maintaining correct semantics. **You are required to at least implement a register allocator.**

At the end of the class (on May 14), we will hold a [Compiler Derby](#derby) where your compiler implementation will compete against the implementations of your fellow classmates on a hidden benchmark suite. A portion of your grade will be based on your compiler's performance on this benchmark suite _relative to some pre-set targets_.

The x86-64 architecture is very complex and aggressive. Part of your work in this phase is to determine which optimizations will provide a benefit given the programs of the provided benchmark suite and the target architecture. Here are some possible optimizations, in addition to the ones listed in the [Phase 4 handout]({% link _pages/project/phase_4.md %}):

1. **Register Allocation (required)** -- You can choose to implement a graph-coloring-based register allocator as taught in lecture (also see Chapter 16 of the Whale book and 9.7 of the Dragon book) or a [linear scan register allocator](https://dl.acm.org/citation.cfm?id=330250). Your register allocator should take advantage of the full set of general-purpose registers provided by the x86-64 ISA. It should also respect the Linux calling convention (e.g. caller-save/callee-save registers) when making external function calls. **This is the single optimization that is most likely to result in the largest speedup.**
2. **Instruction Selection and Scheduling** -- So far, we have been using a restricted subset of the x86-64 ISA. As a peephole optimization, you might replace a sequence of simple instructions with a single, complex instruction that performs the same operation in fewer cycles. Instruction scheduling minimizes pipeline stalls for long latency operations such as loads, multiplies, and divides. See Chapter 17 of Whale book.
3. **Data Parallelization** -- Computation executed in different iterations of a loop may be independent of each other. See the note on parallelization below.

You are also free to implement optimizations not covered in class, including optimizations that you come across in your reading or come up with on your own.
If you choose to do so, your writeup must demonstrate that each optimization is effective, semantics-preserving, and general (meaning that it is not a special-case optimization that works only for a specific application in the benchmark suite).

In addition to the course materials, we have also linked some useful resources on the [Resources page]({% link _pages/resources.md %}).

### Note on parallelization

{: .note }
Historically, parallelization is the most difficult to get right; without a good implementation and a lot of work, you might end up with a buggy compiler, or worse, generating slower assembly code. Unless you're feeling ambitious, we recommend focusing on other optimizations. **If you choose to do this, please talk to the TAs.**

The Java/Scala skeleton also includes a simple parallelization analysis library (`decaf/Parallel/Analyze.java`) to help you find parallelism in programs being compiled. The library computes the *distance vector*. For more information you can read Chapter 9.3 in the Whale book.

## Performance testing

{: .note }
The current set of benchmark programs on the autograder is not finalized yet, and benchmark programs may be added or removed.

The test cases we have provided during the previous phases are much too simple to be used as effective benchmarks for the performance of your compiler. For this phase, we will run your compiler on a benchmark suite of more complex programs simulating various real-world workloads.
Some of these programs will be released to you. (The rest will only be available on the autograder.) Your first priority is to produce correct unoptimized assembly code for each benchmark.

Once compiler produces correct unoptimized code, you should begin to study the released programs of the benchmark suite. You will use these programs to determine which optimizations to implement and in what order to apply them. You are expected to analyze the assembly code produced by your compiler to classify the effectiveness of each proposed optimization, perhaps first applying the optimization manually and empirically measuring the benefit. Your writeup should include evidence for the effectiveness of each optimization you considered **(including those of phase 4)**.

While the autograder will return some benchmark statistics about your programs, we **strongly recommend** that you set up a benchmarking framework locally. As the benchmark suite will represent a general set of real-world workloads, you are also encouraged to write your own benchmark programs.
- The simplest way to do this is to use the Unix command `time`, focusing on the `user` time, but we recommend using benchmarking tools such as [hyperfine](https://github.com/sharkdp/hyperfine). (This is also the autograder uses.)
- You can also use profilers to determine the performance of specific sections of your generated assembly code --- for example, you can provide the `-pg` option to `gcc` or `cc` while assembling in order to generate profiling information. After the code is executed, you can use `gprof` to examine the generated profile statistics.

## Derby

{: .note }
More information about the Compiler Derby will be posted later.

On the last day of class (May 14), we will run a Compiler Derby in which your group will compete against other groups to identify the compiler that produces the fastest code. The programs used in the derby will be similar to/include the ones in the benchmark suite on the autograder.

<!-- [uiCA](https://uica.uops.info) is also a useful tool for predicting the performance of specific x86 instruction sequences. -->

<!-- Midway through phase 5 (the "checkpoint"), we will start benchmarking your submissions against the derby program. Everyone's performance on the derby program will be visible through a live leaderboard on an autograder portal. Take these numbers as estimates, however; there's a 5-10% variance in the benchmarking results, and we may decide to e.g. rerun everyone's submissions on a new machine. The final results will be announced at the end of class. -->

<!-- ## Testing

We have provided sample programs that perform image processing and filtering. Pull them like before:

```bash
cd tests
git pull origin main
```

As usual, run the tests using the following command:

```bash
./tests/test.py optimizer
```

Note that these programs must be linked against the library provided in `optimizer/lib/` directory. If you're using the test script, this linking is already done for you.

You should also make sure that any valid program provided during previous phases continues to run correctly. -->


## Specifications

Your compiler's command line interface must provide an interface for turning on each optimization individually. Something similar to the following should be provided for every optimization you implement. Document the names given to each optimization not specified here.

- `-O cp` turns on copy propagation optimization only
- `-O regalloc` turns on register allocation only
- `-O cp,regalloc` turns on copy propagation optimization and register allocation only
- `-O all` **turns on "all optimizations", i.e. this is your compiler's best effort at producing the fastest generated code.**

This is the interface provided by the skeleton repositories. For the full command-line specification, see the project overview handout.

You should be able to run your compiler from the command line with:

```
./run.sh -t assembly <INPUT FILE> -o <OUTPUT FILE>          # no optimizations
./run.sh -t assembly -O all <INPUT FILE> -o <OUTPUT FILE>   # all optimizations
```

Your compiler should then write a x86-64 assembly listing to standard output, or to the file specified by the `-o` argument.

## Design Document

In this phase you will also write a design document that explains the technical details of your overall compiler implementation, including work done in previous phases. (You may reuse the relevant sections from your previous design documents.)

As per the [main Project page][design-doc], the design document should include the following sections.

1. **Design:** An overview of your design, an analysis of design alternatives you considered, and key design decisions. This section should help us understand your code, convince us that it is sufficiently general, and let us know anything that might not be reflected in your code. **In addition to summaries of various design aspects from previous phases, you must also include the following information relevant to Phase 5:**
   1. A detailed discussion of your `-O all` option, including which optimizations are performed, which order they are performed in, how many times they are performed, and how you arrived at this choice.
   2. Details of each optimization you implemented, including:
      - a brief explanation of how your optimization worked (this should convince your reader that the optimization was beneficial, general, and correct)
      - a sample test case, with generated code before and after, under `doc/phase5-code/` in your repository.
      - if possible, include empirical evidence that proves the effectiveness of your optimization.
2. **Extras:** A list of any clarifications, assumptions, or additions to the problem assigned. This includes any interesting debugging techniques/logging, additional build scripts, or approved libraries used in designing the compiler.
3. **Difficulties:** A list of known problems with your project, and as much as you know about the cause. If there are any test cases that you failed from previous phases that you fixed in this phase, you should also include this information in the write up.
4. **Contribution:** A brief description of how your group divided the work. This will not affect your grade; it will be used to alert the TAs to any possible problems.

In addition, if you used LLMs when working on the project, you should also describe how you used them and provide us with chat logs (if possible) in your design document.

## Evaluation

Your final submission at the end of this phase is worth 40% of the overall grade in this class, divided as follows:
- **10%:** Your work specifically in Phase 5, including implementing a working register allocator along with relevant discussion in your [design document](#design-document) (§1a, §1b).
- **30%:** Your overall work on the compiler project, including:
  - **5%:** Your overall design document, including summaries of previous phases in the Design section (§1) as well as the Extras, Difficulties, and Contribution sections (§2--4).
  - **15%:** The correctness of your final Decaf compiler, both without optimizations and with optimizations enabled (`-O all`). This includes correctness on all the previously released test cases (available either at the [`6110-sp24/public-tests` repository](https://github.com/6110-sp24/public-tests) or the [`6110-sp24/private-tests` repository](https://github.com/6110-sp24/private-tests)) as well as on the Derby benchmark suite.
  - **10%:** The performance of your final Decaf compiler on the Derby benchmark suite.

## Submission

### Design Document

Please submit your design document as a PDF in the [Phase 5 Report assignment](https://www.gradescope.com/courses/727449/assignments/4381734) on Gradescope, and remember to add your team members to the submission.

{: .note }
Please also include both the design document _and_ your sample test case under the `doc` subdirectory in your team GitHub repository.

### Code

Please submit your phase 5 code on Gradescope via GitHub, following the steps below:

1. Push your code to your team GitHub repository (`6110-sp24/<TEAM NAME>`). We suggest making a separate branch for the submission, say, `phase5-submission`.
2. Go to the [Phase 5 assignment](https://www.gradescope.com/courses/727449/assignments/4380508) on Gradescope, and select your GitHub repository and branch.
3. Add your team members to the submission on Gradescope.

Submitted repositories should have the following structure:
```txt
<repo name>
├── build.sh
├── run.sh
├── doc/
│   ├── phase5.pdf    # phase 5 design document
│   └── phase5-code/  # phase 5 sample test case
└── ...
```

{: .warning }
Make sure the `./build.sh` and `./run.sh` scripts are located at the **root** of your repository, otherwise the autograder will fail.

[design-doc]: {% link _pages/project.md %}#project-design-document