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

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
