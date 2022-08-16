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
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

This `^` is an anchor at the beginning of the regex string.  What ever characters follow this carat is what starts the match

This `$` is an anchor at the end of the string you want to search.  

Where are the anchors on our URL?

```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```

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

### Character Classes

Regex characters are catorgorized by digits, letters, or special characters. 

How does our URL apply to character classes?

```
[\da-z\.-]
```
This will match with `\d` a single digit between 0-9, lowercase letters `a-z`, a period `.`, or hyphen `-`.

### Grouping and Capturing

Grouping together strings to be matched are inside `()`.<br>
How does our URL apply to grouping/capturing?

- `(https?:\/\/)`: to group the protocol
- `([\da-z\.-]+)`: to group the domain
- `([a-z\.]{2,6})`: to group the top domain
- `([\/\w \.-]*)`: to group any endpoints that might be there

### Bracket Expressions



### Greedy and Lazy Match


## Author

Kate Patch is currently a student at the Coding Bootcamp with the University of Utah.<br>
Github: [katepatch](https://github.com/katepatch)<br>
Email: kate.epatch@gmail.com
