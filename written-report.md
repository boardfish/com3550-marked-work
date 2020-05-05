---
title: Report \break
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

# Introduction

The satisfaction of learning and understanding new concepts is universal.
Pursuit of this drives my decisions and my passions - each challenge is a new
chance to grow. I enjoy sharing this satisfaction with others by passing on my
skills. This is why I chose to take this module.

Though I am unlikely to take up teaching as my first job, I wish to improve my
confidence and interpersonal skills through a variety of experience. Previously,
I have volunteered as an instructor and assistant for Code First: Girls, and I
have also taken to teaching coding to my 7-year-old brother at home in the wake
of the COVID-19 pandemic. I also presented during work experience at UKCloud
last year in a variety of circumstances, whether demonstrating my team's work to
other departments during sprint reviews or coaching new developers on using
Docker.

I was chosen, along with another student, to volunteer at King Ecgbert School in
the nearby village of Dore. King Ecgbert is a school and sixth form that tutors
around 1350 students, of which the sixth form accounts for around 350 students.
IT and Computer Science tutoring is primarily covered by two teachers. For
purposes of anonymity, I will refer to them as Maya and Nick.

Our original contact in the school was Maya. Maya explained to us that she was
originally from a business studies teaching background, but had been teaching
computer science for around four years. Our help was important to her
particularly around tougher concepts such as big O notation. She expressed
interest in different and more interactive styles of teaching.

In my discussions with Maya on initial observations and visits, we decided that
my role in the classroom would be dictated by my special project's target
audience. I came to the conclusion that this would be a class of Year 12
students. Nick's class of Year 12 students were working on a software
development project. To teach them how to use `git`, I thought, would bring them
a skill that would grant them more control over their software development
process.

<!-- TODO: cite their website -->

# Observation Visits

I visited the school on seven separate occasions. Over the course of
these visits, I was able to gather confidence and was eventually able to present
some concepts to the class ad-hoc. If not for the pandemic, I would have begun
to move forward with my special project, with hopes of leading lessons
afterwards, but I am personally happy with the progress I was able to make.

Initially, I visited alongside the other chosen ambassador for the school. This
was so that Maya could establish what we would both be doing for our special
projects. We observed lessons and used Maya's free periods to discuss the
special project and what needed to be done to make it happen. This is discussed
in more detail in the special project report.

Once we had established our roles, the other ambassador and I began to meet with
Maya on different schedules. I would aim to be around for the Year 12 group's
consecutive lessons with her and Nick, whereas they would focus on the Year 7
class.

Much of my confidence in the classroom was dictated by the environment I worked
in. During my visit on the 22nd of January, I was assisting with a
Year 7 class doing a practical task guiding Sphero robots around a maze. I was
able to freely wander the room and help students that raised their hands.

Conversely, in my first lesson with Nick's Year 12 class, the students were
given time to work on their Python projects in silence, and gave little if any
indication that they needed help. Nick was friendly with the class and knew them
well, whereas I had some difficulty in approaching them. I shared the sentiment
with other ambassadors that it is hard to know where to draw the line in
acquainting oneself with students - I imagine that it is something that comes
with experience.

Though I followed Nick's guidance to talk to the students about their projects,
I did not feel that doing so helped me to build the rapport I wanted to achieve
with them. I expressed to Nick and Maya that I would like to make some input
during lessons, even if this meant demonstrating a concept ad-hoc. I felt that
if I was able to lead them and teach them, both I and they would feel more
comfortable in discussion together. Nick suggested in one lesson that I lead
off-the-cuff - without any prior preparation. The thought of signing up for this
was daunting at first, but the satisfaction of doing so was what I wanted from
this module.

I took up the challenge during my visits in March, in which I demonstrated a few
different concepts. The first of these was fixed-point binary numbers. I had not
received any indication that I was to take a role in teaching before this point,
but i stepped up nonetheless. I explained the concept by taking the class back
to the foundations of how bases work - each digit of a binary number is the sum
of $x \times 2^y$ for each bit, where *x* is the value at the given bit and *y* is
the position of the bit. For example:

\begin{center}
\begin{math}
\begin{array}{lcl}
110 \\
\\
  & 1 \times 2^2 & = 4 \\  
+ & 1 \times 2^1 & = 2 \\  
+ & 0 \times 2^0 & = 0 \\  
  &         & = 6 \\  
\end{array}
\end{math}
\end{center}

I showed that fixed-point binary numbers extend this pattern, with $y$
continuing to decrease by $1$ for each digit. Nick took my demonstration in
stride and commented that I had done a good job. I was able to quickly conjure
up a spreadsheet that could be used as a calculator for fixed-point decimals,
which was used to verify answers. I raised the exercise as a suggestion for
something students could work on in their own time to test their understanding
of the topic.

Another topic I was able to demonstrate was the purpose of the BIOS. Maya taught
the lesson by reading from the course textbook, which students had to copy. I
was able to interject and suggest that I could show the students the UEFI on my
laptop, since the BIOS was believed to be locked down on the school PCs. I told
the class of how I had used the BIOS in practical situations, such as modifying
the boot order when dual-booting Linux with Windows or updating the firmware for
compatibility with newer CPUs. I felt that this would introduce some necessary
real-world context to the lesson and increase students' familiarity with the
practical purpose of the BIOS in doing so.

