---
title: Syllabus
layout: home
nav_order: 10
---

<script>
document.body.style.fontFamily = "Papyrus";
</script>
<marquee scrollamount="20"><h1> Computer Language Engineering (6.110) <img src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn.pixabay.com%2Fphoto%2F2016%2F09%2F01%2F08%2F24%2Fsmiley-1635449_960_720.png&f=1&nofb=1&ipt=3f856a6caebae52252680ceb1aaa0cbc517f3dc051aaaa933ab7e09b4c74fa65&ipo=images" width="100px"> </h1></marquee>
<center><img src="https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.techyv.com%2Fsites%2Fdefault%2Fusers%2Fsuperuser%2Fdepositphotos_43853639-stock-photo-word-cloud-programming-languages-or.jpg&f=1&nofb=1&ipt=e75ed663bfdf0fa575bab697d319f38feb278a176a02c0a297366047c66555cf&ipo=images" width="500px"></center>

{: .note }
> - You are _not_ expected to work over the spring break. Phase 3 deadline was chosen so you have ample time before and after spring break to work on this phase. Please make sure to prioritize your well-being!
> - There are no lectures, recitations, re-lectures, or office hours during spring break.
> - Quiz 1 has been graded and returned on Gradescope. Regrade requests are open until **April 4**.
> - You can find the quiz solutions here: [Quiz 1 solution](/assets/documents/quizzes/2024sp-exam1-key.pdf).
> - [Phase 3][phase_3] is due on **Friday, April 5.**

{% include toc.html %}

## Basic Information

### MIT Catalog Description

> [6.1100<sub>\[6.035\]</sub> Computer Language Engineering][catalog] \\
> **Prereq:** [6.1020<sub>\[6.031\]</sub>][031] and [6.1910<sub>\[6.004\]</sub>][004] \\
> **Units:** 4-4-4 \\
> **Lecture:** _MWF11_ ([32-124][bldg32]) Recitation: _TR12_ ([32-124][bldg32])
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
- Miniquizzes and weekly check-ins need to be completed via [Gradescope][gradescope]. The join code is __<u>2P4YY5</u>__.

### Recommended Texts

6.110 has no officially required textbook. All of the material you need is taught in class, with the exception of the documentation for your implementation language and associated libraries.

We can point you to many resources such as well-known textbooks, technical papers, interesting and useful blog posts, and reference guides. These are available on the [Resources][resources] page.

## Course Components

We want you to succeed in this course. You should be aware of the following components of the course and utilize them for your benefit.

### Compiler project

The main component of this course (75% of the grade) is a project where you will build a compiler almost entirely from scratch. The [first phase][phase_1] (lexing and parsing) of the project will be done individually, and the rest of the project will be done in groups of 3-4.
Details about the project can be found on the [Project Overview][project] page. Specific instructions for each phase of the project will be released later in the class.

### Class meetings

Nominally, class meetings are one hour long and take place at [32-124][bldg32] at the following times:

- At 11 a.m. on Mondays, Wednesdays, and Fridays.
- At 12 p.m. (noon) on Tuesdays and Thursdays.

_Lectures_, which will cover the fundamental concepts and structures of compilers, will be held on Mondays through Thursdays, and _recitations_, which will focus more on the project, will be held on Fridays. (Please disregard the official listing of "lectures" versus "recitations".)

 __Please check the [schedule][schedule] regularly.__ Lecture dates are not all finalized at the start of the semester. Some lectures may be canceled or moved depending on the class's comfort and progress on the projects.
 There will be weeks that have few or no lectures, especially as we draw closer to project deadlines. (Last year, there were around 7 weeks of lectures in total.) We will also announce urgent changes on [Piazza][piazza].

#### Re-lectures

If you are unable to attend a lecture, we plan to offer weekly _re-lectures_, which will cover material from the past week's lecture. Re-lectures will be at 4-6 p.m. on Wednesdays in [26-322][bldg26].

### Mini-Quizzes and Weekly Check-ins

In an effort to ensure your project stays on track, your team should submit a short weekly check-in on [Gradescope][gradescope].
In addition, for weeks with lectures, we will have a weekly "mini-quiz" on the concepts covered in lecture that week.
While these mini-quizzes will only be graded on completion, they are useful for checking your understanding of the lecture material and also serve as good preparation material for the quizzes.

