# Regex Tutorial

An introduction to what  Regex is and how they work

## Summary

A Regex (Regular Expression) is a string of text that can be used to create search patterns that locate, match and manage text. Here is an example code snippet of regex:
 ```
 /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
 ```

* This Regex is used to match an e-mail address

A Regex can be used from the command line and text editors as well to locate text residing in a file.

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

Anchors are characters contained within the regular expression that enables a user to match strings which may begin or end, or both, certain characters.

Examples of Anchors:

* `^` - matches any string that start with the anterior word
* `$` - matches a string that end with preceeding word before the character

```
^Harrison          matches any string starting with `Harrison`
Pets$          matches any string ending with `Pet`
^New Pet$   matches exact string
Oldpet         matches any string that has the exact text `Oldpet` in it
```

### Quantifiers

Quantifiers are characters contained within the regular expression that specify how many instances a character, group, or character class must be represented in the input to be matched.

Examples of Quantifiers:

* `*` - matches a string that has the anterior followed by zero or more of the last character
* `+` - matches a string that has the anterior followed by one or more of the last character
* `?` - matches a string that has the anterior followed by zero or one of the last character
* `{}` -  matches a string that has the anterior followed by how ever many the number in the brackets of the last character in the string
* `()*` - matches a string that has any anterior characters followed by zero or more copies of the string within the brackets
* Examples:

```
xyz*        matches a string that has xy followed by zero or more z
xyz+        matches a string that has xy followed by one or more z
xyz?        matches a string that has xy followed by zero or one z
xyz{3}      matches a string that has xy followed by 3 z
xyz{3,}     matches a string that has xy followed by 3 or more z
xyz{3,6}    matches a string that has xy followed by 3 up to 6 z
x(yz)*      matches a string that has a followed by zero or more copies of the sequence yz
x(yz){3,6}  matches a string that has a followed by 3 up to 6 copies of the sequence bc
```

### Grouping Constructs

Grouping unifies a pattern or string so that it is matched in a complete block

Examples of Grouping are as follows:
* `()` - parentheses creates a capture group
* `(?:)` - using `?:` disables the capturing group
* `(?<>)` - using `?<>` puts a name to the group
* Examples:
```
x(yz)           parentheses create a capturing group with value yz
x(?:yz)*        using ?: we disable the capturing group
x(?<end>yz)     using ?<end> we put a name to the group
```

### Bracket Expressions

Bracket Expressions are characters enclosed by a bracket `[]` matching any single character within the brackets. 
*note*: if the first character within the brackets is a `^` then it signifies any character *not* in the list, and is unspecified whether it matches an encoding error. 

Examples of Bracket Expressions are as follows: 
* `[]` - matching any single character within the brackets
* `[]%` - matching the string inside the brackets before the `%`
* `[^]` - matching any string that has not a letter from within the brackets (negation of expression)
* Examples:
```
[xyz]         matches a string that either has 'x' or 'x y' or 'x z' (same as x|y|z)
[x-y]         behaves the same as [xyz]
[u-zU-Z0-9]   a string that represents a single case insensitive hexadecimal digit
[0-9]%        a string that has a character from 0-9 before a %
[^a-zA-Z]     a string that does not contain a letter from 'a' to 'z' or from A to Z
```

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
