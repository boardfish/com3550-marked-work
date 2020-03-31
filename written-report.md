# Report

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

### Observations

I found that some lessons were taught by reading from the course textbook, which
the students would then type up to add to their own notes. This style of
teaching ranks low on the pyramid of retention, and seemed suboptimal to me.
However, i understand why it is employed - to craft resources and try to make
every lesson as interactive as possible would be another job in itself. Given
the opportunity, I would have liked to change this by using my role to introduce
more interactive means of learning, as I did with the UEFI demonstration.

Another realisation I had was that exercises based on repetition might not be as
effective as developing software to answer those exercises. For example, in the
lesson on fixed-point binary numbers, I was able to quickly craft a Ruby script
that functioned as a quiz, giving the user randomly-generated fixed-point binary
numbers, each one byte long. This worked as follows:

1. Make a random byte
2. insert a fixed point somewhere in the byte, and base the maximum power of 2 in
  the number off this - e.g. for 1110.0000, the position of the fixed point is
  after index 3, and the greatest value bit would be worth 2^3.
3. calculate the value of the fixed-point binary number by iterating through and
  reducing the power of 2 each time

If this were given to the students as a task instead of worksheets with similar
questions, I feel that the students' understanding would improve as a result.
This style of learning may not be suitable for KS3, however, as it is reliant on
programming ability - at that lower level, there is a disparity in skill between
students.

The continued use of worksheets with similar questions interests me. Online
platforms for education such as MyMaths and Times Tables Rock Stars bring
opportunities for staff to evaluate students' progress and investment in
learning. The pandemic also highlights the importance of remotely available
tools such as these.

I see potential for platforms like these to grow, and particularly in the case
of fixed-point binary numbers, I found it quite easy to create a generator to
provide students with questions. Of course, developing scalable online platforms
for hundreds of thousands of students to use is not an easy task by any stretch
of the imagination, but the pandemic signals the fast arrival of a future where
educational institutions might come to rely on them.

In spite of this idealism and the potential for change, I am impressed by the
behaviour of the students and the quality of teaching at King Ecgbert School. I
would welcome the opportunity to return.

### Challenges

My primary challenge at King Ecgbert School was becoming comfortable with the
environment. When I applied to take the module, I felt confident that I would
begin to feel comfortable enough in the school to lead lessons. I knew, however,
that this would take some time, and that I would need to build a good working
relationship with not just the staff, but the students.

When the pandemic hit, I felt as though I was approaching that point, having
already taken several small opportunities to lead parts of lessons. Though Nick
persuaded me before this to try and immerse myself in the class and ask students
what they were working on, I thought that by establishing my role as a teaching
assistant, I would gain familiarity with the class.

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
confidently assist the class.

### Lessons

I was pleasantly surprised to see that the students had some strong inspiration
and passion for their projects. Particularly, I was interested to see one
developing an Engima simulation machine - a friend I met on my year in industry
reported that he once did something of this nature for an assignment at
university. Cases like this suggest to me that students at this level desire to
be challenged with stimulating tasks, and wish to learn practically.

### Skill Development

In taking this module, I sought to improve my confidence and ability to explain
concepts in a simple way. I took opportunities to exercise both. These are
skills I have made strides to train in various ways throughout my life - on a
personal level, I am still trying to discover what it means and what it takes to
be confident in any situation. This experience, which confronted me with many
unfamiliar people and scenarios, helped me move towards confidence.

## Conclusions

In conclusion, I have really enjoyed being able to pass on knowledge and give
back as part of this module. I feel that it has given me time to exercise
valuable skills and think about the current and future direction of computer
science education. Going into teaching is still unlikely to be my first career
choice, but the scope for improvement of teaching and inspiration for students
is vast.

A more practical direction is someting I have longed for as a student, all the
way from GCSE level to degree level. Whether this bias is a good bias to hold is
something I was not able to find decisive proof on during my time at King
Ecgbert School, but it continues to dictate my approach to teaching. Regardless
of rebuttals to the validity of the NTL Learning Pyramid model, I would hope
that my practical approach to teaching would support learning in it current form
- @letrud2012rebuttal states that the more powerful forms of learning "have made
several major contributions to our grasp of different subject matters", though
they warn that such methods can be "overemphasized".

```
@article{letrud2012rebuttal,
  title={A Rebuttal Of NTL Instituteʼs Learning Pyramid},
  author={Letrud, K{\aa}re},
  journal={Education},
  volume={133},
  number={1},
  year={2012}
}
```