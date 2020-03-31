# Special Project Report

<!--

1500 words. This will describe the content, methods, reasoning,
planning, delivery and reception of the project. If appropriate, it will also
include sample material e.g. worksheets prepared by the student, or feedback
returns.

Comment. This is the tricky one, because most of you will not have delivered
your special project in the school. You should focus on explaining the reasoning
for the intervention, referring to the educational literature where possible,
and on the methods used and planning.
-->

For my special project, I chose to teach the students how to use `git`, a
version control tool that is widely used in the software development industry
and beyond. `git` is a cause that is close to my heart; since starting
university, it has been one of the tools I have used the most. I am encouraged
to teach others what I wished to know when I was at their level of experience -
Git immediately struck me as that topic.

For purposes of anonymity, I will refer to my primary contacts in the school as
Maya and Nick.

## Reasoning

One of the first reasons that struck me for teaching `git` was that it is useful
independent of context. I am using `git` as I write this report, and as I make
changes to the text content, I will have a full history of when things were
written and why they were written the way they were. When plaintext formats are
used, `git` can be effective in this way for all sorts of work - presentations,
reports, and more. Even if students would not wish to take their computer
science qualification further, `git` would still be a valuable tool.

Upon explaining the topic to Maya, I realised that another strength of teaching
`git` would be to change how computer science is taught in schools
fundamentally. I was well aware that as an ambassador, I could only do so much.
However, ideally, if I could demonstrate the power and the benefits of online
tools such as GitHub Classroom, perhaps I could leave a more lasting impact. If
I could teach not only students but staff about the strength of `git`, teaching
at the school could advance in a major way.

When I was told that the Year 12 class was working on projects, I came to
realise that teaching `git` was perhaps more of a necessity than a desire.
Currently, it is tough for me to imagine abandoning version control. `git`, when
used correctly, makes it easier to test code, safely make edits, revert, and
figure out the source of an issue or bug. Especially in the absence of a test
suite, writing code against a bare filesystem without any version control sounds
like a potentially uncomfortable experience.

`git` is explained in many different ways, from many different angles, by many
different parties. Fortunately, this means that documentation on it is very
strong. However, I have seen a general dissatisfaction among teachers and
students of `git` alike around how `git` is taught. I saw this as an opportunity
to craft my own resources, potentially with the goal of making the source freely
available.

`git` has enabled me to do many things - collaborating effectively at hackathons
and in group projects, and managing my personal projects more sustainably, to
name a couple. Many freely available tools integrate with it; `git` serves as a
good platform to deployment services like Netlify and Heroku, and continuous
integration tools like CircleCI and GitHub Actions. `git` has been the key to a
number of software development tools for me personally.

One of the most important things `git` has enabled me to do is to contribute to
open source. I have met my pull request goals during the past two Hacktoberfest
events, and in doing so, I have enhanced projects I personally use, such as
[ZDog](https://github.com/metafizzy/zdog),
[Spectacle](https://github.com/formidable-labs/spectacle),
and [Faker](https://github.com/stympy/faker). This has always been a goal of
mine, but making the first step to contribute to those repositories has been a
daunting concept. I hoped that in teaching `git` and showing my work, I could
encourage others to make the first step at a much younger age than I did and
potentially get a headstart on their peers in making themselves presentable to
employers.

## Content

My first intent was to focus on creating commits by introducing the concepts of
staging and committing. First, I'd explain the concepts, and I would then allow the
students to briefly try it out through a sequence of commands like:

```
git init
touch readme.md
echo "# Hello\!" >> readme.md
git add readme.md
git commit
git log
```

They'd be able to intersperse these commands with `git status` to see how their
actions affect the stage.

I'd also briefly discuss other `git` features such as pushing to and pulling
from remotes, branching, cloning, and bisecting. A variety of tools are backed
by `git` and `git` repositories, such as Netlify and CircleCI. I would raise
these as examples of how learning `git` is a platform for upping your presence
and abilities as a developer.

The exercise also demonstrates the strength of test-driven development, though a
demonstration of continuous integration servers would be subject to
implementation. 

## Methods

My aim was to teach the students `git` by way of a short presentation. This
would present the concept of `git`, making sure not to get too rooted in
context, while quickly communicating the benefits of its use. I would then
explain the flow of how to use `git` - going from editing and saving to staging,
committing and pushing. To end the demonstration, I would go through the use of
`git` in whichever environment we were to use, and allow students to briefly do
the same as previously explained.

Students would then be tasked with a sample of test-driven development - they
would need to write a Python class `GetBirthDay` that could return which day it
was upon a given date, as a number between 0 and 6 inclusive. For example,
`GetBirthDay(8, 4, 2020)` would return `2` (Wednesday). They would need to do
this without using date/time-related libraries, but they would have a
pre-written test suite that tested the output of their code against a variety of
scenarios.

The first part of the exercise would be to make it function for dates within the
current year. In my implementation, this involved summing the number of days in
each month up to the given month, adding the days since the start of the month,
taking modulo 7 of the result, and adding the day on which January 1st fell as
an offset. I felt that this would provide an ample degree of coding challenge
without distracting too far from the `git` aspect.

The second part of the exercise would be to make it function for dates in any
year, which for me involved figuring out whether a given year was a leap year
and incorporating this in recalculation of the offset.

## Planning

Plans changed in a variety of ways, eventually leading to cancellation due to
the pandemic. Originally, I established that it would be difficult and
sub-optimal to encourage the school's IT department to install `git` tools on
school PCs, upon advice from both Maya and my module tutor.

My first solution to navigate the problem was to investigate taking out
Raspberry Pi computers on loan from the university. Students would have been
given a command line environment and access to a text editor (or potentially
IDE, depending on the capacity of the Pi computers). From there, they would be
able to write their code, run the test suite, and commit it. I also investigated
hosting a Jenkins and Git server using Docker, so that students would be able to
have the tests run against a continuous integration environment. This would
bring the lesson closer to an emulation of industry software development.

This would have needed microSD cards for each board, a prebuilt system image
with Git server credentials and Jenkins credentials for each user, and display
adapters for each device. Thankfully, I managed to remind myself of a better
idea before going too far with this - online IDEs like Repl.it and Codio would
have still allowed students to interface with Git and their code, without
creating an overwhelming dependency on additional hardware. Before the pandemic
hit, I was able to make progress with Maya on enrolling the school for Repl.it.