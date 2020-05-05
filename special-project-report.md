---
title: Special Project Report \break
  \large COM3550 Undergraduate Ambassador Ambassadors Scheme in Computer Science
subtitle: 
author: |
  Simon Fish
geometry: left=37mm,right=25mm,top=25mm,bottom=25mm
papersize: a4
links-as-notes: true
bibliography: [bibliography.bib]
link-citations: true
table-of-contents: true
documentclass: report
header-includes: |
  \usepackage{lscape}
  \newcommand{\blandscape}{\begin{landscape}}
  \newcommand{\elandscape}{\end{landscape}}
  \usepackage{fancyhdr,ragged2e}
  \fancyhead{}
  \fancyhead[CO,CE]{\leftmark}
  \pagestyle{fancy}
---
\makeatletter

\newcommand\frontmatter{%
    \cleardoublepage
  %\@mainmatterfalse
  \pagenumbering{roman}}

\newcommand\mainmatter{%
    \cleardoublepage
 % \@mainmattertrue
  \pagenumbering{arabic}}

\newcommand\backmatter{%
  \if@openright
    \cleardoublepage
  \else
    \clearpage
  \fi
 % \@mainmatterfalse
   }
\makeatother
\frontmatter
\tableofcontents
\mainmatter

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

# Introduction

For my special project, I chose to teach a group of Year 12 students how to use
`git`, a version control tool that is widely used in the software development
industry and beyond. Since starting university, `git` has been one of the tools
I have used the most. I am encouraged to teach others what I wished to know when
I was at their level of experience - `git` immediately struck me as that topic
when considering what to take on in this project.

`git` is a version control tool that tracks changes to files between what it
calls 'commits'. Commits show the state of tracked files at a particular point
in development, and have messages attached to explain changes that were made
since the last commit. Some benefits of `git` include the ability to work
asynchronously and have conflicting changes resolved safely through the use of
branches, and `git`'s log of commits, which can come to represent a timeline of
development.

For purposes of anonymity, I will refer to my primary contacts at King Ecgbert
School as Maya and Nick.

# Reasoning

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
However, I thought that if I could demonstrate the power and the benefits of
`git` and automated testing, perhaps I could leave a more lasting
impact. `git`, whether in the hands of students or teachers, could improve and
reform ways of working across the school.

When I was told that the Year 12 class was working on projects, I came to
realise that teaching `git` was perhaps more of a necessity of theirs than a
desire of mine. Currently, it is tough for me to imagine abandoning version
control. `git`, when used correctly, makes it easier to test code, safely make
edits, revert, and figure out the source of an issue or bug. Especially in the
absence of a test suite, writing code against a bare filesystem without any
version control increases the risk that a bug may be introduced and makes it
more difficult to understand how it might have arisen.

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

# Content

My first intent was to focus on creating commits by introducing the concepts of
staging and committing. I would also briefly discuss other `git` features such
as pushing to and pulling from remotes, branching, cloning, and bisecting. A
variety of tools are backed by `git` and `git` repositories, such as Netlify and
CircleCI. I would raise these as examples of how learning `git` is a platform
for increasing one's online presence and abilities as a developer.

The exercise also demonstrates the strength of test-driven development, though a
demonstration of continuous integration servers would be subject to
implementation. Instead of testing their code manually, students would be given
a test suite ([Appendix II][Appendix II: Special Project Test Suite]) which
their code would be run against.

# Methods

I would teach the students `git` by way of a short presentation. This would
present the concept of `git`, making sure not to get too rooted in context,
while quickly communicating the benefits of its use. I would then explain the
flow of how to use `git` - going from editing and saving to staging, committing
and pushing. To end the demonstration, I would go through the use of `git` in
whichever environment we were to use, and allow students to briefly do the same
as previously explained.

In the terminal, demonstration could be done through a sequence of commands such
as:

```
git init
touch readme.md
echo "# Hello\!" >> readme.md
git add readme.md
git commit
git log
```

These commands could be interspersed with `git status` to see how
their actions had affected the stage.

Students would then be tasked with a sample of test-driven development - they
would need to write a Python class `GetBirthDay` that could return which day it
was upon a given date, as a number between 0 and 6 inclusive. For example,
`GetBirthDay(8, 4, 2020)` would return `2` (Wednesday). They would need to do
this without using date/time-related libraries, but they would have a
pre-written test suite ([Appendix II][Appendix II: Special Project Test Suite])
that tested the output of their code against a variety of scenarios. While
completing this exercise, they would be encouraged to make a commit after
completing a feature - a good landmark at which to make a commit would be after
having made another test pass. The task sheet ([Appendix I][Appendix I: Special
Project Task Sheet]) would be their guide in this task, but they would be
permitted to ask for further help.

