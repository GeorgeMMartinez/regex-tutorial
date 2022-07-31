# Matching a URL using regex.

A regular expression, or regex, is a sequence of characters that specifies search patterns in text. This tutorial will explain how a regex functions, what components make up a regex, and what each component is.
## Summary

This tutorial will focus on the following regex, which will be called "Matching a URL".
```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```
This regex will answer if a text is a valid URL.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

There are two anchors in this regex, which are ```^``` and ```$```. These two symbols represent the beginning and end of a string of text, ```^``` marking the beginning and ```$``` marking the end. 

### Quantifiers

Quantifiers such as ```*```, ```?```, and ```{}``` signify how many times an expression may be identified. ```*``` means multiple occurences of the character before the quantifier is optional. ```?``` means a single occurence of the character before the quantifier is optional. Lastly, ```{}``` defines a range of occurences that a match may be identified.

### OR Operator

```[]``` is the main operator in the Matching a URL regex above. This operator will match for any characters/character classes within the brackets. ```[a-z]``` matches for any characters between a and z. 

### Character Classes

Like above, ```[a-z]``` will match lowercase characters from a-z. Two other character classes are include ```\d``` and ```\w```. The first is a character class which searches for a numeric digit while the second searches for an alphabetic character. 

### Grouping and Capturing

Grouping expressions are used to check parts or sections of a string by using ```()```. These subexpressions will look for exact searches like for ```(uci)```, ```uci``` would match but not ```uic```.

### Bracket Expressions

A bracket expression is a expression between ```[]``` brackets, such as the OR Operator above. For bracket expressions, you can include all characters you would want to match but uses a hypen to show a range of characters. So instead of including the entire alphabet, ```[a-z]``` would suffice. 

### Greedy and Lazy Match

Greedy and lazy searches will find the longest matching string and the shortest matching string, respectively. 
For example: ```<.+>``` is a greedy match while ```<.+?>``` is a lazy match. 
If you have the following code:
```<h1>Hello World!</h1>```
The greedy match will be ```<h1>Hello World!<h1>``` while the lazy match will be ```<h1>``` and ```</h1>```.

## Author

Written by George Martinez. GitHub profile can be found at https://github.com/GeorgeMMartinez
