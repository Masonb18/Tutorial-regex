# Basic Regex
In the most basic beginner formant, this tutorial should be ale to teach you reader/user how to format basic regualar expressions.



## Summary

This regex pattern can be used to match strings that start with at least 3 alphabetic characters, followed by 2 to 3 numeric characters, an optional word, and ending with one or more special characters. This example is just for demponstratived purposes and may not have a practical use. Regex patterns depend on specific requirements based on input data.
Here is what the the regex would look like in it's entirety. 
 `/^([A-Za-z]{3,})\s([0-9]{2,3})\s?(\w+)?\s?[!@#$%^&*()]+$/`


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

Anchors are used to match specific positions in a string. The most common anchors are the caret (^), which matches the start of a string, and the dollar sign ($), which matches the end of a string.
Using the carrot `^` and the beginning and the dollar sign `$` and the end of the string; ensures that the pattern matched the whole string.


### Quantifiers

Quantifiers specify the number of times a character or group should be matched. For example, the asterisk (*) indicates zero or more occurrences, the plus sign (+) indicates one or more occurrences, and the question mark (?) indicates zero or one occurrence.
Putting `{3,}` after `[A-Za-z]` specifies that the previous character class should occur at least 3 times.
As well as using `{2,3}` after `[0-9]` specifies that the previous character class should occur between 2 and 3 times.



### Grouping Constructs

Grouping constructs allow you to group multiple characters or patterns together and treat them as a single unit. Parentheses () are used to define groups. This allows you to apply quantifiers and other operators to the entire group.
`([A-Za-z]{3,})` captures a group of alphabetic characters with a length of at least 3.
`([0-9]{2,3})` captures a group of numeric characters with a length between 2 and 3.
`(\w+)?` captures an optional group of word characters.
The difference in specifications is because you are puting the parentheses around that section.



### Bracket Expressions

 Bracket expressions, also known as character classes, allow you to define a set of characters to be matched. For example, [a-z] matches any lowercase letter, [0-9] matches any digit, and [aeiou] matches any vowel.
 `[A-Za-z]` matches any alphabetic character.
`[0-9]` matches any numeric character.
`(\w+)` matches any word character (alphanumeric and underscore).



### Character Classes

Character classes are similar to bracket expressions but provide shorthand notations for common character sets. For example, \d matches any digit, \w matches any word character (letter, digit, or underscore), and \s matches any whitespace character. You can also use capital letters for other specifications.



### The OR Operator

The OR operator (|) allows you to specify multiple alternative patterns. It matches either the pattern on its left or the pattern on its right.
In this specific example the or opoerator is not being used. 
An example of this would be `(color|colour)` depending on the spelling it will match both options. 


### Flags

 Flags are used to modify the behavior of a regex pattern. Common flags include "g" (global), which allows multiple matches, and "i" (case-insensitive), which ignores case when matching.
 In this specific example the or opoerator is not being used.
 For example `/hello/i` would match with 'hello', 'Hello', 'HELLO'.


### Character Escapes

Character escapes are used to match special characters or represent characters that have special meanings in regex. For example, . matches a literal dot character, ^ matches a literal caret character, and \s matches a whitespace character.
`\s` matches a whitespace character.
`[!@#$%^&*()]+` matches one or more occurrences of the specified special characters.



## Author