The first part of the exercise would be to make it function for dates within the
current year. In my implementation, this involved summing the number of days in
each month up to the given month, adding the days since the start of the month,
taking modulo 7 of the result, and adding the day on which January 1st fell as
an offset. I felt that this would provide an ample degree of coding challenge
without distracting too far from the `git` aspect.

The second part of the exercise would be to make it function for dates in any
year. In my implementation, I needed to extend my solution to know whether a
given year was a leap year. This would be incorporated in recalculation of the
aforementioned January 1st offset - knowing which day a year starts on and
whether it is a leap year are the keys to determining which day it is on any
given date.

# Planning

Plans changed in a variety of ways, eventually leading to cancellation due to
the pandemic. Originally, I established that it would be difficult and
sub-optimal to encourage the school's IT department to install `git` tools on
school PCs, upon advice from both Maya and my module tutor.

My first resolution was to investigate taking out Raspberry Pi computers on loan
from the university. Students would have been given a command line environment
and access to a text editor (or potentially IDE, depending on the capacity of
the Pi computers). From there, they would be able to write their code, run the
test suite, and commit it. I also investigated hosting a Jenkins and Git server
using Docker, so that students would be able to have the tests run against a
continuous integration environment. This would bring the lesson closer to an
emulation of industry software development.

This would have needed microSD cards for each board, a prebuilt system image
with Git server credentials and Jenkins credentials for each user, and display
adapters for each device. Thankfully, I managed to remind myself of a better
idea before going too far with this - online IDEs like Repl.it and Codio would
have still allowed students to interface with Git and their code, without
creating an overwhelming dependency on additional hardware. Before the pandemic
hit, I was able to make progress with Maya on enrolling the school for Repl.it.

\backmatter

# Appendices

## Appendix I: Special Project Task Sheet

### Your challenge

Let's apply what we've learned about `git`, and combine it with something new. We're going to do some
**test-driven development**.

In the software development industry, it's common practice to not just write code, but write *tested* code - use a test
framework such as Python's `unittest` to make sure your work meets all the requirements. Fortunately for you, I've
written the tests for you already! You'll just need to make them green.

You'll also want to **commit** as you go along - if you hit a small milestone or get a new test passing, that's your cue
to commit. Did you *raise an error if the date is outside the month limit*? Did you
*write and test a new function to see whether a given year is a leap year?* Those are good changes worth documenting and
committing.

#### Part 1 - What day is it?

Do you know what day of the week your birthday falls on this year? Well, you're about to write something that'll help
you figure it out!

Write your code in `getbirthday.py`, but if you want to see how well it does against the tests, run `tests.py`.
You should aim to get the tests in `tests.py` to pass. 

##### What we're working with - a class

A class is a type of object that you can build yourself, then initialise. If your class has an `__init__` method (known
as an **initialiser**), you can initialise it by calling `YourClassName()`. In our case, we're making a class called
`GetBirthday`, which we're passing a `day`, `month` and `year`. So we can call it like `GetBirthday(8, 4, 2020)`, for
example.

The `__init__` method should also be responsible for checking if what's passed in is valid. If it's passed an invalid date (like the 30th of February), it should `raise ValueError`.

`GetBirthDay` should have a method `day_index`, which returns the day of the week (0-indexed!) that the date in
your instance falls on. For example, my birthday falls on a Wednesday, so `2` should be returned:

```python
>>> GetBirthDay(8, 4, 2020).day_index()
2
```

Focus on making sure things work for dates in **2020 only** to start with, and don't forget to **commit** to save your
progress.

Expect output like this after running `python tests.py -v`:

```
test_errors_if_dates_outside_feb_limits (__main__.TestGetBirthDay) ... skipped 'Delete this line for the extension task'
test_errors_if_dates_outside_month_limits (__main__.TestGetBirthDay) ... ok
test_errors_if_year_outside_limits (__main__.TestGetBirthDay) ... ok
test_important_dates (__main__.TestGetBirthDay) ... skipped 'Delete this line for the extension task'
test_important_dates_this_year (__main__.TestGetBirthDay) ... ok
test_outputs_within_limits (__main__.TestGetBirthDay) ... ok

----------------------------------------------------------------------
Ran 6 tests in 0.001s

OK (skipped=2)
```

