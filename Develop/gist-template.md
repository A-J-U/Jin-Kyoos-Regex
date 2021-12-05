# Regex email Validation

Regex is the abbreviated word for regular expression, this is used to detect different patterns inside a string. An example of a regular expression is validating an email address, This lets you have a much more polished database. Problems will appear if you do not validate the email addresses as people could create new email addresses that are not registered. 


## Summary

The Regex(Regular Expression) I will be covering today is used for email validation.
The Expression looks like this 	^([a-zA-Z0-9_\-\.]+)@([a-zA-Z0-9_\-\.]+)\.([a-zA-Z]{2,5})$

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

The anchors are the start and end of the expression. The start looks like this ^ and the ending looks like this $. Once you see the $ at the end you know thats the finished expression.

### Quantifiers

Quantifiers are used to see the amount of instances needed to find a match.
The + in the email expression ([\da-z\.-]+)\ allows the component to be broken up into the name, domain and TLD. Example: User01@gmail.com
{2,6} is to only find matches that are more than 2 characters and less than 6 characters.

### Grouping Constructs

The grouping in this expression can be seen by the parentheses. It is broken up into 3 parts 1.Email: /^([a-z0-9_\.-]+) 2.Domain: @([\da-z\.-]+)\ 3. TLD: .([a-z\.]{2,6})$/ 

### Bracket Expressions

Anything with [] around it is considered a bracket expression. This Regex Contains 3.

/^([a-z0-9_\.-]+) Is used to find any lowercase letters from a-z and any numbers from 0-9.

([\da-z\.-]+)\ Is used to find any lowercase letter from a-z and the /d assigns a number to each of those letters.

([a-z\.]{2,6})$/ Is used to find any lowercase letter from a-z and is also looking for a period(.)

### Character Classes

Character classes are used to distinguish different types of characters.
This Regex contains 2 characters that must be distinquished before validation of the email can be completed. They look like this => @ and .

### The OR Operator

The OR operator allows the regex to do either one of the requests in the expression. In this part of the Regex ([a-z0-9_\.-. You can see that The regex is finding any lowercase letter from a-z OR any number from 0-9.

### Flags

 This Regex does not contain any flags, A flag is used after the second / in the regex. A good example though is an i and it is used to ignore any case sensitive searches.

### Character Escapes

The \ is used before { in order for the Regex to know to search for the information inside the brackets and not the start of the quantifier.O nce it is inside a bracket it is no longer used for that purpose. In the email validation the backslash is inside of brackets /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/.

## Author

https://github.com/A-J-U
