# Regex Tutorial

Regular expression (regex), or rational expression, is a series of characters that utilize a search pattern within text. This is commonly known by the "find/find or replace" key binding functions that allows a user to search for specific characters. 

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

### Anchors

Anchors are at the start and or of strings. Anchors do not match any character and instead matches a position in a line/characters. It is important to note how it functions in groups. For example:
* For the start of a line, use ^ followed by the string you are searching. If you do ^a for a line "abc", the highlighted portion will be a. However, if you do this for ^b, it will not return anything. This is due to the fact that ^ anchor is used for the start of a string or line. 
* For the end of a string, use the anchor $. In the previous example for "abc", you can find c by entering c$. However, b$ will not find the b in abc. 

### Quantifiers

Quantifiers are used to specify the number of results a user wants to match their search. For example, the quantifier * will return something that appears zero or more times. Or for something more specific, you can use something like ``` + ```.

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
