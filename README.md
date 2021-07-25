# Regex Tutorial

A regular expression is a sequence of characters that forms a search pattern. The search pattern can be used for text search and text replace operations. A regular expression can be a single character, or a more complicated pattern. Regular expressions can be used to perform all types of text search and text replace operations.

### Syntax 

``````javascript
/pattern/modifiers;
``````

## Summary

In this tutorial, we will use `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` as an example to understand more about regular expressions.
This example is a regular expression to match a valid email address.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

The characters ^ and $ are both considered to be anchors. The character ^ signifies that string with start with characters that are
mentioned after it, where as $ signifies that string will end with characters that are preceeding it.
In this example, the string will start with any characters matching the pattern `a-z0-9_-.`
and must end with `a-z`


### Quantifiers

Quantifiers specify the frequency of occurence of the characters. In other words, it tells the minimun and maximun number of characters the 
regex is looking for.

 - `+` Matches the pattern one or more times . In this example, It tells that before and after  `@` , it must have one or more characters
 - `{ n, x }` Matches the pattern from a minimum of n number of times to a maximum of x number of times. 
    In this example, `{2,6}` signifies that after `.`,  string must have minimum two and maximum of six characters.


### Grouping Constructs
We primarily use () bracket to define a group. Anything inside these brackets is called a subexpression. 
In the above example,
- First capturing group: `([a-z0-9_\.-]+)` The "name" to match at any letters, numbers, underscore, dots and/or hyphens followed by @ symbol.
- Second Capturing group: `([\da-z\.-]+)` The "domain" to match any digits meta characters, letters, dot and/or hyphens.
- Third Capturing group: `([a-z\.]{2,6})` The "domain suffix".

### Bracket Expressions

Bracket expressions are denoted by []. Anything inside these brackets are the range of characters we would like to match.
In this example, `[a-z0-9_\.-]` 
 
### Character Classes

They define the set of characters in a string to fulfill an equivalent match.

- `\d` Matches any Arabic numeral digit. This class is equivalent to the bracket expression [0-9]. 
   In the above example, to match for domain, `([\da-z\.-]+)` this has been used

### Character Escapes

When we want to look for special characters. we use backslash `\` to include the search for these characters.
Example, we wanted period to be included. So the period is preceeded with backslash above like this. `)\.(`

## Author

Kunal Choudhary
Github (https://github.com/kunalc156)
