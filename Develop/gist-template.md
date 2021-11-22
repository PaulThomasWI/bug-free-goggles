## RegEx Tutorial

This tutorial will describe how to understand the various parts of a validating / verifying a e-mail address regular expression.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary. A regex or REGular EXpression is a sequence of characters that specifies a search pattern. America mathematician Stephen Cole Kleene was the first person to formalize the description.

There are four parts for an email address which include the username, an @ symbol, domain name, a dot, and the domain.

email: paul@theseusgrp.com

username: paul  
@ symbol  
domain name: theseusgrp  
.  
domain: com  

^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$ 

username: ([a-z0-9_\.-]+) / match any lowercase letter or digit 0 through 9 or .  
@ symbol: @  
domain name: ([\da-z\.-]+)  
matches dot character: \. 
domain: ([a-z\.]{2,6})

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

Anchors have special meaning in regex. They do not match any character. Instead, they match a position before or after characters.

- ^ the caret anchor matches the beginning of the text.
- $ the dollar anchor matches the end of the text.

### Quantifiers

Quantifiers match a number of instances of a character, group, or character class in a string.

Exact {n} \d{4} - match four digits  
Range {n, m} \d{2,4}/g - match two, three, or four digits

For the email address reg ex we have a {2,6} quantifier.

### OR Operator

### Character Classes

A character class allows you to match any symbol from a certain character set. A character class is also called a character set. Suppose that you have a phone number like this:

+1-(408)-555-0105
And you want to turn it into a plain number:

14085550105

let phone = '+1-(408)-555-0105';  
let re = /\d/g;

let numbers = phone.match(re);  
let phoneNo = numbers.join('');

console.log(phoneNo);

### Flags

### Grouping and Capturing

Grouping is denoted by by parentheses, it unifies a pattern or string to be matched in a complete block.

### Bracket Expressions

[a-z0-9_\.-] a-z indicates we are looking for lowercase a through z, 0-9 indicates we are looking for 0 through 9, and we literal match special characters "_" underscore, "\." dot, and "-" hyphen.  
[\da-z\.-] indicates we are looking for "\d" 0 through 9, "a-z" a through z, "\." dot, and "-" hyphen.  
[a-z\.] indicates we are looking for "a-z" a through z, and "\." dot.

### Greedy and Lazy Match

### Boundaries

The \b is an anchor. The following three positions qualify as boundaries:  
1. Before the last character in a string if the first character is a word character.
2. After the last character in a string if the last character is a word character.
3. Between two characters in a string if one is a word character and the other is not.

### Back-references

### Look-ahead and Look-behind

## Author

Paul Thomas is a husband, father, brother, friend who grew up in Rockford, IL but now lives in Northeast Wisconsin. After getting a BS-Computer Science degree from Northwest Missouri State University Paul went on to work as the lead web developer for Plexus Corp. a multi-billion contract manufactuer in Neenah, WI. He was cherry picked away by a former Plexus executive to Healthcare where for the last 15 years he ran the technical operations of a $100M orthopedic group. Missing his development roots Paul took it upon himself to learn a new stack and focus on giving back for his last decade of full-time work.

You can learn more about Paul @  
GitHub | https://github.com/PaulThomasWI   
LinkedIn | https://www.linkedin.com/in/paulthomaswi/  
Facebook | https://www.facebook.com/paul.thomas.osi