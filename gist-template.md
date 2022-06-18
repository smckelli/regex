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

### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