The tests check that:

- `errors_if_dates_outside_month_limits`: Dates outside the limits of each month (e.g. 31st April, 32nd January) raise `ValueError`
- `errors_if_year_outside_limits`: Dates outside more general limits (0/1/2020, 1/13/2020, 1/1/-1) raise `ValueError`
- `important_dates_this_year`: A few dates this year, just to check that your class is returning the right days consistently
- `outputs_within_limits`: Only number between 0-6 inclusive are returned

##### Tips, if you're stuck on the algorithm

- This year starts on a Wednesday (`2`). Might want to bear that in mind!
- March 3rd might be the 3rd day of March...but which day of the *year* is it?
- The modulo operator (`%`) is good for wrapping numbers within a range. It's normally used for checking if numbers are
  even (`x % 2 == 0`), but where might you use it here?

#### Part 2 - What day *was* it?

If you manage to get the tests passing, remove the lines starting with `@unittest.skip(...)` to reveal another set of
tests. These will push you to get the program working for **different years**, so you can have a look at some other
dates from across history. Pay particular attention to **leap years**!

The tests check that:

- `important_dates`: More important dates from across the years
- `errors_if_dates_outside_feb_limit`: This year is a leap year, so the 29th of February happened. In other years,
  though, that might not be the case...

##### Tips

- This year starts on a Wednesday (`2`)...but what did last year start on? Or the year before? There's a pattern here...
- Leap years are divisible by 4, but multiples of 100 aren't leap years unless they're *also* divisible by 400. 

---

### Recap - `git gud`: Learning to use `git`, a version control tool

#### What is `git`?

`git` is one of the most widely-used tools in the software development industry,
but it's applicable just about anywhere else, both inside and outside the field
of computer science. It's a **version control** tool - you can keep track of
different versions of your code, whether they're full releases or just a
one-line fix. `git` has a variety of benefits, such as:

- pinpointing where something broke in your code
- enabling collaboration with others, using branches
- allowing you to more easily back up your code and work offline

Whatever your use for it, every **commit** you make in `git` tells a story -
decisions that were made, ways in which things were implemented, and even some
mishaps. It's a bit like writing a diary and taking a timelapse of your code at the same time!

#### How to use `git`

##### Committing

**Commits** are the string that ties `git` together. They're **snapshots** of 
the code at some point in time, with a message attached to detail what changed. Let's look at how to make a commit.

When you edit a file normally, the process looks like this:

1. Edit the file.
2. Save the file.

`git` gives you a few more things you need to do afterwards:

3. **Stage** your changes.
4. **Commit**.

You might also then **push**. But what does all this mean?

###### Staging files

If you **stage** a file, you add the changes you've made to the file onto the **stage**. When you then **commit**, all changes on the stage are included in that commit.

To stage a file, use the `git add` command. `git add <filename>` stages the file(s) you give it. 

You might also stage a file by accident - perhaps there's a file with some passwords in that you only use on your device? Remove files from the stage (without changing or deleting them) with `git reset <filename>`.

To get an idea of what's been staged and what hasn't, use `git status`. `git status` reports back like this:

```
On branch readme
Your branch is up-to-date with 'origin/readme'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        file_not_committed_yet

no changes added to commit (use "git add" and/or "git commit -a")
```

- `README.md` is a file that I've committed before. `git` knows it exists, but I've made changes to it that I haven't
  committed yet.
- `file_not_committed_yet` is a file that I've never added to a commit before. `git` isn't **tracking** this file - it
  doesn't know it exists yet.

If I run `git add README.md`, it'll show up like this:

```
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   README.md
```

This means my changes to `README.md` are staged, but if I edit the file and save it again, any further changes I make
will need to be staged again.

**Shortcuts**

Often you'll just want to stage everything you've changed, but sometimes you'll want to be more picky about it. So if you want to:

- add everything, even files you haven't committed before, to the stage: `git add -A`
- add only files you've changed to the stage: `git add -p`

###### Committing

Then, all that's left to do is to `git commit` and supply a descriptive message about the changes you've just made, such as "Write section about staging files". And after that, it's time to `git push` your code over to whichever server you're keeping it on and synchronise your changes.

Let's have a look at how commits show up in `git log`:

