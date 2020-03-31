# Report

<!--
You might find the following guideline helpful (this is not mandatory but should
be good starting point in most cases):

Introduction, context about the school (500 words) Reflection on observation
visits to the school (500 words) Thoughts about your experiences in the school,
challenges you faced, things you learned, skills you developed (or wanted to
develop and didn’t have time!) (1500 words) Conclusions (500 words)
-->

## Introduction

The satisfaction of learning and understanding new concepts is universal.
Pursuit of this drives my decisions and my passions - each challenge is a new
chance to grow. I enjoy sharing this satisfaction with others by passing on my
skills. This is why I chose to take this module.

Though I am unlikely to take up teaching as my first job, I wish to improve my
confidence and interpersonal skills through a variety of experience. Previously,
I have volunteered as an instructor and assistant for Code First: Girls, and I
have also taken to teaching coding to my 7-year-old brother at home in the wake
of the coronavirus pandemic. I also presented during work experience at UKCloud
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
a skill that would grant them more control over the process.

<!-- TODO: cite their website -->

## Observation Visits

I visited the school on <!-- TODO: -->  separate occasions. Over the course of
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
consecutive lessons, whereas they would focus on the Year 7 class.

Much of my confidence in the classroom was dictated by the environment. For
example, during my visit on the 22nd of January, I was assisting with a Year 7
class doing a practical task guiding Sphero robots around a maze. I was able to
freely wander the room and help students that raised their hands.

Conversely, in my first lesson with Nick's Year 12 class, the students were
given time to work on their Python projects in silence, and gave little if any
indication that they needed help. Nick is friendly with the class and knows them
well, whereas I shared the sentiment with many other ambassadors that it's hard
to know where to draw the line in acquainting oneself with students.

Though I followed Nick's guidence to talk to the students about their projects,
I did not feel that doing so helped me to build the rapport I wanted to achieve
with them. I expressed to Nick and Maya that I would like to make some input
during lessons, even if this meant demonstrating a concept ad-hoc. The thought
of signing up for this was daunting at first, as I was admittedly nervous -
perhaps my Asperger's Syndrome has some small part to play in my need for
preparation to perform off the cuff - but the satisfaction of doing so was what
I wanted from this module.

I took up the challenge during my visits in March, in which I demonstrated a few
different concepts. The first of these was fixed-point binary number, which Nick
suggested I take care of. I had not received any indication that I was to take a
role in teaching before this point, but i stepped up nonetheless. I explained
the concept by taking the class back to the foundations of how bases work - each
digit of a binary number is the sum of *x* x 2^*y* for each bit, where *x* is
the value at the given bit and *y* is the position of the bit. For example:

```
110

1 x 2^2 =  4
1 x 2^1 =  2
0 x 2^0 =  0
         ---
           6
```

I showed that fixed-point binary numbers extend this pattern, with numbers
beyond the point using negative powers. Nick took my demonstration in stride and
commented that I had done a good job. I was able to quickly conjure up a
spreadsheet that could be used as a calculator for fixed-point decimals, which
was used to verify answers. I raised the exercise as a suggestion for something
students could work on in their own time to test their understanding of the
topic.

Another topic I was able to demonstrate was the purpose of the BIOS. Maya taught
the lesson by reading from the course textbook, which students had to copy. I
was able to interject and suggest that I could show the students the UEFI on my
laptop, since the BIOS was believed to be locked down on the school PCs. I told
the class of how I had used the BIOS in practical situations, such as modifying
the boot order when dual-booting Linux with Windows or updating the firmware for
compatibility with newer CPUs. I felt that this would introduce some necessary
real-world context to the lesson.

Following that success, I expressed to Maya that I would be very happy to talk
about open source software on my next visit, in line with the topic of types of
system software (e.g. proprietary, custom-made, open/closed source), I talked
about a few different elements of open source software using examples I
recalled. These included:

- its regular use in both daily life and industry scenarios (referencing
  Linux/Android, Visual Studio Code, Inkscape and more)
- securities and vulnerabilities granted by the open source model (user
  auditing, social engineering attacks), and
- ownership of code ([forking](https://github.com/Airblader/i3),
  [passing on the maintainer's mantle](https://github.com/michael-lazar/rtv/issues/696))

While I hesitated to go into particular detail on `git` under the assumption
that I would teach it through my special project, I would have liked to show
them the pull requests I have personally submitted as a way to express to the
students that contributing to open source is worth the attempt, daunting though
it may seem.

## My Experience

<!-- Thoughts about your experiences in the school -->

- course is often taught by rote and content isn't particularly stimulating,
  understandable that as it's a day job it's difficult to make every lesson
  crazy interactive, but it could be a lot better
- would it be possible to move a lot of exercises to building stuff that can
  solve the problem, as opposed to just solving a ton of the same problem?
- interesting that there's a reliance on worksheets with the same questions, as
  opposed to a bunch of random questions - I whipped up generators pretty easily
  in class
- very good school with well-behaved classes, would welcome the opportunity to
  return

<!-- challenges you faced -->

- becoming comfortable with the environment
- having to forge my own role

<!-- things you learned -->

- they're bright kids, their inspiration needs tapping into and channeling in
  the right ways! the current curriculum doesn't quite get this right

<!-- skills you developed (or wanted to develop and didn’t have time!)  -->

- confidence
- ability to explain concepts in a simple way
- 

## Conclusions