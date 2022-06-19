# Password Strength RegEx

In today's online experience it is ever more important to create passwords that are difficult crack with a mind to cyber sercurity. The level of password complexity should increase with the sensitivity of the data being protected. Therefore, what follows is a description of the RegEx that will ensure the minimum level of password strength a user can put in the UI.

## Summary

The 'Complex Password Strength' RegEx should ensure the establishment of passwords that contain- at a minimum- 1 lowercase letter, 1 uppercase letter, 1 number, 1 special character, and be at least 8 characters long. Of course passwords can be (and should be) more complex than the minimum defined here but this RegEx will even verify those more complex passwords we should be creating. The actual RegEx for the 'Complex Password Strength' is:

**/(?=(.*[0-9]))(?=.*[\!@#$%^&*()\\[\{}\-_+=~`|:;"'<>,./?])(?=.*[a-z])(?=(.*[A-Z]))(?=(.*)).{8,}/** 

We will break down this RegEx below and explore its components a little more below...


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

In looking at the code in the summary we see the expression begins and ends with a slash (/). These slashes define the expression as a Regular Expression Literal. From there, as we scan the expression from left to right, we can indentify the various components of the expression. These components have important roles in the expression.


**?=** - Repeated component- Positive lookahead that ensures the input matches the following expression without returning it.
**.** - Repeated component- Wildcard matching. This position will match any combination of **numbers**, **special characters**, **lowercase**, **uppercase** characters and ensures the minimum **length** of 8 characters in the password.
__*__ -  Repeated component- Matches 0 or more repetitions of...
**[0-9]** - Any number, 0 through 9...
**[\!@#$%^&*()\\[\{}\-_+=~`|:;"'<>,./?]** - Any special character...
**[a-z]** - Any lowercase letter...
**[A-Z]** - Any uppercase letter...
**{8,}** - Minimum of 8 characters


### Anchors

**^** and **$** are used to indicate the start and end (respectively) of the line. An anchor generally means that the current position in the string matches a certain position...the beginning, the end, or the positionimmediately following the last match.
### Quantifiers

__*__ is an example of a quantifier. A quantifier will specify you many instances of the group, character or character class muxt be present in the input to be considered a match. In this case, the 'Complex Password Strength', the * is looking to match the element zero or more times. Other quantifiers can include:

**+** or **+?** - Match 1 or more times
**?** or **??**- Match zero or 1 time.
**{n}** or **{n}?** - Match exactly n times.
**{n,}** or **{n,}?**- Match at least n times.
**{n,m}** or **{n,m}?**- Match between n and m times.

### OR Operator

The 'OR' operator in regex is represented by the pipe (**|**) symbol on the keyboard, This operator will return any one of a series of various and sundry single characters. For example, (**a|e**) will match either an 'a' or an 'e'.

### Character Classes

A character class defines a set of characters. Examples of character classes are:

**Positive Character Groups**
**Negative Character Groups**
**Any Character**
**A General Unicode Category or Named Block**
**A Negative General Unicode Category or Named Block**
**A Word Character**
**A Non-Word Character**
**A White-Space Character**
**A Non-White-Space Character**
**A Decimal Digit**
**A Non-Decimal Digit**

### Flags

Flags in RegEx enhance the search capabilities. Specifically these flags have specific functionality:

**d** - Generates indices for substring matches
**g** - Global Search
**i** - Case-sensitive search
**m** - Multi-line search
**s** - Allows **.** to match newline characters
**u** - Unicode--Treats a pattern as Unicode characters
**y**- Performs a sticky search that matches starting at the current postion in the target string

### Grouping and Capturing

Capturing groups is a way to treat multiple characters as a single unit, like in parentheses (i.e **(dog)**). 
### Bracket Expressions

### Greedy and Lazy Match

A greedy quantifier (or match) tries to match as many instances of the element as possible while a lazy quatifier (or match) tries to match as few as possible. For example, the __*__ quantifier is considered a 'greedy match' or 'greedy quantifier' because it will look for as many instances of the match as possible. 

The quantifier __*?__ is considered a 'lazy quatifier' or a 'lazy match' as it is looking for as few matches as possible.

### Boundaries

A boundary tells us what can be matched to the left or right of the current position. The most common use of a boundary is a word boundary where **/b** matches conditions in which one side is a word character (like a letter) and the other side is not a word character (like a space).

### Back-references

A back-reference refers to the most recent definition of a group or the most recent capture.

### Look-ahead and Look-behind

Understanding that a 'look-around' looks for some parts of a text string, a 'look-ahead' is looks at the patern ahead of the desired match. A 'look-behind' is when the pattern occurs before the desired match.

## Author

I am Scott McKellips and this Bootcamp is really my first in-depth exposure to programming. I have had some experience with FORTRAN and Pascal, Apple Basic and Unix but that exposure was somewhat limited and a long time ago. I have a bit of experience as a technician and 'Engineer' (CDMA Call Processing, SATCOM, Spread Spectrum, etc) but I haven't utilized thos skills in over 2 decades. I have spent more than 25 years in the United States Army and as a government civilian in the Department of Homeland Security leading people. I am now approaching retirment age and looking for something I can do remotely and from anywhere in the world. Software Development seems to be a profession that fits that bill.


## Research links

https://docs.microsoft.com/en-us/dotnet/standard/base-types/quantifiers-in-regular-expressions
https://www.rexegg.com/regex-boundaries.html
https://www.section.io/engineering-education/password-strength-checker-javascript/
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions
https://docs.oracle.com/javase/tutorial/essential/regex/groups.html
https://betterprogramming.pub/demystifying-look-ahead-and-look-behind-in-regex-4a604f99fb8c

