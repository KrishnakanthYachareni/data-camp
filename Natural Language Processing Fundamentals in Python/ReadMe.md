## Natural Language Processing Fundamentals in Python
In this course, you'll learn Natural Language Processing (NLP) basics, such as how to identify and separate words,
how to extract topics in a text, and how to build your own fake news classifier. You'll also learn how to use basic libraries such as NLTK, 
alongside libraries which utilize deep learning to solve common NLP problems. This course will give you the foundation to process and 
parse text as you move forward in your Python learning.

### What is	Natural	Language	Processing? 
* Field of study focused on making sense of language Using statistics	and	computers You will learn the basics	of NLP.
1. Topic identification
2. Text	classification
* NLP	applications include: 
1. Chatbots
2. Translation
3. Sentiment analysis ...
4. and many	more!

### Common	Regex	Patterns

| Pattern        | matches      | Example |
| ------------- |:-------------:| -----:|
|\w+ | word |'Magic'| 
|\d | digit |9|
| \s |space |' '| 
|.* | wildcard |'username74'|
| +	or *| greedy match |'aaaaaa'| 
|\S | not space |'no_spaces'| 
|[a-z]| lowercase group |'abcdefg|
``` 
NOTE:
It's important to prefix your regex patterns with r to ensure that your patterns are interpreted in the way you want them to.
Else, you may encounter problems to do with escape sequences in strings. For example, "\n" in Python is used to indicate a new line,
but if you use the r prefix, it will be interpreted as the raw string "\n" - that is, the character "\" followed by
the character "n" - and not as a new line
``` 
### regular expressions: re.split() and re.findall()
```  Python
# Import the regex module
import re

my_string = "Let's write RegEx! Won't that be fun?I sure think so.Can you find 4 sentences? Or perhaps, all 19 words?"
# Write a pattern to match sentence endings: sentence_endings
sentence_endings = r"[.?!]*"

# Split my_string on sentence endings and print the result
print(re.split(sentence_endings, my_string))

# Find all capitalized words in my_string and print the result
capitalized_words = r"[A-Z]\w+"
print(re.findall(capitalized_words, my_string))

# Split my_string on spaces and print the result
spaces = r"\s+"
print(re.split(spaces, my_string))

# Find all digits in my_string and print the result
digits = r"\d+"
print(re.findall(digits, my_string))

``` 
### What is tokenization
* Turning	a string or document into tokens (smaller chunks) One step in preparing	a text for NL.
* nltk:	natural	language toolkit library provide tokenization. some of the examples are
1. sent_tokenize: tokenize a document	into	sentences
2. regexp_tokenize:	tokenize	a	string	or	document	based	on	a	regular expression	pattern
3. TweetTokenizer:	special	class	just	for	tweet	tokenization,	allowing	you to	separate	hashtags,	mentions	and	lots	of	exclamation	points!!