### Quizzes

Two quizzes, each worth 10%, will be held during class time on __Friday, March 15__, and __Friday, May 3__.
More information about quizzes, including practice material, will be released closer to the quiz dates.
If you have a conflict with the quiz dates, please let the course staff know as early as possible.

### Office hours

- Monday 4-6 p.m. in [26-322][bldg26] (Tarushii)
- Thursday 4-6 p.m. in [26-322][bldg26] (Yoland)
- Fridays 2-7 p.m. in [26-204][bldg26] (Pleng, 2-4 p.m.; Krit, 4-7 p.m.)

## Policies

### Grading

| Component                                                    | Weight |
| ------------------------------------------------------------ | ------ |
| [Project phase 1][phase_1] (lexing and parsing)              | 5%     |
| [Project phase 2][phase_2] (IR and semantic checking)        | 5%     |
| [Project phase 3][phase_3] (code generation)                 | 15%    |
| Project phase 4 (dataflow optimization)                      | 10%    |
| Project phase 5 (register allocation and other optimizations) <br/>and final submission | 40%    |
| Quiz 1                                                       | 10%    |
| Quiz 2                                                       | 10%    |
| Participation (weekly miniquizzes and check-in form)         | 5%     |

For more information on the way the compiler project is graded, see the [Project Overview][project].

### Late policy

We expect you to submit all components of the class on time. For extensions under extenuating circumstances (e.g., a member of your team is sick, family emergencies), we require a letter from one of the student deans at [Student Support Services (S<sup>3</sup>)][s3].

### Collaboration policy

While you may discuss the high-level approaches to the project with anybody, you must develop your code within your team (or by yourself for [phase 1][phase_1] of the project). In particular:
- You _are allowed_ to use reference material available online, as well as resources and existing libraries, as long as you cite them in your project reports, and they don't trivialize the project. (Please use your best judgment here, and ask the course staff if you are unsure.) If you decide to use larger code snippets, please also explain how you adapted and used them in your project report.
- You _are allowed_ to use LLM-generated code. Make sure to read [the LLM policy](#llm-policy) below.
- You _may not_ share any code with other teams.
- You _may not_ post your project code or miniquiz solutions on publicly accessible websites or file spaces, including public GitHub repositories.

You may collaborate on weekly miniquizzes, but you should write all your solutions yourself.

### LLM policy

We encourage you to try to use LLM-generated code in your project. Your use of LLM generated code will have no effect, either positive or negative, on your grade. To cite one extreme example, if you type "Can you please generate a compiler for the MIT Decaf programming language" into the prompt box of an LLM and get a full compiler back (we have tried this and it does not seem to work), you will get full credit if the compiler satisfies the course requirements.

If you decide to use LLM-generated code, you should explain your general approach to using LLMs in your project report.
We also ask that all teams document their use of LLM generated code via a LLM code usage survey turned in three days after each project phase deadline. This survey will be made available on Gradescope.
One easy way to record your interactions with LLMs is, for example, the "Share link to Chat" feature that ChatGPT provides.

[004]: https://student.mit.edu/catalog/m6a.html#6.1910
[031]: https://student.mit.edu/catalog/m6a.html#6.1020
[bldg26]: http://whereis.mit.edu/map-jpg?mapterms=26
[bldg32]: http://whereis.mit.edu/map-jpg?mapterms=32
[catalog]: https://student.mit.edu/catalog/m6a.html#6.1100
[github]: https://github.com/6110-sp24/
[gradescope]: https://www.gradescope.com/courses/727449
[piazza]: https://piazza.com/mit/spring2024/6110/home
[s3]: https://studentlife.mit.edu/s3
[phase_1]: {% link _pages/project/phase_1.md %}
[phase_2]: {% link _pages/project/phase_2.md %}
[phase_3]: {% link _pages/project/phase_3.md %}
[quizzes]: {% link _pages/quizzes.md %}
[resources]: {% link _pages/resources.md %}
[schedule]: {% link _pages/schedule.md %}
[project]: {% link _pages/project.md %}
