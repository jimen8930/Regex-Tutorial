Regular Expression - Confirming an Email

Regular expressions, commonly known as regex, are distinct strings composed of various character sets. They serve as query tools and validators within codebases and traditional documents. Regular expression function as tools to identify patterns in text files. Despite their initially cryptic appearance, regular expressions can be broken down into manageable components, revealing that they are not as intricate as they may seem to beginners.  expressions.

## Summary

This tutorial will be covering the regex expression used for both matching and cofirming an email: 

^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$

The provided regular expression can also be applied as a text sequence in a code repository to validate and match an email address. This technique ensures that users cannot proceed in situations where valid email addresses are required for form completion. By incorporating the regex sequence, users are compelled to enter an unspecified count of characters, succeeded by an "@" symbol, followed by a domain name of unspecified length. Additionally, the domain name system (for example, ".com," ".net," ".dev," etc.) must have a length between 2 and 6 characters as demonstrated in this instance.

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
The building blocks of this specific expression include anchor points, quantifiers, meta escape characters, character classes, individual character matches, grouping and capturing, as well as bracket expressions.
Based on the provided tutorial example, the anchor points "^" and "$" are employed. Quantifiers such as "+" and "{2, 6}" are used. The meta escape character "\d" is utilized. Character classes are represented by "[a-z0-9_.-]," "[\da-z.-]," and "[a-z.]." Individual character matches are symbolized by "_," ".," and "-." Grouping and capturing are denoted by "()" and the bracket expression is illustrated by "[]."

### Anchors
Anchors within regex mark the start and end points of the expression. In regards to this expression, the ^ marks the start of the expression and the $ marks the end of the expression.

### Quantifiers
Quantifiers in regex are symbols or meta-characters that indicate the number of times a preceding element should be matched. They allow you to specify how many occurrences of a particular character or group of characters are required in the input string for a match to occur. 

-  + after [a-z0-9_\.-]: This quantifier matches one or more occurrences of any lowercase letter, digit, underscore, dot, or hyphen.

-  + after ([\da-z\.-]+): This quantifier matches one or more occurrences of any digit, lowercase letter, dot, or hyphen within the group.

{-  2,6} after [a-z\.]: This quantifier specifies that the character class [a-z\.] should repeat between 2 and 6 times. This is used for the domain name system (e.g., ".com," ".net," ".dev").

### OR Operator
There are no OR operators within this particular regex expression. OR operators are represented with the pipe | and specified under the regex type of alternation.

### Character Classes
In a regex code, a character class is a way to define a set of characters that can be matched within a single position in the input string. Character classes allow you to specify a range of characters that could appear at that particular position. 
The character classes utilized in this regex expression are [a-z0-9_\.-], [\da-z\.-], and [a-z\.].

Character classes are enclosed in square brackets `[ ]` and can contain various types of characters or character ranges. Here are some examples of character classes and what they represent:

-  `[a-z]`: This character class matches any lowercase letter from 'a' to 'z'.
-  `[A-Z]`: This character class matches any uppercase letter from 'A' to 'Z'.
-  `[0-9]`: This character class matches any digit from 0 to 9.
-  `[\d]`: This shorthand character class also matches any digit (equivalent to `[0-9]`).
-  `[a-zA-Z]`: This character class matches any letter, either lowercase or uppercase.
- `[a-zA-Z0-9]`: This character class matches any alphanumeric character.

### Flags
The regex expression covered in this tutorial does not utilize flags.

In a regex, flags are modifiers that you can apply to a regex pattern to change how the pattern is interpreted or how the matching process behaves. These flags allow you to control various aspects of regex matching.

There are only 6 of them in JavaScript -> i: case-sensitivity, g: looks for all matches, m: multiline mode, s: enables "dotall" mode that allows a dot . to match a newline character \n, u: enables full Unicode support, and y: "sticky" mode.

### Grouping and Capturing
In regex, grouping and capturing are techniques that allow you to create subpatterns within your main pattern. 
() creates a sequence or sub expression and is a way to treat multiple characters as a single unit. You will notice the regex expression being covered in this tutorial uses () to distinct groups of characters. The first set covers all characters before the @ symbol. The second group coveres all characters before the ., and the last group covers all characters from the . to the end.

### Bracket Expressions
In the regex, brackets and expressions refer to the use of square brackets [ ] to define character classes or sets of characters that can be matched within a specific position in the input text. 

[] create a character or group range and represent a single character. In regards to the regex expression this tutorial is covering, the brackets are used to separate each character class. The character can be anything specified within the brackets.

Example: [a-z0-9_\.-] -> this character can be matched with any lowercase letters from a-z, and digit from 0-9, an underscore _, a period ., or a dash -.


### Greedy and Lazy Match
In a regex, greedy matching is a default behavior where the regex engine will try to match a much of the string as possible, while lazy matching will try to match as little of the string as possible.

Greedy will keep searching until the condition is satisfied while lazy will stop searching once the condition is satisfied.

### Boundaries
In a regex, \b is an example of a word boundary. It usually represents matching positions on either side; where once side is a word character and the other is something other than a word character.

### Back-references
In a regex, back-references are commands which refer to a previous part of the matched regualr expression. It is usually specified with a backslash and a single digit  ex: \2
### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
