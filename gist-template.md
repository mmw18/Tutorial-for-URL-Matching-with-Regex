# URL Matching with Regex

Welcome to this tutorial on understanding and utilizing regular expressions (Regex) for URL matching. Regular expressions are a powerful tool in programming, allowing for precise pattern matching in text. This tutorial focuses on a Regex pattern specifically designed to match URLs. Regex components will be broken down step-by-step, clarifying how each part contributes to to identifying valid URLs.


## Summary

This tutorial will specifically explore a Regex pattern used for matching URLs: `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`. This pattern combines various components, such as anchors, quantifiers, and character classes to correctly identify different parts of a URL. Each segment will be discussed for this, providing insight into how it validates protocols, domains, and paths.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)


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

In Regex, a character class is defined by square brackets `[]`, and it will match any one character from a set of characters specified within the brackets. Brackets say, "Match any one of *these* characters".

In the URL Regex `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`...

`[\da-z\.-]` : This character class matches a single character that can be:

`\d` : Any digit (0-9). The `\d` is a shorthand character class that matches any numeral digit.

`a-z` : Any lowercase letter from 'a' to 'z'. This range includes all lowercase alphabetic characters.

`\.` : The dot character, which will match any character (except newLine), but when it's inside square brackets, it's taken literally. This here means it will only match a period.

`-` : This is used literally here, and is searching for a `-` in the string.


### Grouping and Capturing

Parentheses create groups for capturing each part of the match. In the URL regex, each set of parentheses is a group.


### Bracket Expressions

Like character classes, bracket expressions will match any one character from a set of characters. 

For example, if your regex has `[abo]`, it's like having a basket with an 'a', 'b', and 'c'. The regex will be happy with any one of these letters, and will match 'a', 'b', or 'c' whereever it finds it in the text.


### Greedy and Lazy Match

Difference between greedy and lazy matching is all about how much text the regex engine tries to consume while making a match.


#### Greedy Matching

- Greedy quantifiers will try to match as much text as possible, and will grab as much as they can while still allowing the overall pattern to match. 
- Commond greedy quantifiers are `*` (zero or more), `+` (one or more), and `{n,m}` (between n and m occurances).


#### Lazy Matching

- Lazy quantifiers are the opposite, and will try to match as little text as possible. They take the least amount that they can and still satisfy the pattern. 
- These are denoted by adding a `?` after the greedy quantifier, like `*?`, `+?`, or `{n,m}?`.


## Author

This tutorial has been created by Megan Wright, a student of web developement and computer science. Follow below for link to view my GitHUb.
[mmw18](https://github.com/mmw18)

