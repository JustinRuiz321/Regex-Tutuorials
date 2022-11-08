# Introduction to Regular Expression (Regex)

In this repository, you can learn more about what Regex is and how to use it in your code.

## Table of Contents

- [Introduction to Regular Expression (Regex)](#introduction-to-regular-expression-regex)
  - [Table of Contents](#table-of-contents)
  - [Summary](#summary)
    - [What is Regex?](#what-is-regex)
    - [When do you use Regex?](#when-do-you-use-regex)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Grouping Constructs](#grouping-constructs)
    - [Bracket Expressions](#bracket-expressions)
    - [Character Classes](#character-classes)
    - [The OR Operator](#the-or-operator)
    - [Flags](#flags)
    - [Character Escapes](#character-escapes)
  - [Author](#author)


## Summary

### What is Regex?

A Regular Expression (or Regex) is a pattern (or filter) that describes a set of strings that matches the pattern. In other words, a regex accepts a certain set of strings and rejects the rest.

### When do you use Regex?
Regular expressions are extremely useful in extracting information from any text by searching for one or more matches of a specific search pattern

## Regex Components
Below is a list of different regex components you may find in different application's code, or even can find useful when developing your own code.

### Anchors
Anchors belong to the family of regex tokens that don't match any characters, but that assert something about the string or the matching process. Anchors assert that the engine's current position in the string matches a well-determined location: for instance, the beginning of the string, or the end of a line.
Examples:
```
^ = Start of a string / line
$ = End of a string / line
\A = Start of a string but not line
\Z = End of a string but not line
```

### Quantifiers
Quantifiers match the preceding element zero or more times but as few times as possible. It's the lazy counterpart of the greedy quantifier.
Examples:
```
* = Zero or more
+ = One or more
*? = zero or more
+? = one or more
? = zero or one
{3,5} = Three to Five
{10,} = Ten or more
{,10} = At most 10
{10} = Exactly 10
```

### Grouping Constructs
Grouping constructs delineate the subexpressions of a regular expression and capture the substrings of an input string. You can use grouping constructs to do the following: Match a subexpression that is repeated in the input string.
Examples: 
```
[chars] = Matches one of the characters inside the brackets
[^ chars] = Matches a character that is NOT inside the brackets
[first - last] = Matches a character between the first and last characters
\w = Matches a character with ASCII code given by the two or three octal digits
\W = Matches a character with the unicode representation given by four hexadecimal digits
\s = Matches a single whitespace character
\S = Matches a single non whitespace character
\d = Matches a single decimal digit
\D matches a single character that is not a decimal digit
```

### Bracket Expressions
A bracket expression (an expression enclosed in square brackets, "[]" ) is an regular expression that shall match a specific set of single characters, and may match a specific set of multi-character collating elements, based on the non-empty set of list expressions contained in the bracket expression.
Example:
```
example@gmail.com
([a-zA-z0-9_.+-]+)@[a-zA-Z0-9_.+-]+\.[a-zA-Z0-9_.+-]
```

### Character Classes
In the context of regular expressions, a character class is a set of characters enclosed within square brackets. It specifies the characters that will successfully match a single character from a given input string.

Use previous Example and notice the characters enclosed within square brackets

### The OR Operator
Regex recognizes range expressions inside a list. They represent those characters that fall between two elements in the current collating sequence. You form a range expression by putting a range operator between two characters.

### Flags
A regular expression consists of a pattern and optional flags: g , i , m , u , s , y . Without flags and special symbols, the search by a regexp is the same as a substring search. The method str. match(regexp) looks for matches: all of them if there's g flag, otherwise, only the first one.
Example:
```
str.match(/puppy/g) = without i flag
str.match(/puppy/gi) = with i flag
```

### Character Escapes
The \ is known as the escape code, which restore the original literal meaning of the following character. Similarly, ^ , $ (position anchors) have special meaning in regex. You need to use an escape code to match with these characters.
```
Use grouping constructs as your example
```

## Author

This was wrote by Justin Ruiz, a Full-stack web developer. If you would like to look at some of his projects, please clink this link to take you to his GitHub profile:
https://github.com/JustinRuiz321

