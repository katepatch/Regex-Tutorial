# Matching a URL Regex Tutorial

When looking to identify patterns in strings, regex can be a very helpful tool for you.  Often used in search engines or text editors, regex looks to find patterns within strings and help validate URL formats.

## Summary

```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```
This snippet above is a regex that serves as a way for search engines or text editors to know what to look for.  It can match patterns in the string.  Let's break this down below.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
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

Anchors are the starting and/or ending of the string you are trying to search.  A URL regex contains two anchors.

This `^` is an anchor at the beginning of the regex string.  What ever characters follow this carat is what starts the match

This `$` is an anchor at the end of the string you want to search.  

### Quantifiers

`*` `+` `?` are quantifiers that can specify how many occurances of a certain pattern/character inside the regex.  They are usually at the end of the string, character, or pattern.  Let's look a little closer:

- `*` zero or more patterns
- `+` one or more patterns
- `?` zero or one pattern

We can even wrap our occurances in currly brackets for the number of times we need:

- `{x}` x number of occurances
- `{x,}` x or more number of occurances
- `{x, y}` at least x but no more than y occurances

How does our URL apply to these quantifiers?

- `https?`: regex will accept the string with or without the 's'
- `(https?:\/\/)?`: regex will accept the string with or without the 'https://'
- `[\da-z\.-]+`: What is inside the bracket needs to occur at least one time.
- `([a-z\.]{2,6})`: What is inside the bracket must occur at least two times but no more than 6.
- `([\/\w \.-]*)*\/?`: With these endpoints whatever is within the parentheses or brackets can occur zero or more times.

### OR Operator

The `|` character can be used for an OR operator.  Place `|` between the characters, pattern, string you are trying to match.  

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

Kate Patch is currently a student at the Coding Bootcamp with the University of Utah.<br>
Github: [katepatch](https://github.com/katepatch)<br>
Email: kate.epatch@gmail.com
