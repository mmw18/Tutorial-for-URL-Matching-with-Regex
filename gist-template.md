# URL Matching with Regex

Welcome to this tutorial on understanding and utilizing regular expressions (Regex) for URL matching. Regular expressions are a powerful tool in programming, allowing for precise pattern matching in text. This tutorial focuses on a Regex pattern specifically designed to match URLs. Regex components will be broken down step-by-step, clarifying how each part contributes to to identifying valid URLs.

## Summary

This tutorial will specifically explore a Regex pattern used for matching URLs: `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`. This pattern combines various components, such as anchors, quantifiers, and character classes to correctly identify different parts of a URL. Each segment will be discussed for this, providing insight into how it validates protocols, domains, and paths.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

In Regex, anchors are what specify the start and end of a string to be matched. 

`^` - This symbol is used as an anchor to match the beginning of a string.

`$` - This symbol is used as an anchor to match the end of a string.


### Quantifiers

In regular expressions, quantifiers are instructions that tell the computer how many times a certain piece of text should appear for it to be considered a match.

#### Quantifier Rules:

`*`: The character can show up as many times as it wants, including not at all

`+`: The character needs to show up at least once, but it can be more than once

`?`: The character can be there, but it's also okay if it's not

`{}`: You need to find the character a specific number of times, like exactly 6 times, or maybe anywhere between 1 to 5 times.

#### In the URL Regex: 

`?` after `https?:\/\/` makes the protocol `(http://` or `https://`) optional.

`*` after `([\/\w \.-]*)` allows for any number (including zero) of path characters.

`{2,6}` after the top-level domain specifies that it should be between 2 to 6 characters long.

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
