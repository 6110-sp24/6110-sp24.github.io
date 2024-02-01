---
title: Syllabus
nav_order: 10
---

{% comment %}
Need to make this a standard feature for page layouts.
{% endcomment %}
<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

## Basic Information

### MIT Catalog Description

> [6.1100 Computer Language Engineering][catalog] \\
> **Prereq:** [6.1020<sub>\[6.031\]</sub>][031] and [6.1910<sub>\[6.004\]</sub>][004] \\
> **Units:** 4-4-4 \\
> **Lecture:** _MWF11_ ([32-124][bldg]) Recitation: _TR12_ ([32-124][bldg])
> 
> Analyzes issues associated with the implementation of higher-level programming languages. Fundamental concepts, functions, and structures of compilers. The interaction of theory and practice. Using tools in building software. Includes a multi-person project on compiler design and implementation.

[bldg]: http://whereis.mit.edu/map-jpg?mapterms=32
[catalog]: https://student.mit.edu/catalog/m6a.html#6.1100
[031]: https://student.mit.edu/catalog/m6a.html#6.1020
[004]: https://student.mit.edu/catalog/m6a.html#6.1910

### Recommended Texts

6.110 has no officially required textbook. All of the material you need is taught in class, with the exception of the documentation for your implementation language and associated libraries.

We can point you to many resources such as well-known textbooks, technical papers, interesting and useful blog posts, and reference guides. These are available on the [Resources]({% link _pages/resources.md %}) page.

### Communication

- We will distribute assignments here and make all announcements via [Piazza][piazza]. Important announcements will also be made via email.
  - Office hours details will be announced on Piazza.
  - Since lecture dates are not all finalized at the start of the semester, please check the schedule regularly.
- For all general questions and/or concerns, please post publicly on Piazza. If the matter is private, please post privately on [Piazza][piazza] or email the course staff at <6.110-staff@mit.edu>.

[piazza]: https://piazza.com/class/ls0no6nhtr817n

### Course Staff

#### Faculty

- [Martin Rinard](https://people.csail.mit.edu/rinard/) (<rinard@csail.mit.edu>)

#### Teaching Assistants

- Krit Boonsiriseth (<talkon@mit.edu>)
- Pleng Chomphoochan (<tcpc@mit.edu>)
- Youran Gao (<youran@mit.edu>)
- Tarushii Goel (<tarushii@mit.edu>)

Please contact the course staff by posting on [Piazza][piazza] or emailing <6.110-staff@mit.edu>.

## Course Components

We want you to succeed in this course. You should be aware of the following components of the course and utilize them for your benefit.

### Lectures

Nominally, the lectures are one hour long and take place at [32-124][bldg] at the following times:
- At 11 a.m. on Mondays, Wednesdays, and Fridays.
- At 12 p.m. (noon) on Tuesdays and Thursdays.

Lecture dates are not all finalized at the start of the semester. Some lectures may be canceled or moved depending on the class's comfort and progress on the projects. This is subject to agreement between the course staff and lecture attendees. Please check the schedule regularly. We will also announce urgent changes on [Piazza][piazza].

### Re-lectures

If you are unable to attend a lecture, please send a request for a re-lecture to 6.110-staff@mit.edu

### Compiler project

This class involves a group project, where you will build a compiler almost entirely from scratch. Details about the project can be found on the [Project Overview]({% link _pages/project-overview.md %}) page. Specific instructions for each phase of the project will be released later in the class.

### Quizzes

Two quizzes, each worth 10%, to be held during class time. See the [Schedule]({% link _pages/schedule.md %}) page for details.

### Office hours

To be announced on Piazza.


## Policies

### Grading

| Component                                                    | Weight |
| ------------------------------------------------------------ | ------ |
| Project phase 1 (lexing and parsing)                         | 5%     |
| Project phase 2 (IR and semantic checking)                   | 5%     |
| Project phase 3 (code generation)                            | 15%    |
| Project phase 4 (dataflow optimization)                      | 10%    |
| Project phase 5 (register allocation and other optimizations) <br/>and final submission | 40%    |
| Quiz 1                                                       | 10%    |
| Quiz 2                                                       | 10%    |
| Participation (weekly miniquizzes and check-in form)         | 5%     |

For more information on the way the compiler project is graded, see the [Project Overview]({% link _pages/project-overview.md %}).

### Late policy

We expect you to submit all components of the class on time. For extensions under extenuating circumstances (e.g., a member of your team is sick, family emergencies), we require a letter from one of the student deans at [Student Support Services (S<sup>3</sup>)][s3].

[s3]: https://studentlife.mit.edu/s3

### Collaboration

- You may discuss the project with anybody.
- For phase 1 (lexing and parsing) of the project, you must develop your code alone.
- For other phases of the project, you should work with your team members only. You may not develop or share any code with other teams.
- You may collaborate on weekly miniquizzes, but you should write all your solutions yourself.
- You may not post your lab or homework solutions on publicly accessible web sites or file spaces.

### LLM policy

ChatGPT/Copilot/other LLMs are capable of generating code examples for many of the tasks you will complete.

You may use code generated by LLMs as long as you disclose it in your project reports and provide us with all the prompts you used and the answers you received. ChatGPT conveniently provides a "Share link to Chat" feature for you to satisfy this requirement.
