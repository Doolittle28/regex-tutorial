# Title 

Regex Tutorial  

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.  

## Table of Contents

- [Anchors](#anchors)  
- [Quantifiers](#quantifiers)  
- [Grouping Constructs](#grouping-constructs)  
- [Bracket Expressions](#bracket-expressions)  
- [Character Classes](#character-classes)  
- [The OR Operator](#the-or-operator)  
- [Flags](#flags)  
- [Character Escapes](#character-escapes)  

## Regex Components
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/  

### Anchors

The Anchors of a regular expression are  the symbols at the beginning and end of the string. The opening anchor is the symbol ^ and the end is the symbol is $. 
  ^ is the anchor that matches the beginning of input.
    $ matches the end of the input string.
The code inside the opening and closing anchors is where the action is. This code is what does the matching of the URL.

### Quantifiers
Quantifiers communicate to the regex engine that it must match the quantity of the character or expression to its left. These are the quatifiers that are used in regex:
  ?, +, *, {n}, {n, }, {n,m}
  In the URL matching regex they are used in the following places:
    https?          Matches 'https', 'http'
    [\da-z\.-]+     Matches a single digit, group of letters (a-z), dot (.) or hyphen (-) 1 or more times
    [a-z\.]{2,6}    Matches 2 to 6 copies of the sequence [a-z\.]
    [\/\w \.-]*     Matches '/', '.', '-', 'www', '//'

### Grouping Constructs
The use of grouping expressions is to allow for the extraction of the characters of a given group for validation. The text between paranthesis is a group.
    (https?:\/\/)       Matches: ' ', 'https://', 'http://'
    ([\da-z\.-]+)       Matches: 'ab.c-7', 'ab'
    ([a-z\.]{2,6})      Matches: 'ab.', '.ca'
    ([\/\w \.-]*)       Matches: '/', '/ab.'

### Bracket Expressions
Bracket expressions are used between brackets. In this example, we have the following Bracket Expressions.
    [\da-z\.-]
    [a-z\.]
    [\/\w \.-]

### Character Classes
Character Classes ensure that a given sequence of characters matches a larger set of characters.

    [a-z]          Matches lowercase alphabetic characters between a and z
    \w             Matches a word
    \d             Matches a single character that is a digit
    .              Matches any character


### The OR Operator
The pipe | is considered an alternation. It will match expressions that come before and after it in the code but this is not present in our code.

### Flags
No flag was used in this example. Flags follow up the closing forward slash of an expression changing how it is interpreted.

Some examples would be:
Ignore case i will make the entire expression case-sensitive.
Global search g store the index of the last match.
Sticky y only matches the last iundex position and ignores global search flag.
Unicode u allows extended unicode escapes in the form.

### Character Escapes
Character escapes use "\.", using the backsplash denotes that we want to find just the dot.

## Author

Kevin Doolittle - github.com/doolittle28 