# Regex Guide

This is a regex tutorial for those who want to take the easy way out in sorting and finding things.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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

(^) and ($) are anchors. (^) starts with, and ($) ends with

### Quantifiers

Quantifiers set the limits of the string that your regex matches. Quantifiers are greedy, so they would match as many occurances of particular patterns as possible.
(*) matches the pattern zero or more times
(+) matches the pattern one or more times
(?) matches the pattern zero or one time
{} curly brackets can provide three different ways to set limits for a mtach:
{n} matches the pattern exactly n number of times
{n,} matches the pattern at least n number of times
{n,x} matches the pattern from a minimum of n number of times to a maximum of x number of times

### OR Operator

It's the line (|). The | line makes it pass so that it is not literal and would be able to pass something that's not exactly in the order. Like how [a-z] would pass any of it in.

So (abc):(xyz) with OR operator equals
(a|b|c):(x|y|z)
Now both of the strings "abc:xyz" would match, as well as "a:z" but "xyz:abc" would not.

### Character Classes

A character class in a regex defines a set of characters, any one of which can occur in an nput string to fulfill a match.

(.) matches any character except the newline character (\n)
(\d) matches any arabic numeral digit. This class is equivalent to the bracket expression [0-9]
(\w) Matches any alphanumeric character from basic Latin alphabet, including the underscore (_). This class is equivalent to the bracket expression [A-Za-z0-9_]
(\s) Matches a single whitspace character, including tabs and line breaks.
Any of the last 3 character classes can be changed to perform an inverse match by capitalizing the letters.

### Flags

Usually a regex must be wrapped in slash characters (//). The one exception to this rule is the flags component. Flags are place at the end of a regex after the second slash. They define additional funcationality or limits for the regex. These are,

(g)  Global search: the regex should be tested against all possible matches in a string.

(i) Case-insensitive search: case should be ignored while attempting a match in a string.

(m) Multi-line search: a multi-line input string should be treated as multiple lines.

### Grouping and Capturing

Grouping in regex refers to the process of enclosing one or more parts of a regular expression in parentheses to create a logical subexpression. Grouping allows you to apply quantifiers, alternations, and other operators to a specific part of the pattern. It also enables you to refer to the captured groups later in the expression or in replacement text.

Capturing refers to the process of extracting the matched substring(s) from the text using a capturing group. Capturing groups are marked by enclosing parentheses around a part of the regex pattern. The matched substring(s) inside the capturing group can be retrieved using a backreference, which is a special code that refers to the captured group by its index or name.

### Bracket Expressions

Bracket expressions are enclosed in square brackets ([]) and can contain any combination of characters, ranges, and special characters.
([a-z]) matches any single lowercase alphabet
([A-Z]) matches the upper case
([abc]) matches any single character that is either a b or c
([0-9]) matches any single number
([a-zA-Z]) all lettters either uppercase or lower
([^abc]) matches any singe letter that isn't abc

### Greedy and Lazy Match

Greedy matching is the default behavior of most quantifiers.
It means regex tries to match much of the text as possible. If for example the expression searches for a and b and the string was abababsasdbasb, it would output that result even though ab would've sufficed.

Lazy matching is strict, and is achieved by appending (?) to the quantifier. So the output is ab

### Boundaries

Boundary expressions are special characters that match the beginning or end of a word or line. Boundaries are used to define the exact location in the input text where a match should start or end.

(^) matches the begging of a line or string
($) matches the end of a line or string
(\b) matches a word boundary. A word boundary is a zero-width character that mathes the position between a word character that is defined by (\w)
(\B) matches a non-word boundary

### Back-references

A back-reference is a feature that allows you to match a previously captured group within the same regular expression.

When you capture a group in a regex, the captured text is stored in a numbered "back-reference" that can be referred to later in the regex using a special syntax. The syntax for back-references is a backslash followed by the number of the captured group, such as (\1), (\2), etc.

### Look-ahead and Look-behind

Look-ahead and look-behind are special zero-width assertions that allow you to match a pattern only if it is followed by or preceded by another pattern, respectively.

## Author

I am a student develepor learning the ropes.
https://github.com/mitsushiro1
