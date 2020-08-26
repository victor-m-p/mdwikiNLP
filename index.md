Natural Language Processing
============
Cognitive Science Msc | Semester 1 | Fall 2020 

Overview 
---------------------

|           | When?         | Where? | Who?                      |
|-----------|---------------|--------|---------------------------|
| Lectures  | Fri 8-10   | ONLINE/1441 - 110  | Rebekah Baglini           |
| Classroom | Wed 8-10 | 1252 - 204  | Kenneth Enevoldsen |


The course addresses how we can approach theoretical and applied topics in human cognition using computational linguistics and natural language processing tools. The course also addresses key ethical topics that arise from the analysis of freely available natural language data, and in the development of natural language processing software and technologies. 
This course builds on students’ background knowledge in statistics and statistical programming, and introduces students to working with large data sets. The course builds towards the data science course. The course introduces students to ethical and philosophical topics, which will be extended on in the data science course. The course prepares students for careers involving analysis of text and other forms of natural language data, and for careers involving development of natural language software. 

   
See the [course catalog](https://kursuskatalog.au.dk/en/course/101106/Natural-language-processing) for more information. 


Schedule 
---------------------


| Week | Prepare                           | Classroom (Weds)       | Live lecture (Fri)      | Assignment (Fri 8am)   |
|------|-----------------------------------|------------------------|-------------------------|------------------------|
| 36   | [Read/Watch](class1.md)           | Computer set-up        | Introduction            | Intro survey           |
| 37   | [Read/Watch](class2.md)           |                        | Text processing         | PS 1                   |
| 38   | [Read/Watch](class3.md)           |                        | Language modeling       | PS 2                   |
| 39   | [Read/Watch](class4.md)           |                        | Classification          | PS 3                   |
| 40   | [Read/Watch](class5.md)           |                        | Classification II       |                        |
| 41   | [Read/Watch](class6.md)           |                        | Information retrieval   | PS 4                   |
| 42   | [Read/Watch](class_break.md)      | BREAK                  | BREAK                   | BREAK                  |
| 43   | [Read/Watch](class7.md)           | Word2Vec               | Vector semantics        | Project pitch   |
| 44   | [Read/Watch](class8.md)           | Topic modeling         | NER/Relation extraction | PS 5  |
| 45   | [Read/Watch](class9.md)           | Data wrangling         | NLP in CogSci research         |                        |
| 46   | [Read/Watch](class10.md)          | Model design           | Ethics in NLP           | Data/pipeline report   |
| 47   | [Read/Watch](class11.md)          | Supervision            | NLP in industry         | Ethics statement       |
| 48   | [Read/Watch](class12.md)          | Evaluation/validation  | Supervision             |                        |
| 49   | [Poster instructions](posters.md) | Poster session 1       | Poster session 2        |                        |

Readings and resources 
---------------------

**Textbook chapters for Weds lectures**
[Speech and Language Processing](https://web.stanford.edu/~jurafsky/slp3/) (3rd ed. draft) by Dan Jurafsky and James H. Martin. 

**Supplementary Python textbook for Thurs classroom session**: 
[Natural Language Processing with Python](https://www.nltk.org/book/) by Steven Bird, Ewan Klein, and Edward Loper. 

### Jupyter notebooks

**For classroom group exercises**:
[The hands-on NLTK tutorial for NLP in Python](https://github.com/hb20007/hands-on-nltk-tutorial) 

**For self-paced Python learning**:
[leriomaggio's Collection of Jupyter Notebooks about Python programming](https://github.com/leriomaggio/python-in-a-notebook)


Learning to program 
---------------

Note: You are expected to bring a laptop to every lecture and class. Please make sure to install [Anaconda](www.anaconda.com) before our first meeting. 

This class will involve lots of hands-on implementation in Python. We will start off very gently, but note that this is *not* an introduction to Python programming class - i.e. you will not be formally instructed on matters like "what makes Python an object-oriented programming language?" and "when should one use a list versus a tuple?", nor will you be penalized for inelegant coding solutions. If the code accomplishes what it's supposed to, that's what matters. 

### Basic elements of Python 

In order to complete the classroom group work and coding assignments, it will help to have a basic understanding of the following: 

+ variables and variable assignment
+ strings, numbers (intergers and floats), basic arithmetic operations
+ lists, sets, tuples, dictionaries 
+ simple input and output
+ conditional (if) statements
+ while and for loops 
+ functions and classes 

By "basic understanding" I mean that you have a grasp of what these different elements do and how they differ from one another. (See also **What does is mean to learn programming?** below.) 

Although can certainly learn these 'as-you-go' during the class, I highly recommend preparing doing a few hours of Python self-paced study in advance. Below is a list of five small programming tasks to help you assess your level of Python proficiency. 

---------------------------------------
### Self-assessment test for Python programming readiness:

**Task 1: Adding machine**

Write a function that adds two numbers x,y and returns the output x + y. Sample input might be x=-1, y=8 in which case the expected output is 7. The expected output is either float or int.

**Task 2: Character count**

Write a function that takes two arguments
- *s* an arbitrary string.
- *l* a letter (i.e. any valid single character).

The function should search the string for occurences of the letter and return an integer indicating how many times the letter *l* occurs in the string *s*.

Note: Your function should be case-insensitive, i.e. it shouldn't care if the letter is "H" or "h"

**Task 3: Function *isEven***

Write a function which evaluates if a given integer number (given as a parameter for the function) is an even number. The function should return a Boolean value True if the number is even and False if the number is odd.
Given a list (or array) of *n* integer numbers, write a program which uses the function *isEven* to determines the number of even items in the list.

**Task 4: Search in List**

Given a list (or array) of *n* floating-point numbers, write a program which searches and outputs the largest number in the list.

**Task 5: String and Loops**

Write a function which takes a string (word) as an argument. The function should print the complete word on the first line and remove the last character on each successive line, ending with a single (the first) character. 
Example: Input word is Test
Function output:
Test
Tes
Te


**Task 6: Get dict keys** 

Write a function that takes as it's single input any dictionary
The function should return the keys of the input dictionary, in a list.

---------------------------------------

### Ok. I need to learn some things. Where should I start? 
If you're starting from 0, that's okay! Just spend a bit of time on self-paced study. There are a dizzying array of Python study options online, including many you can do from your web browser (Coursera, LearnPython.org, DataCamp). If you go ahead and set up your computer for the class, I highly recommend following this course: 

[Python in a notebook](https://github.com/leriomaggio/python-in-a-notebook) 
This course will also familiarizing you with Jupyter notebooks, which we will be using a lot this semester. 

Troubleshooting and email policy
---------------------

![](googlingstuff.jpg)

This meme is funny because it's true. Programming can only be learned by doing. And no matter how much experience you have, it's a process of trial, error, and **lots and lots of Googling.** 

You're working on a group programming project and you're stuck. What do you do? 

1. Google it. 
2. Google it again. Try creative rephrasing. There is a very high chance someone has asked some version of your exac question on [StackExchange](www.stackexchange.org).
3. Try backtracking and simplifying your code. 
4. Use Google to find an alternative way of accomplishing the same task. 

Still stuck? 

5. Ask your classmates in the forum. 
6. Bring it to class on Thursday to troubleshoot. 

Note! *Email your instructors* is not listed as an option above. This is not because we don't care. But we simply do not have enough paid hours to provide help over email (which, of course, would really just outsource the Googling to us)! Do your best, get as far as you can, work with your classmates, and seek help in the Thursday classroom sessions. 



Assessment and exam
--------------

### Assignments 

You will have a number of group programming assignments to complete.

Use Github classroom to upload your assignments. You will receive an email invitation to register in week 36. 

### Assessment/Academic goals 
In the evaluation of the student's performance, emphasis is placed on the extent to which the student is able to:

**Knowledge**: 
- contrast different natural language processing methods in terms of their strengths and weaknesses in different use contexts 
- explain how formal analysis of natural language can provide insights into human cognition and behavior 
- discuss ethical and philosophical issues related to natural language processing software and technology .

**Skills**: 
- identify relevant data sources for specific research and applied questions 
- correctly choose and apply tools for analyzing natural language data.

**Competencies**: 
- critically reflect on and discuss theoretical and empirical implications of using natural language processing techniques 
- justify the choice between relevant methods and analyzes used for specific research questions within the field of natural language processing 
- clear oral presentation of complex analyzes.

### Preparing project for your final exam

Start thinking about your final project idea as early as possible. If you would like to do a group assignment (*highly recommended*) you will have the opportunity to present a brief **project pitch** in week 43 (October 23) where you can recruit collaborators, or join someone else's cool project! 

### Final exam details  
Note: Oral exams will take place between January 20-24, 2020. 

The exam is an individual oral exam based on a written synopsis. The duration is 30 minutes including the student's presentation of the synopsis project, followed by dialogue with the examiners and assessment. 

The synopsis can be done as an individual or group assignment. If it is done as a group assignment, the final product must 

(i) form a coherent text and 
(ii) be organized so that it is possible to make individual assessments of the students contributing. 

In other words, the contribution of each individual student to the whole assignment must be clearly delineated (excluding the introduction, conclusion and bibliography). 

A maximum of three students can take part in a group assignment.
- Length of individual synopsis: 4-7 standard pages (not including code and figures) 
- Length of synopsis for 2 students: 8-14 standard pages (not including code and figures) 
- Length of synopsis for 3 students: 12-21 standard pages (not including code and figures)

### Questions? 

Please ask in the [Padlet](https://padlet.com/rbkh/t0ei3w2v04tx)! 


Poster sessions
--------------

Information on the poster sessions [can be found here](posters.md). 
