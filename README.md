# Regex Tutorial

Regular expression (regex), or rational expression, is a series of characters that utilize a search pattern within text. This is commonly known by the "find/find and replace" functions that allows a user to search for specific characters. 

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
* For the start of a line, use ``` ^ ``` followed by the string you are searching. If you do ``` ^a ``` for a line ``` abc ``` , the highlighted portion will be a. However, if you do this for ``` ^b ```, it will not return anything. This is due to the fact that ``` ^ ``` anchor is used for the start of a string or line. 
* For the end of a string, use the anchor ``` $ ```. In the previous example for "abc", you can find ``` c ``` by entering ``` c$ ```. However, ``` b$ ``` will not find the ``` b ``` in ``` abc ```. 

### Quantifiers

Quantifiers are used to specify the number of results a user wants to match their search. For example, the quantifier ``` * ``` will return something that appears zero or more times. So for the ``` abc ``` example once more, you can do ``` a* ``` to find all instances of ``` a ```. Or for something more specific, you can use something like ``` ? ```, which returns zero or one instances of a search. Other examples include:
* ``` + ``` -  One of more instances.
* ``` {n} ``` - n is the number of matches the user wants. 

### Grouping Constructs



### Bracket Expressions



### Character Classes



### The OR Operator

The ``` | ``` operator is used to search for the inputs on both sides of the line, like using the word "or" between the two inputs. For example, if you use ``` a|A ```, it will search for all instances of lower case or upper case a. 

### Flags

Flags are used to alter a search. There are six JavaScript regex flags:
* ```i``` - This flag makes the search case-insensitive, so there is no difference between ```A``` and ```a```.
* ```g``` - 
* ```m``` - 
* ```s``` - 
* ```u``` - 
* ```y``` - 

### Character Escapes



## Author

Connor Bazil is a student at the UNH Coding Bootcamp, ending March 2023. </br>
[Github](https://github.com/cbazil114)