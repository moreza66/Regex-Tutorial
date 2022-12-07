# Regex Tutorial on Matching an Email

Regular expressions can be used to find certain patterns of characters within a string. You can also find and replace a character or sequence of characters within a string. They are also frequently used to validate input. This regex matches character information for valid e-mail addresses.

## Summary

This tutorial will cover a step by step deconstruction of a regex that matches a valid email address.

The regex expression we will be decoding is /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Final Test](#Final-Test)
- [Author](#Author)

## Regex Components

Regular expressions are patterns used to match character combinations in strings. Please see below components used for this regex expression to match an email address.

### Anchors

Anchors match a position before or after characters.

^ – The caret anchor matches the beginning of the text. $ – The dollar anchor matches the end of the text.

In our example /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, we have two anchors ^ and $, meaning where to start a matching pattern and when to end it.

You can see the / slash at the beginning and at the end of our regex expression. Meaning it starts at /^ (beginning) and ends at $/.

### Quantifiers

In our example /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, we specify how many instances of a character, group, or character class must be present in the string matched.

In the case of the left side of the @: /^([a-z0-9_\.-]+)

We will match one string as dictated by the + sign before the last parentheses.

In the case of the right side of the @: ([\da-z\.-]+)\.([a-z\.]{2,6})$/

We will match one string as dictated by the + sign before the escaped period .

{2,6} --> matches between 2 and 6 of the preceding token ([a-z\.])

### Character Classes

In our example /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, we have [] square brackets, these are used to match different types of strings in order to match what you are looking for.

In this case let's divide the expression in two sections, before and after @.

Left side of the @: [a-z0-9_\.-]+

a-z --> match and lowercase character from a-z 0-9 --> match any characters from 0-9 _ --> allow the usage of _ (underscore character) in the matching. . --> escape character for the . character.

--> We will match one string as dictated by the + sign before the last parentheses.
--> allow the usage of - (minus symbol) in the matching
Right side of the @: [\da-z\.-\.-]+)\.([a-z\.]{2,6})$/

\da-z\.-\.-]+) or before .com scenarios for matching.

\d --> match any digit character from 0-9 a-z --> match any character from a-z lowercase (case sensitive) . --> escape character for the . character.

--> allow the usage of - (minus symbol) in the matching
--> We will match one string as dictated by the + sign before the last parentheses.
\.([a-z\.]{2,6})$/ or the .com scenarios for matching.

. --> escape character for the . character. a-z --> match any character from a-z lowercase (case sensitive) . --> escape character for the . character. {2-6} --> matches between 2 and 6 (min 2 and max of 6) of the preceding token ([a-z\.]) $ --> matched at the end of the string. It means that the .com or .ca etc has to be at the end of the email address string.

e.g (right of the @) --> @gmail.ca or hotmail.com

Full example

test1_ab.--@gmail.com test123_ab--.@hotmail.com

### Grouping and Capturing

In our example /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, we have () parentheses used to group two sections. That is before @ and after.

That is to group two regular expressions. One will target before the @, and the other after to match the email address format.

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
