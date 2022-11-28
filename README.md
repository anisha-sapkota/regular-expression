# regular-expression

Regular expression breakdown.

## Summary

This tutorial will break down the regular expression for matching an email address and explain the individual components.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

/`^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$`/

Anchors don't match any characters but rather the position.

- `^` - the caret anchor matches the beginning of the text
- `$` - the dollar anchor matches the end of the text

### Quantifiers

Quantifiers specify how many characters or expressions to match.

- `a*` - matches `a` 0 or more times
- `a+` - matches `a` 1 or more times
- `a?` - matches `a` 0 or 1 times
- `a{n}` - matches `n` occurrences of `a`, where `n` is a positive integer
- `a{n}` - matches at least `n` occurrences of `a`, where `n` is a positive integer
- `a{n,m}` - matches at least `n` and at most `m` occurrences of `a`, where `n` and `m` are positive integers

/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)$/

- `+` - one ore more times
- `{2,6}` - match at least 2 and at most 6

### Character Classes

Characters classes are used to distinguish different kinds of characters, for example letters and numbers.

/^([`a-z0-9`_\.-]+)@([\d`a-z`\.-]+)\.([`a-z`\.]{2,6})$/

- `a-z` - match a character in the range `a` to `z` (case sensitive)
- `0-9` - match a character in the range `0` to `9`

### Grouping and Capturing

A part of a pattern enclosed within parentheses is known as capturing group.

In our email regex, we have 3 capturing groups.

/^`([a-z0-9_\.-]+)`@`([\da-z\.-]+)`\.`([a-z\.]{2,6})`$/

### Bracket Expressions

Brackets (`[]`) indicate a set of characters to match.

/^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/

- `[a-z0-9_\.-]` - lower case letters (a-z), digits (0-9) and the characters: underscore (\_), period (.) and hyphen (-)
- `[\da-z\.-]` - digits (0-9), lower case letters (a-z) and the characters: period (.) and hyphen (-)
- `[a-z\.]` - lower case letters (a-z) and the character period (.)

### Greedy and Lazy Match

Greedy match will try to match the longest possible string whereas lazy match will try to match the smallest possible string. Appending the `?` character to a quantifier makes it lazy. In our expression we only have greedy quantifiers.

/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)$/

- `+` - match one or more times
- `{2,6}` - match at least 2 times but no more than 6 times

## Author

Created with ❤ by [anisha-sapkota](https://github.com/anisha-sapkota).
