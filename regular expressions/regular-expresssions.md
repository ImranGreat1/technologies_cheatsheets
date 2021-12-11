# REGULAR EXPRESSIONS
Regular expressions is a way to search through a string of text.
We use regular expressions to do stuff like validations, get part 
of a string, find and replace and so many advance stuff.

In almost every programming language, we start regular expression
operations by using two forward slashes and then everything inside
the slashes is our expression that we are trying to search. There
can also be a flage after the last slash (the end of the expression)
which will add more conditions to the search


### Find the first string that matches or include "food" in it
~~~bash
  /food/  
~~~

### Find all the string that matches or includes "food" in it
the g flag means global, that is match all not just the first string that match
~~~bash
  /food/g
~~~


### Find all the string that matches or include "The" in it with case sensitive
The following expression will match "The" but not "the" since it's case sensitive
~~~bash
  /the/
~~~


### Find the string that matches or include "the" in it with case insensitive
~~~bash
  /the/i
~~~


### Find all the string that matches atleast one or more "e" in a string
This expression will match "e" or "ee" or match more of the proceeding token.
Match as many e's in a row as you can but match aleast one e.
~~~bash
  /e+/g
~~~


### Find all the string but whatever is before the question mark is optional
This expression will match "e" and if it find anything with "ea" is allow
to match but that is optional
~~~bash
  /ea?/g
~~~

### Find all the string that matches or includes "ea"
~~~bash
  /e+a/g
~~~


### Find all the string that matches or includes "e" or e's in arow or "ea"
The "ea" is optional
~~~bash
  /e+a?/g
~~~


### Find all "r" or "re" or with atleast any numbers of e's in a row proceeding
This e's here is optional
~~~bash
  /re*/g
~~~


### This matches anything before the period
The following will match "eat", "sat", "cat". The number of period will determine
the number of character it matches before the period. But it doesn't match a new
line
~~~
  /.at/g
~~~ 

### This matches anything after the period
The following will match "game", "gard", "gase". The number of period will determine
the number of character it matches after the period. But it doesn't match a new line
~~~bash
  /ga../g
~~~ 

### To search all the periods (.)
This is escaping the period not to treat it as an expression
~~~bash
  /\./g
~~~


### Matches any character that comes before the period and the period
~~~bash
  /.\./g
~~~


### Matches any word character e.g A-Z but not periods . or question marks
~~~bash
  /\w/g
~~~

### Matches anything that is not a word character
Note that is an uppercase W
~~~bash
  /\W/g
~~~


### Matches any form of whitespaces that there is  
~~~bash
  /\s/g
~~~

### Matches anything that is not whitespace
Note that this is an uppercase S
~~~bash
  /\S/g
~~~


### Matches any for 4 digit characters in a row
~~~bash
  /\w{4}/g
~~~

### Matches any 4 digits or more characters in a row
~~~bash
  /\w{4,}/g
~~~

### Matches any 4 or 5 digits characters in a row
~~~bash
  /\w{4,5}/g
~~~

### Matches any character that start with "f" or "c" and ends with "at"
~~~bash
  /[fc]at/g
~~~

### Matches any character that start from a - z and ends with "at"
~~~bash
/[a-z]at/g
~~~

### Matches any character that start with a-z or uppercase A-Z and ends in "at"
~~~bash
/[a-zA-Z]at/g
~~~ 

#### Matches any character that start with 0-9 and ends in "at"
~~~bash
/[0-9]at/
~~~

**We can do [] any range in between the brackets e.g [a-f], [1-4], [f-s] etc**


## GROUP
Anything inside the () are going to be there on group and they only act upon
themselves. Anything inside () is affected by what comes after the parenthesis.
e.g /er{1,2}/ only affect the r, /(er){1,2}/ affect the er together, /(e|r){1, 3}/
after the e or r. 

### Matches anything that starts with lowercase or uppercase t and continue with "he"
~~~bash
/(t|T)he/
~~~

### Matches anything that has "t" or "The"
~~~bash
  /t|The/g
~~~

### Matches characters with "t" or "e" or "s" that contains 2 to 3 chracters after it
~~~bash
  /(t|s|e){2, 3}/g
~~~



### search T that matches the beginning of the entire text not just one word
~~~bash
  /^T/g
~~~

### search T that matches the beginning of each line
The m flag stands for multinline
~~~bash
  /^T/gm
~~~

### Period (.) should Match the end of our entire text
~~~bash
  /\.$/g
~~~

### Period (.) should Match the end of our each line in our text
~~~bash
  /\.$/gm
~~~


### Look Behind
Look behind allows you to find characters that are after certain
characters but not including the initial characters

### Find every single character that is after the word "the" or "The"
~~~bash
  /(?<=[tT]he)/g
~~~

### Matches every single character that is not after the word "the" or "The" 
~~~bash
  /(?<![tT]he)/g
~~~

### Look Ahead
Find characters that come before certain characters but not including the initial
characters

### Matches any character that is followed by "at"
~~~bash
  /(?=at)/
~~~

### Matches any character that is not followed by "at"
~~~bash
  /(?!at)/
~~~


# \d means any form of digit
~~~bash
  /\d/g
~~~

# Get 10 digits in a row
~~~bash
  /\d{10}/g
~~~

