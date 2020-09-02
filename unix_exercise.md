Unix for Poets exercise

# extended counting exercises

- Merge upper and lower case by down casing everything (use tr a second time)



1. tokenize by replacing the complement of letters with newlines (takes care of \s* with -s which squeezes repeats)
2. replace all uppercase with lowercase
3. sort alphabetically
4. merge duplicates and show counts

- How common are different sequences of vowels, e.g., ''ieu'' (use tr a second time)

1. tokenize by replacing the complement of letters with newlines
2. replace all uppercase with lowercase
3. replace the complement of vowels with newlines (preserve vowels that are originally together and consider vowel sequences as words)
4. sort alphabetically
5. merge duplicates and show counts

# counting and sorting exercises

- Find the 50 most common words in the NYT (use sort a second time, then head)


1. tokenize by replacing the complement of letters with newlines
2. sort alphabetically
3. merge duplicates and show counts
4. sort numerically (i.e. by the counts) and in descending/reverse order
5. show the top 50

- Find the words in the NYT that end in ''zz"


1. tokenize by replacing the complement of letters with newlines
2. reverse all words
3. sort alphabetically (words ending in ''zz'' are at the end)
4. reverse all words again so they are normal
5. show the last several words just to peek at the file to see which ones end in ''zz"

Alternatively, could use grep to specifically find the words that end in ''zz''.


- Get all bigrams


1. tokenize
2. output lines starting with the 2nd line to nyt.nextwords (these are words_{i+1})
3. write lines of the sequentially corresponding lines from nyt.words (words_i) and nyt.nextwords (words_{i+1}) separated by tabs
4. Peek at the first 5

# bigrams and trigrams exercises

- Find the 10 most common bigrams


1. lowercase bigrams
2. sort alphabetically
3. count 
4. sort in descending order by number
5. look at top 10

- Find the 10 most common trigrams


1. output lines starting with the 3rd line to nyt.thirdwords (these are words_{i+2})
2. write words_i words_{i+1} words_{i+2}
3. lowercase
4. sort alphabetically
5. count
6. sort in descending order by number
7. look at top 10



# grep and wc exercises



1. look for words that start capitalized, are 1 capitalized letter or more, and end capitalized.
2. word count

- How many 4-letter words?
grep -P '^[a-zA-Z]{4}$' nyt.words | wc
grep -P '^[A-Za-z][A-Za-z][A-Za-z][A-Za-z]$' nyt.words | wc

Answer: 169549

- How many different words are there with no vowels

grep -v '[AEIOUaeiou]' nyt.words | sort | uniq | wc

1. keep lines not containing vowels
2. sort
3. merge duplicates
4. count words
Answer: 429

- How many "1 syllable" words are there (i.e. words with exactly one vowel)

tr 'A-Z' 'a-z' < nyt.words | grep -P '^[^aeiouAEIOU]*[aeiouAEIOU]+[^aeiouAEIOU]*$' | uniq | wc

Answer: 559044

1. match words that may or may not start with a non-vowel, contains one sequence of vowels (e.g. ball, beat), and that may or may not end a non-vowel.
2. merge duplicates
3. count words

tr "[:upper:]" "[:lower:]" < nyt.words | grep -v '.*[aeiou].*[aeiou].*' | uniq | wc

Answer: 508450
Jade: I think .* is too lenient--should specify non-vowels instead of wildcard. Also potentially could match words with more than one syllable like ballast.

# sed exercises

- Count frequency of word initial consonant sequences

tr "[:upper:]" "[:lower:]" < nyt.words | sed 's/[aeiouAEIOU].*$//' | sort | uniq -c

tr "[:upper:]" "[:lower:]" < nyt.words | sed 's/[aeiou].*//g' | sort | uniq -c | sort -rn | less

1. tokenize
2. delete first vowel through end of the word
3. sort and count

(total of 711 sequences when ignoring case)

- Count word final consonant sequences
tr "[:upper:]" "[:lower:]" < nyt.words | rev | sed 's/[aeiouAEIOU].*$//' | sort | uniq -c | rev

tr "[:upper:]" "[:lower:]" < nyt.words | sed 's/^.*[aeiou]//g' | sort | uniq -c | sort -rn | less

Can reverse words before deleting first vowel through end of the word OR can delete from beginning of the word to the first vowel.

(total of 811 sequences)

# shuf exercises

- Print 10 random word tokens from the NYT excerpt (where each word instance, i.e. word token, is equally likely)

tr "[:upper:]" "[:lower:]" < nyt.words | shuf -n 10

- Print 10 random word types from the NYT excerpt (where each different word, i.e. word type, is equally likely)

tr "[:upper:]" "[:lower:]" < nyt.words | uniq | shuf -n 10

Merge duplicates before shuffling.

# cut exercises

- How often is 'that' used as a determiner (DT) "that rabbit" vs. a complementizer (IN) "I know that they are plastic" vs. a relative (WDT) "The class that I love"

cat parses.conll | grep -P '(that\t_\tDT)|(that\t_\tIN)|(that\t_\tWDT)' | cut -f 2,4 | sort | uniq -c

1. grep out the specific cases
2. only include the word and POS
3. sort
4. count

- What determiners occur in the data? What are the 5 most common?
cat parses.conll | tr 'A-Z' 'a-z'| grep -P '\tdt\t' | cut -f 2,4 | sort | uniq -c | sort -rn |head -n 5

1. lowercase
2. grep for DT (which has been lowercased)
3. only include word and POS
4. sort
5. count
6. sort in descending order
7. include top 5