Following that success, I expressed to Maya that I would be very happy to talk
about open source software on my next visit, in line with the topic of types of
system software (e.g. proprietary, custom-made, open/closed source), I talked
about a few different elements of open source software using examples I
recalled. These included:

- its regular use in both daily life and industry scenarios (referencing
  Linux/Android, Visual Studio Code, Inkscape and more)
- securities and vulnerabilities granted by the open source model (user
  auditing, social engineering attacks), and
- ownership of code in the community, particularly referring to
  [forking](https://github.com/Airblader/i3) and [passing on the maintainer's
  mantle](https://github.com/michael-lazar/rtv/issues/696)

While I hesitated to go into particular detail on `git` under the assumption
that I would teach it through my special project, I would have liked to show
them the pull requests I have personally submitted. This could have expressed to
the students that contributing to open source is worth the attempt, daunting
though it may seem, and that no contribution is too small.

# My Experience

## Observations

I found that some lessons were taught by reading from the course textbook, which
the students would then type up to add to their own notes. This style of
teaching ranks low on the pyramid of retention, and seemed suboptimal to me.
However, I understand why it is employed - to craft one's own resources and try
to make every lesson as interactive as possible would be another job in itself.
Given the opportunity, I would have liked to change this by using my role to
introduce more interactive means of learning, as I did with the UEFI
demonstration.

Another realisation I had was that rote could be replaced with exercises that
challenge students' logic and creativity practically. For example, in the lesson on
fixed-point binary numbers, I was able to quickly craft a Ruby script that
functioned as a quiz, giving the user randomly-generated fixed-point binary
numbers, each one byte long. This worked as follows:

1. Generate a random byte
2. Insert a fixed point somewhere in the byte, and base the maximum power of $2$
   in the number off this - e.g. for $1110.0000$, the position of the fixed
   point is after index $3$, and the greatest value bit would be worth $2^3$.
3. Calculate the value of the fixed-point binary number by iterating through and
   reducing the power of $2$ each time

If this were given to the students as a task instead of worksheets with similar
questions, I feel that the students' understanding would improve as a result.
Understanding of the topic is not always reflected by the ability to answer
repeat questions. Instead, understanding may be better tested by seeing if the
students can express the algorithm in a different form - i.e. code. This style
of learning may not be suitable for KS3, however, as it is reliant on
programming ability - at that lower level, students may be too unfamiliar with
programming. @letrud2012rebuttal states that the more powerful forms of
learning, such as this more practical angle, "have made several major
contributions to our grasp of different subject matters". However, they also
warn that such methods can be "overemphasized".

The continued use of worksheets with similar questions interests me. Online
platforms for education such as MyMaths and Times Tables Rock Stars bring
opportunities for staff to evaluate students' progress and investment in
learning, and could be reflected in computer science with tools such as Repl.it
or GitHub Classroom. The pandemic also highlights the importance of remotely
available tools such as these.

I see potential for platforms like these to grow. However, teachers who already
find it difficult to teach computer science may have some trouble creating
assignments with automated marking through test suites. The pandemic signals the
fast arrival of a future where educational institutions might come to rely on
online platforms like these, which could mean a major change both for teachers
and students in how they experience lessons.

In spite of my idealism and the potential for change, I am impressed by the
behaviour of the students and the quality of teaching at King Ecgbert School. I
would welcome the opportunity to return.

## Challenges

My primary challenge at King Ecgbert School was becoming comfortable with the
environment. When I applied to take the module, I felt confident that I would
begin to feel comfortable enough in the school to lead lessons. I knew, however,
that this would take some time, and that I would need to build a good working
relationship with not just the staff, but the students.

When the pandemic hit, I felt as though I was approaching that point, having
already taken several small opportunities to lead parts of lessons. Though Nick
persuaded me before this to try and immerse myself in the class and ask students
what they were working on, I thought that by establishing my role as one who
teaches, I might have better luck conversing normally with the students.

This scenario reflected another of my challenges fairly well. I did not feel as
though I was given a particular framework for my role, and had to forge it
myself. At first, I found this quite difficult to navigate, but a combination of
things helped me to feel a bit more comfortable.

Firstly, the opportunity I took to show the UEFI on my laptop gave me a moment
to speak and have the class's full attention, and I felt able to discuss more
with Maya about this afterwards. This led to my section on open source software
in the next lesson with her. 

Secondly, when Nick encouraged me to teach fixed-point binary numbers without
any prior preparation, I once again had the chance to teach. Admittedly, I was
nervous in the moment, but I managed to explain the concept in a way that
allowed the lesson to carry on as normal and helped the class to understand it
effectively. Had my time at the school not been cut short by the pandemic, I
feel that by this point, I had set myself up to take my role in stride and more
confidently assist in class.

## Lessons

I was pleasantly surprised to see that the students had some strong inspiration
and passion for their projects. Particularly, I was interested to see one
developing an Engima simulation machine - a friend I met on my year in industry
reported that he once did something of this nature for an assignment at
university, and the machine is also the topic of an assignment I face in another
module at the time of writing. Cases like this suggest to me that students at
this level desire to be challenged with stimulating tasks, and wish to learn
practically.

## Skill Development

In taking this module, I sought to improve my confidence and ability to explain
concepts in a simple way. I took opportunities to exercise both. These are
skills I have made strides to train in various ways throughout my life - on a
personal level, I am still trying to discover what it means and what it takes to
be confident in any situation. This experience, which confronted me with many
unfamiliar people and scenarios, helped me move towards confidence.

# Conclusions

In conclusion, I have really enjoyed being able to pass on knowledge and give
back as part of this module. I feel that it has given me time to exercise
valuable skills and think about the current and future direction of computer
science education. Going into teaching is still unlikely to be my first career
choice, but the scope for improvement of teaching and inspiration for students
is vast.

A more practical direction is something I have longed for as a student, all the
way from GCSE level to degree level. Whether this bias is a good bias to hold is
something I was not able to find decisive proof on during my time at King
Ecgbert School, but it continues to dictate my approach to teaching. Regardless
of rebuttals to the validity of the NTL Learning Pyramid model, I would hope
that my practical approach to teaching would support learning in it current
form.

# References

::: {#refs}
:::

\backmatter

# Appendices

\pagebreak

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

## Appendix II: `fixed_point.rb`

```ruby
# redo this for two's complement?

def generate_binary_number
  Array.new(8) { [0, 1].sample }
end

def generate_binary_number_question
  binary_number = generate_binary_number.join
  [binary_number, binary_number.to_i(2)]
end

def generate_fixed_point_binary_number_question
  max_power = (4..7).to_a.sample
  binary_number = generate_binary_number
  iterator = max_power + 1
  answer = binary_number.map do |binary_value|
    iterator -= 1
    binary_value * (2 ** iterator)
  end.sum

  binary_number.insert(max_power + 1, '.')
  [binary_number.join, answer.to_f]
end

def quiz(questions_answers)
  correct_count = 0
  questions_answers.each do |question, answer|
    puts "#{question}: "
    choice = gets.chomp.to_f
    if choice == answer
        correct_count += 1 
        puts "correct!"
    end
  end
end

def binary_number_quiz
  questions_answers = Array.new(10) { generate_binary_number_question }
  quiz(questions_answers)
end

def fixed_point_binary_number_quiz
  questions_answers = Array.new(10) { generate_fixed_point_binary_number_question }
  quiz(questions_answers)
end

fixed_point_binary_number_quiz
```

## Appendix III: `noughts-and-crosses.rb`

This is a quick implementation of the game *Noughts and Crosses*. It does not
check for a winner - it only checks if the board is completely full. My main
intent when writing it was to demonstrate to the class how arrays can be
interacted with.

```ruby
def empty_board
    [
        [nil, nil, nil],
        [nil, nil, nil],
        [nil, nil, nil]
    ]
end

def current_piece
    @osTurn ? 'O' : 'X'
end

def place_piece(board, x, y)
    if board[y][x]
        return [false, board]
    end
    board[y][x] = current_piece
    return [true, board]
end

def print_board(board)
    iter = 1
    board.each_with_index do |row|
        row.each do |square|
            print "#{square ? square : iter} "
            iter += 1
        end
        puts
    end
end

def translateXY(input)
    y = input / 3
    x = input % 3
    return [x, y]
end

def take_turn(board)
    x, y = translateXY(gets.chomp.to_i - 1)
    okay, board = place_piece(board, x, y)
    @osTurn = !@osTurn if okay
    [okay, board]
end

@osTurn = false
board = empty_board
while (!board.flatten.any? nil) do
    _, board = take_turn(board)
    print_board(board)
end
```

## Appendix IV: `Queue`

`queue.py`

```python
class Queue:
    def __init__(self, array):
        self.queue = array

    def front(self):
        return self.queue[0]
    
    def rear(self):
        return self.queue[-1]
    
    def enqueue(self, item):
        self.queue.append(item)
    
    def dequeue(self):
        front = self.front()
        self.queue = self.queue[1:-1]
        return front
    
    def is_empty(self):
        return len(self.queue) == 0
```

`queuetests.py`

Note: I did not write tests for `Queue#dequeue` during the lesson, but manually
verified that it worked as intended.

```python
import unittest
from queue import Queue

class TestQueue(unittest.TestCase):

    def setUp(self):
        pass

    def test_front(self):
        self.assertEqual(Queue([1,2,3]).front(), 1)
        self.assertEqual(Queue([2,1,3]).front(), 2)
        self.assertEqual(Queue([3,1,2]).front(), 3)
    
    def test_enqueue(self):
        queue = Queue([1,2,3])
        queue.enqueue(4)
        self.assertEqual(queue.rear(), 4)

    def test_is_empty(self):
        queue = Queue([])
        self.assertEqual(queue.is_empty(), True)
        queue.enqueue(4)
        self.assertEqual(queue.is_empty(), False)


if __name__ == '__main__':
    unittest.main()
```

## Appendix V: Special Project Closing Survey

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