# Regex Tutorial

A regular expression (regex), or rational expression, is a series of characters that utilize a search pattern within text. This is commonly known by the "find/find and replace" functions that allows a user to search for specific characters. 

## Summary

I will use a regular expression for this tutorial to match an email address. 
* Matching an Email: ```^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$```

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

Anchors are at the start and or of strings. Anchors do not match any character and instead match a position in a line/characters. It is important to note how it functions in groups. For example:
* For the start of a line, use ```^``` followed by the string you are searching. If you do ```^a``` for a line ```abc``` , the highlighted portion will be a. However, if you do this for ```^b```, it will not return anything. This because ```^``` anchor is used for the start of a string or line. 
* For the end of a string, use the anchor ```$```. In the previous example for "abc", you can find ```c``` by entering ```c$```. However, ```b$``` will not find the ```b``` in ```abc```. 
* When looking at the summary expression, the returned value would be the entire email, since all the parameters are between the ```^``` and ```$```. When I enter "email@hotmail.com" as a test string, the matched value is the entire email address. 

### Quantifiers

Quantifiers are used to specify the number of results a user wants to match their search. For example, the quantifier ```*``` will return something that appears zero or more times. So for the ```abc``` example once more, you can do ```a*``` to find all instances of ```a```. Or for something more specific, you can use something like ```?```, which returns zero or one instances of a search. Other examples include:
* ```+``` -  One of more instances. In the expression from the summary, this is used to search both ```[a-z0-9_\.-]``` and ```\da-z\.-]``` for between one and unlimited matches. 
* ```{n}``` - n is the number of matches the user wants. In the expression in the summary, the use of ```{2,6}``` means that it searches ```[a-z\.]``` between two and six times. 

### Grouping Constructs

Grouping constructs are used to group substrings of an input. Usually utilizing ```()```, you can group multiple tokens together to create a group for extracting a substring. For example, in the summary expression, there are three groups:
* ```([a-z0-9_\.-]+)```
* ```([\da-z\.-]+)```
* ```([a-z\.]{2,6})```</br>
If you were searching username@gmail.com, the three groups would be "username", "gmail", and "com".

### Bracket Expressions

Using ```[]``` to house a range of characters we want to match. For a small example, if you use ```[abc]```, it will search for any string that include either a, b, or c. </br>
In the summary expression, there are three different instanes of ```[]```
* ```[a-z0-9_\.-]``` - Searches for all instances of a-z, 0-9, ```_```, ```.```, and ```-```. 
* ```[\da-z\.-]``` - Searches for any digit between 0-9, any character a-z, and any instance of ```.``` and ```-```.
* ```[a-z\.]``` - Searches for any character a-z, and any ```.``` in the string. </br>
As you can see from the three bracket expressions, they are most of what you'd find in the grouping constructs. However, some elements are outside of the bracket expressions, such as the quantifiers. 

### Character Classes

Character classes are used to define a range of character which which can appear in an input string to satisfy a given search. For example, we mention the bracket expression ```[\da-z\.-]``` in the previous section. The ```\d``` is used to match a digit equivalent of ```[0-9]```. 

### The OR Operator

The ```|``` operator is used to search for the inputs on both sides of the line, like using the word "or" between the two inputs. For example, if you use ```a|A```, it will search for all instances of lower case or upper case a. 

In the case of the summary regular expression, there is no OR operator being used. But, for example, you can add additional quantifiers like this: ```([a-z\.]{2,6}|[a-z\.]{7})```. In this example, it will return a match if the string is between two and six characters, or it will return if it is seven characters. 

### Flags

Flags are used to alter a search (a form of parameter). There are six common regex flags:
* ```i``` - ignoreCase - This flag makes the search case-insensitive, so there is no difference between ```A``` and ```a```.
* ```g``` - global - The search looks for all matches versus just the first match. 
* ```m``` - Multiline mode - It affects the behavior of ```^``` and ```$```; the search will match the beginning and the end of line, not just the string. 
* ```s``` - dotall - Expanding off of the ```.```, which is the dot that matches any character in a string, the ```s``` flag is used to search any character, newline included. 
* ```u``` -  Unicode - This flag allows for the use of Unicode in regex. For example, the character ```a``` has a unicode of ```0x0061```, which has a byte length of two. The ```u``` flag enables the correct reading of the unicode of a given character. 
* ```y``` - Sticky form - Executes a search which only checks the position of the source string. For example, if you want to find a word in the fourth position in a string, you can use the ```y``` flag to find the text at the designated spot. </br>

In the regular expression from the summary, these flags are not applicable.

### Character Escapes

In regular expressions, the ```\``` character is used when you do not want to search for a character literally. For example, using ```{}``` is a commonly used quantifier. If you add the ```\``` before the curly brackets, you are searching for the curly brackets themselves. </br>
In the summary expression, there are actually a few examples of character escapes. In ```[\da-z\.-]```, the ```\.-``` is a character escape to enable matching of both ```.``` and ```-```. 

## Author

Connor Bazil is a student at the UNH Coding Bootcamp, ending March 2023. </br>
[Github](https://github.com/cbazil114)