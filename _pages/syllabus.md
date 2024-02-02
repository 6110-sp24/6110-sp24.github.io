---
title: Syllabus
layout: home
nav_order: 10
---

<h1> Welcome to Computer Language Engineering (6.110) </h1>

{: .warning }
⚠️ This website is still under active development. If you are taking the class, please note that the information currently on this website may not be completely accurate while this notice is up. ⚠️

{% include toc.html %}

## Basic Information

### MIT Catalog Description

> [6.1100<sub>\[6.035\]</sub> Computer Language Engineering][catalog] \\
> **Prereq:** [6.1020<sub>\[6.031\]</sub>][031] and [6.1910<sub>\[6.004\]</sub>][004] \\
> **Units:** 4-4-4 \\
> **Lecture:** _MWF11_ ([32-124][bldg]) Recitation: _TR12_ ([32-124][bldg])
>
> Analyzes issues associated with the implementation of higher-level programming languages. Fundamental concepts, functions, and structures of compilers. The interaction of theory and practice. Using tools in building software. Includes a multi-person project on compiler design and implementation.

### Course Staff

#### Faculty

- [Martin Rinard](https://people.csail.mit.edu/rinard/) (<rinard@csail.mit.edu>)

#### Teaching Assistants

- Krit Boonsiriseth (<talkon@mit.edu>)
- Pleng Chomphoochan (<tcpc@mit.edu>)
- Youran (Yoland) Gao (<youran@mit.edu>)
- Tarushii Goel (<tarushii@mit.edu>)

Please contact the course staff by posting on [Piazza][piazza] or emailing <6.110-staff@mit.edu>.

### Communication

- We will distribute assignments here and make all announcements via [Piazza][piazza]. Important announcements will also be made via email.
  - Office hours details will be announced on [Piazza][piazza].
  - Since lecture dates are not all finalized at the start of the semester, please check the [schedule][schedule] regularly.
- For all general questions and/or concerns, please post publicly on [Piazza][piazza]. If the matter is private, please post privately on [Piazza][piazza] or email the course staff at <6.110-staff@mit.edu>.
- Miniquizzes and status reports need to be completed via [Gradescope][gradescope]. The join code is __<u>2P4YY5</u>__.

### Recommended Texts

6.110 has no officially required textbook. All of the material you need is taught in class, with the exception of the documentation for your implementation language and associated libraries.

We can point you to many resources such as well-known textbooks, technical papers, interesting and useful blog posts, and reference guides. These are available on the [Resources][resources] page.

## Course Components

We want you to succeed in this course. You should be aware of the following components of the course and utilize them for your benefit.

### Compiler project

The main component of this course (75% of the grade) is a group project where you will build a compiler almost entirely from scratch. Details about the project can be found on the [Project Overview][project] page. Specific instructions for each phase of the project will be released later in the class.

### Lectures

Nominally, the lectures are one hour long and take place at [32-124][bldg] at the following times:

- At 11 a.m. on Mondays, Wednesdays, and Fridays.
- At 12 p.m. (noon) on Tuesdays and Thursdays. (While these are listed officially as "recitations," we treat them the same as lectures.)

 __Please check the [schedule][schedule] regularly.__ Lecture dates are not all finalized at the start of the semester. Some lectures may be canceled or moved depending on the class's comfort and progress on the projects. There are often weeks that do not have any lectures. (Last year, there were around 7 weeks of lectures in total.) We will also announce urgent changes on [Piazza][piazza].

#### Re-lectures

If you are unable to attend a lecture, please send a request for a re-lecture to <6.110-staff@mit.edu>. The course staff plans to give one re-lecture per one week of lecture.

### Mini-Quizzes and Weekly Check-ins

In an effort to ensure your project stays on track, your team should submit a short weekly check-in on [Gradescope][gradescope]. In addition, we will have a weekly "mini-quiz" graded for completion credit on the concepts covered in lecture that week. We believe these mini-quizzes will be useful to check your understanding of the material as well as good quiz preparation.

### Quizzes

Two quizzes, each worth 10%, will be held during class time on the days listed on the [Schedule][schedule] page. More information about quizzes will be released closer to the quiz dates.

### Office hours

To be announced on [Piazza][piazza].


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

For more information on the way the compiler project is graded, see the [Project Overview][project].

### Late policy

We expect you to submit all components of the class on time. For extensions under extenuating circumstances (e.g., a member of your team is sick, family emergencies), we require a letter from one of the student deans at [Student Support Services (S<sup>3</sup>)][s3].


### Collaboration

- You may discuss the project with anybody.
- For phase 1 (lexing and parsing) of the project, you must develop your code alone.
- For other phases of the project, you should work with your team members only. You may not develop or share any code with other teams.
- You may collaborate on weekly miniquizzes, but you should write all your solutions yourself.
- You may not post your lab or homework solutions on publicly accessible web sites or file spaces.

### LLM policy

ChatGPT/Copilot/other LLMs are capable of generating code examples for many of the tasks you will complete.

You may use code generated by LLMs as long as you disclose it in your project reports and provide us with all the prompts you used and the answers you received. ChatGPT conveniently provides a "Share link to Chat" feature for you to satisfy this requirement.


[bldg]: http://whereis.mit.edu/map-jpg?mapterms=32
[catalog]: https://student.mit.edu/catalog/m6a.html#6.1100
[031]: https://student.mit.edu/catalog/m6a.html#6.1020
[004]: https://student.mit.edu/catalog/m6a.html#6.1910
[gradescope]: https://www.gradescope.com/courses/727449 
[piazza]: https://piazza.com/class/ls0no6nhtr817n
[s3]: https://studentlife.mit.edu/s3
[resources]: {% link _pages/resources.md %}
[schedule]: {% link _pages/schedule.md %}
[project]: {% link _pages/project.md %}