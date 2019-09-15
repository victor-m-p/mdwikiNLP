Class 2: Introduction
============

## Videos 
[Basic Text Processing and Edit Distance](https://www.youtube.com/watch?v=808M7q8QX0E&list=PLaZQkZp6WhWy4_bClrW9EGQKnUUD9yp8V)
(Playlist duration: 1 hours, 14 minutes and 30 seconds) 

## Reading 
J+M 3rd Chapter 2 ["Regular Expressions, Text Normalization, Edit Distance", pages 1-25](https://web.stanford.edu/~jurafsky/slp3/2.pdf) 

## Exercises 
*From J+M 3rd Chapter 2 ["Regular Expressions, Text Normalization, Edit Distance"](https://web.stanford.edu/~jurafsky/slp3/2.pdf)*

2.1 Write regular expressions for the following languages.
* 1. 	the set of all alphabetic strings;
* 2.	the set of all lower case alphabetic strings ending in a b;
* 3. 	the set of all strings from the alphabet a,b such that each a is immediately preceded by and immediately followed by a b;

2.3 Implement an ELIZA-like program, using substitutions such as those described
on page 9. You might want to choose a different domain than a Rogerian psychologist, although keep in mind that you would need a domain in which your
program can legitimately engage in a lot of simple repetition.

2.4 Compute the edit distance (using insertion cost 1, deletion cost 1, substitution
cost 1) of “leda” to “deal”. Show your work (using the edit distance grid).

2.5 Figure out whether drive is closer to brief or to divers and what the edit distance is to each. You may use any version of distance that you like.

2.6 Now implement a minimum edit distance algorithm and use your hand-computed
results to check your code.

2.7 Augment the minimum edit distance algorithm to output an alignment; you
will need to store pointers and add a stage to compute the backtrace.


