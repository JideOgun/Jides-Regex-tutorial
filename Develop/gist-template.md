# Title (replace with your title)

This gist will be covering a tutorial on regular expression and how it can be used to match a url. 

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.
A regular expression is a sequence of characters that defines a search pattern.
The regex expression that will be covered in this tutorial is /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/.
Regex can be interpreted from left to right. 

https://www.youtube.com/watch?v=c9HbsUSWilw

https://regexr.com/

https://stackoverflow.com/questions/5061940/changing-the-child-elements-css-when-the-parent-is-hovered
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
- [Escaped Characters](#escaped-characters)
- [Literal Characters](#literal-characters)

## Regex Components

### Anchors
In this tutorial the ^ symbol is used. It matches the beginning of a string. It also matches the beginning of a new line if the multine flag is enabled. It is important to note that the ^ symbol matches a position and not a character.
$ matches the end of the string, or the end of a line line if the multiline flag is enabled. It is important to note that the $ symbol matches a position and not a character.

### Literal Characters
This represents literally the characters that are being matched. For example, in the first captured group (https?:\/\/).
 h is a literal character that will be matched, followed by t, followed by another t, followed by a p, followed by an s.
 Regex will match https as these are the literal characters being searched for in the text.
 Notice there is a ? after s, meaning matching the s is optional. This is a quantifier called an optional, and it'll be discussed in the Quantifiers section of the tutorial.
 Then there's a : which is a literal colon.
 The \/\/ is an escaped character and will be discussed in more detail in the escaped character section of the tutorial.

### Quantifiers
Quanitifiers are use to indicate that the prepending chatacter is to matches a certain number of times.
In this tutorial there are a bunch of different quantifiers being used.

The ? optional quantifier which was briefly introduced in the preceeding section indicates that the preceeding character is optional. 
For example (https?:\/\/) indicates that the match can return text that has an s or not. Therefore, all matches of http and https will be returned.

The + matches one or more of the prepending character.

The {2,6} matches the specified quantity of the prepending character. {2,6} will match 2 to 6. {2} will match only 2.
For example in the group ([a-z\.]{2,6}), only character sets between 2 and 6 will be matched.

The * matches 0 or more of the prepending character.
For example in the captured group ([\/\w \.-]*)*

### Escaped Characters
This is used to insert reserved, special and unicode characters. To use an escaped character a \ must be prepended to the character.
In the first captured group (https?:\/\/) the \/  will match a forward slash /. \/\/ will match two forward slashes //.

### Grouping and Capturing
When a group of characters are enclosed in parentheses, this is refered to as grouping and capturing.
This enables substrings to be extracted
In this tutorial there are 4 capturing groups.
(https?:\/\/) - Here the group captured is https:// with the s being optional so http:// will also be matched.
([\da-z\.-]+)
([a-z\.]{2,6})
([\/\w \.-]*)

### Character Classes
Character classes match a characters from a specific set. Example of  character classes are character set, negated set, range, dot, match any, word, not word, digit, not digit.
In this tutorial character set will be discussed in detail.

Character set matches any character enclosed in square brackets [].
There are three character sets in the regular expression.

[\da-z\.-] - In this character set there are two character classes digit and range.
digit - \d will match any digit character from 0-9
range - a-z will mtach characters in the a-z range. It is case sensitive.
Escaped characters - \. this is an escaped character that uses the \ prepended to the . character to find a match


[a-z\.] - In this character set there is a range character class and an escaped character

[\/\w \.-] - In this character set there is a escaped character \/ which will match a forward slash /, there is a character class \w, followed by an escaped character \., followed by a literal - character.
word - \w will match any word character both alphanumeric and underscore. So a-z, A-Z, and 0-9.

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
