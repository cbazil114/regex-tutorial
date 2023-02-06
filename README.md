# Regex Tutorial

Regular expression (regex), or rational expression, is a series of characters that utilize a search pattern within text. This is commonly known by the "find/find and replace" functions that allows a user to search for specific characters. 

## Summary

For this tutorial, I will be using a regular expression used for matching an email address. 
* Matching an Email: ```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```

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
* For the start of a line, use ```^``` followed by the string you are searching. If you do ```^a``` for a line ```abc``` , the highlighted portion will be a. However, if you do this for ```^b```, it will not return anything. This is due to the fact that ```^``` anchor is used for the start of a string or line. 
* For the end of a string, use the anchor ```$```. In the previous example for "abc", you can find ```c``` by entering ```c$```. However, ```b$``` will not find the ```b``` in ```abc```. 

### Quantifiers

Quantifiers are used to specify the number of results a user wants to match their search. For example, the quantifier ```*``` will return something that appears zero or more times. So for the ```abc``` example once more, you can do ```a*``` to find all instances of ```a```. Or for something more specific, you can use something like ```?```, which returns zero or one instances of a search. Other examples include:
* ```+``` -  One of more instances.
* ```{n}``` - n is the number of matches the user wants. 

### Grouping Constructs



### Bracket Expressions



### Character Classes



### The OR Operator

The ```|``` operator is used to search for the inputs on both sides of the line, like using the word "or" between the two inputs. For example, if you use ```a|A```, it will search for all instances of lower case or upper case a. 

### Flags

Flags are used to alter a search (a form of parameter). There are six regex flags:
* ```i``` - This flag makes the search case-insensitive, so there is no difference between ```A``` and ```a```.
* ```g``` - The search looks for all matches versus just the first match. 
* ```m``` - Multiline mode - It affects the behavior of ```^``` and ```$```; the search will match the beginning and the end of line, not just the string. 
* ```s``` - dotall - Expanding off of the ```.```, which is the dot that matches any character in a string, the ```s``` flag is used to search any character, newline included. 
* ```u``` -  Unicode - This flag allows for the use of Unicode in regex. For example, the character ```a``` has a unicode of ```0x0061```, which has a byte length of two. The ```u``` flag enables the correct reading of the unicode of a given character. 
* ```y``` - Sticky form - Executes a search which only checks the position of the source string. For example, if you want to find a word in the fourth position in a string, you can use the ```y``` flag to find the text at the designated spot. 

### Character Escapes



## Author

Connor Bazil is a student at the UNH Coding Bootcamp, ending March 2023. </br>
[Github](https://github.com/cbazil114)