# Jide's Regex Tutorial

This gist will be covering a tutorial on regular expression and how it can be used to search for a url. 

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.
A regular expression is a sequence of characters that defines a search pattern.
The regex expression that will be covered in this tutorial is `^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`.
Regex can be interpreted from left to right. <br>

The opening symbol ^ indicates to start matching from the beginning of a string or line,
the first group enclosed in parentheses is optional because of the ? appended (https?:\/\/) will match http and optionally s, then a :, then //.<br>
The next group will be `([\da-z\.-]+)`, which will match one or more set of digits and small case letters a-z followed by a period and a dash. <br>
The next group will be `([a-z\.]{2,6})` which match small letter case aphabets from a-z followed by a period within the range of 2 to 6. <br>
`([\/\w \.-]*)*\/?$` will match all forwards slahes followed by any word followed by any period, followed by any dash. <br>
The * after the closing parentheses will match 0 or more of the captured group followed optionally by an forwards slash and finally the dollar symbol to signify the end of the string or line.

## Table of Contents

- [Anchors](#anchors)
- [Literal Characters](#literal-characters)
- [Quantifiers](#quantifiers)
- [Escaped Characters](#escaped-characters)
- [Grouping and Capturing](#grouping-and-capturing)
- [Character Classes](#character-classes)
- [Author](#author)

## Regex Components
## Anchors
In this tutorial the ^ symbol is used. It matches the beginning of a string. It also matches the beginning of a new line if the multine flag is enabled.<br>
It is important to note that the ^ symbol matches a position and not a character. For example in the beginning of the regex `^(https?:\/\/)` it used to indicate beginning of the string<br>
<br>
The dollar sign matches the end of the string, or the end of a line line if the multiline flag is enabled. It is important to note that the `$` symbol matches a position and not a character. For example `([\/\w \.-]*)*\/?$` is used to indicate the end of the string.

## Literal Characters
This represents literally the characters that are being matched. For example, in the first captured group `(https?:\/\/)`.<br>
 h is a literal character that will be matched, followed by t, followed by another t, followed by a p, followed by an s.<br>
 Regex will match https as these are the literal characters being searched for in the text.<br>
 Notice there is a ? after s, meaning matching the s is optional. This is a quantifier called an optional, and it'll be discussed in the Quantifiers section of the tutorial.<br>
 Then there's a : which is a literal colon.<br>
 The `\/\/` is an escaped character and will be discussed in more detail in the escaped character section of the tutorial.<br>

## Quantifiers
Quantifiers are used to indicate that the prepending chatacter is to matches a certain number of times.<br>
In this tutorial there are a bunch of different quantifiers being used.<br>

The ? optional quantifier which was briefly introduced in the preceeding section indicates that the preceeding character is optional. <br>
For example `(https?:\/\/)` indicates that the match can return text that has an s or not. Therefore, all matches of http and https will be returned.<br>

The + matches one or more of the prepending character.<br>
For example `([\da-z\.-]+)` will match one of more of the captured group of digits from 0-9, followed by small case alphabets from a-z, followed by a period and a -. <br>

The {2,6} matches the specified quantity of the prepending character. {2,6} will match 2 to 6. {2} will match only 2.<br>
For example in the group `([a-z\.]{2,6})`, only character sets between 2 and 6 will be matched.<br>

The * matches 0 or more of the prepending character.<br>
For example in the captured group `([\/\w \.-]*)*` will match one of more of the captured group<br>

## Escaped Characters
This is used to insert reserved, special and unicode characters. To use an escaped character a \ must be prepended to the character.<br>
In the first captured group `(https?:\/\/)` the `\/`  will match a forward slash /. `\/\/` will match two forward slashes //.<br>
Another example is the `([\da-z\.-]+)` group. `\.` this is an escaped character that uses the \ prepended to the . character to find a match.<br>

## Grouping and Capturing
When a group of characters are enclosed in parentheses, this is refered to as grouping and capturing.v
This enables substrings to be extracted.<br>
In this tutorial there are 4 capturing groups.<br>
`(https?:\/\/)` - Here the group captured is https:// with the s being optional so http:// will also be matched.<br>
`([\da-z\.-]+)`<br>
`([a-z\.]{2,6})`<br>
`([\/\w \.-]*)`<br>

## Character Classes
Character classes match a characters from a specific set. Example of  character classes are character set, negated set, range, dot, match any, word, not word, digit, not digit.<br>
In this tutorial character set will be discussed in detail.<br>

Character set matches any character enclosed in square brackets [].<br>
There are three character sets in the regular expression. 
`[\da-z\.-]`, `[a-z\.]` and  `[\/\w \.-]`<br>

`[\da-z\.-]` - In this character set there are two character classes digit and range.<br>
digit - `\d` will match any digit character from 0-9 <br>
range - `a-z` will mtach characters in the a-z range. It is case sensitive. <br>

`[a-z\.]` - In this character set there is a range character class and an escaped character. <br>

`[\/\w \.-]`- In this character set there is a escaped character \/ which will match a forward slash /, there is a character class \w, followed by an escaped character \., followed by a literal - character.<br>
word - `\w` will match any word character both alphanumeric and underscore. So a-z, A-Z, and 0-9. <br>

## Author
Jide is a Full Stack Web Developer with experience in coding and electronics. He has obtained Certificate from the UT Austin coding bootcamp and a Mechanical Engineering degree from the University of Texas at San Antonio. Full stack technologies include HTML, CSS, JavaScript, Node.js, while electronics experience include Allen Bradley, Omron and Siemens PLC’s, sensors, servo-motors and all sorts of electro-mechanical devices. He is also  a certified Scrum Master in Agile methodologies, and project management. He is passionate about approaching programming challenges from different angles and collaborating with others to create meaningful web applications.<br>
Connect with Jide on LinkedIn - [Jide's LinkedIn](https://www.linkedin.com/in/jide-ogunbanjo/) <br>
Connect with Jide on Github - [Jide's Github](https://github.com/JideOgun)
