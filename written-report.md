---
title: Written Report \break
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
challenge students' logic and creativity practically. For example, in the lesson
on fixed-point binary numbers, I was able to quickly craft a Ruby script that
functioned as a quiz ([Appendix I][Appendix I: `fixed_point.rb`]), giving the
user randomly-generated fixed-point binary numbers, each one byte long. This
worked as follows:

1. Generate a random byte
2. Insert a fixed point somewhere in the byte, and base the maximum power of $2$
   in the number off this - e.g. for $1110.0000$, the position of the fixed
   point is after index $3$, and the greatest value bit would be worth $2^3$.
3. Calculate the value of the fixed-point binary number by iterating through and
   reducing the power of $2$ each time

If this were given to the students as a task instead of worksheets with similar
questions, I feel that the students' understanding would improve as a result. I
made similar strides to support students' learning in this way with
demonstrations of uses of arrays ([Appendix II][Appendix II:
`noughts-and-crosses.rb`]) and queues ([Appendix III][Appendix III: `Queue`]).
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
unfamiliar people and scenarios, helped me move towards confidence. In
particular, teaching small parts of lessons without preparation helped me test
and extend the limits of my comfort zone.

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

## Appendix I: `fixed_point.rb`

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

## Appendix II: `noughts-and-crosses.rb`

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

## Appendix III: `Queue`

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