```
commit c6813f8f4805d752b7480c585c3cda669b576365
Author: Simon Fish <si@mon.fish>
Date:   Mon Mar 2 14:44:49 2020 +0000

    Write tests for various dates, skip years tests at first
    
    Students can delete the skip lines to enable those tests if they get
    that far. I'll write another block of tests for important dates for 2020
    only.
```

So, what have we got here?

The long hex string at the top is a **commit hash**. It might seem totally random, but it's actually
[a lot of information about the commit encoded with SHA-1](https://gist.github.com/masak/2415865). Okay, you didn't need
to know that part...but what you *do* need to know if that if you want to know what the code looked like at that point
in time, you'd do this:

```
git checkout c6813f
```

Think to yourself "hey, let's **check out** what the code looked like at this point in time" - "this point in time"
being the commit hash.

There are also details of when the commit was made and who the commit was made by. The message is really important -
commit early and often so that you can summarise things quickly on the first line. You can use the rest of the message
space, if you wish, to document anything you think is particularly important to know in the future.

##### Collaborating with others

This isn't something there'll be an exercise on, but it's good to have a little context on. `git` is great for working
with others, but why wouldn't you code in Google Docs, say? Because everyone edits at the same time, and with code, that
could have some nasty side effects. It's got its uses, which is why editor features exist to let you do that if you
wish, but typically, various different people will work on various different features across a huge codebase, and any
overlaps will need to be resolved. That's why `git` has **branches**.

Branches allow you to, well, 'branch off' from any commit and make some changes, whatever the reason may be - a feature,
a fix, a refactor. You can then **merge** this branch back into the one you branched off, and combine the changes you
made with anything that happened since you branched off. If you edited some of the same lines as other people, `git`
will show you both and allow you to **resolve conflicts** so that the merge finishes smoothly.

##### Making code publicly available

There are a lot of `git` providers online - **GitHub** might be the most familiar to you. Others include **BitBucket**
and **GitLab**, but it's also possible to host your own `git` server using free or proprietary software. Free options
include **Gitea** and **GitLab CE**, but the three main providers also offer their services to enterprise.

## Appendix II: Special Project Test Suite

`tests.py`

```python
import unittest
from getbirthday import GetBirthDay


class TestGetBirthDay(unittest.TestCase):

    def setUp(self):
        pass

    def output_under_upper_limit(self, gbd_instance, upperLimit):
        self.assertLess(gbd_instance.day_index(), upperLimit)

    def output_over_lower_limit(self, gbd_instance, lowerLimit):
        self.assertGreater(gbd_instance.day_index(), lowerLimit)

    # =======================
    # Months
    # =======================

    def test_errors_if_year_outside_limits(self):
        self.assertRaises(ValueError, lambda: GetBirthDay(-1, 1, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(1, -1, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(1, -1, -1))
        self.assertRaises(ValueError, lambda: GetBirthDay(32, 1, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(1, 13, 2020))

    def test_errors_if_dates_outside_month_limits(self):
        self.assertRaises(ValueError, lambda: GetBirthDay(32, 1, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(30, 2, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(32, 3, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(31, 4, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(32, 5, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(31, 6, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(32, 7, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(32, 8, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(31, 9, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(32, 10, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(31, 11, 2020))
        self.assertRaises(ValueError, lambda: GetBirthDay(32, 12, 2020))

    def test_outputs_within_limits(self):
        for x in range(1, 31):
            gbd = GetBirthDay(x, 1, 2020)
            self.output_over_lower_limit(gbd, -1)
            self.output_under_upper_limit(gbd, 7)

    def test_important_dates_this_year(self):
        # My birthday
        self.assertEqual(GetBirthDay(8, 4, 2020).day_index(), 2)
        # Christmas this year
        self.assertEqual(GetBirthDay(25, 12, 2020).day_index(), 4)
        # Super Smash Bros. Ultimate's second anniversary
        self.assertEqual(GetBirthDay(6, 12, 2020).day_index(), 6)
        # The 2020 Olympics begin
        self.assertEqual(GetBirthDay(24, 7, 2020).day_index(), 4)

    # ==========================
    # Years
    # ==========================

    # Leap year specific tests
    @unittest.skip("Delete this line for the extension task")
    def test_errors_if_dates_outside_feb_limits(self):
        # divisible by 4
        self.assertIsInstance(GetBirthDay(29, 2, 2020), GetBirthDay)
        # divisible by 100 but not 400
        self.assertRaises(ValueError, lambda: GetBirthDay(30, 2, 1900))
        # divisible by 400
        self.assertIsInstance(GetBirthDay(29, 2, 2000), GetBirthDay)

    @unittest.skip("Delete this line for the extension task")
    def test_important_dates(self):
        # My birthday
        self.assertEqual(GetBirthDay(8, 4, 1998).day_index(), 2)
        # Super Smash Bros. Ultimate's release date
        self.assertEqual(GetBirthDay(6, 12, 2018).day_index(), 3)
        # Satoru Iwata's birthday
        self.assertEqual(GetBirthDay(6, 12, 1959).day_index(), 6)
        # Kamen Rider's first airdate
        self.assertEqual(GetBirthDay(3, 4, 1971).day_index(), 5)


if __name__ == '__main__':
    unittest.main()

```

## Appendix III: Original Jenkins CI server concept

Please see https://github.com/boardfish/call_jenkins_builds_from_ruby.

The original proof of concept for interacting with the Jenkins API from Ruby was
something I developed during my year in industry. I authored commits
`86fc0b2815f21ce610b22a2376fd1e979e4b9e9d` and
`fa94a9369a443b131db25eae41510d909b272438` to get this closer to working for my
special project. I was also able to add an instance of
[Gitea](https://gitea.io/en-us/) to the `docker-compose` environment, but I have
lost records of this work.

Additional work included deployment and seeding of users and repositories on
Jenkins and Gitea. My vision for these is detailed below.

Jenkins and Gitea would have been hosted alongside an
[`nginx-proxy`](https://github.com/nginx-proxy/nginx-proxy) container, which
would have exposed the frontend to the class. The `docker-compose` environment
comprising these three containers would be running on a VM hosted with
DigitalOcean. Students would access Jenkins and Gitea through their domain
names. They would be able to log in and see their code run against the
development server as it had been pushed. 

Admittedly, this may not have been the most secure deployment - I investigated
use of Docker secrets and maintaining SSL through the stack, but this proved
difficult. If my knowledge of platforms such as Kubernetes were stronger, I
might have been able to develop this while holding security as a priority more
easily.

Seeding would have been done using requests to Jenkins and Gitea's APIs. I would
provide a script with the number of users required, and the script would
authenticate with both APIs. These items would be created for each user:

- A Gitea account
- A Jenkins account
- A repository on Gitea against their account, containing the `README` <!-- TODO:
  Appendix I -->, test suite, and `Jenkinsfile` that dictates how the test suite
  should be run on Jenkins.

## Appendix IV: Special Project Closing Survey

### Exposure to and understanding of `git`

Select the statement that applies to you. Before the lesson, you...   
*Option select answer*

- Did not know that `git` existed
- Had heard of `git`
- Had used `git` previously

How would you describe your understanding of the purpose of `git`?   
*Option select answer*

- I do not understand why people use `git`
- I am not very confident in my understanding of why people use `git`
- I feel like I have a good understanding of why people use `git`
- I am fully confident in my understanding of why people use `git`

### Practical use of `git`

How would you describe your confidence in using `git` during the lesson?   
*Option select answer*

- I do not understand how to use `git`
- I am not very confident when using `git`
- I feel like I have a good understanding of how to use `git`
- I am fully confident in my ability to use `git`

Before the lesson, had you encountered testing frameworks (such as Python's
unittest)?   
*Option select answer*

- I had already written a test suite
- I was aware of testing frameworks
- I was not aware of testing frameworks

How comfortable would you be in applying `git` to work you do...   
*Matrix answer*

Rows:

- ...alone (e.g. assignments)?
- ...in open source software?
- ...with a group that doesn't yet know how to use `git`?
- ...with a group that knows how to use `git`?

Columns:

- Uncomfortable
- Not very comfortable
- Neither comfortable nor uncomfortable
- Somewhat comfortable
- Comfortable

What is your opinion of open source software?   
*Option select answer*

- Positive
- Neutral/apathetic
- Negative
- Conflicted
- I don't understand the concept of open source software

How do/did you feel about contributing to open source using `git`...  
*Matrix answer*

Rows:

- ...before the lesson?
- ...after the lesson?

Columns:

- Apathetic about it
- Not at all comfortable
- Not very comfortable
- Neither comfortable nor uncomfortable
- Somewhat comfortable
- Comfortable
- Motivated to do so