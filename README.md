# Regex Tutorial Starter Code
This tutorial is going to explain the use of regex to match emails using the expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. 

## Summary

A regular expression is a sequence of characters that defines a search pattern. This is commonly used to find patterns within a string, find/replace characters within a string or validate input. This tutortial will go walk through the components of a regex and how it applies to matching an email. 

## Table of Contents

- [Regular Expression](#regular-expression)
- [RFC 5322 Standard](#rfc-5322)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Sets](#character-sets)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Resources](#resources)

## Regex Components

### Regular Expression
Regex is short for Regular Expression.  
A regular expression is a sequence of characters that forms a search pattern.  
When you search for data in a text, you can use this search pattern to describe what you are searching for.  
A regular expression can be a single character, or a more complicated pattern.  
Regular expressions can be used to perform all types of text search and text replace operations.  

### RFC 5322 Standard
The official standard is known as RFC 5322. It describes the syntax that valid email addresses must adhere to.  
RFC 5322 leaves the domain name part open to implementation-specific choices that won’t work on the Internet today.  
The regex implements the “preferred” syntax from RFC 1035 which is one of the recommendations in RFC 5322.
It is not recomended to implement the RFC 5322 standard in your code. However you should be aware, that there is an official standard. 

### Anchors
The anchors used in this regex expression are `^ `, which indicates the beginning of the string and `$`to indicate the ending of the string.  
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` 

### Quantifiers
Quantifiers in this regex includes the `+` operator, which will connect the users email name + email service + `.com`. Another quantifier for this regex includes `{2,6}`, which will allow a match range of 2-6 characters for the character set of `[a-z\.]`.  
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Character Classes
The character class in this expression is `\d`,  
'`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`'  
which matches a single characters that is a digit from 0-9. 

### Grouping and Capturing
Capturing group #1 in this expression is `([a-z0-9_\.-]+)` that matches the user email name. The second capturing group is `([\da-z\.-]+)` which will match the email service. Then lastly, capture group #3 is `([a-z\.]{2,6})` to capture the `.com`.
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Bracket Expressions
Bracked expressios for email validation includes the character sets of `[a-z0-9_\.-]`, which is matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters "_" , "-" , and "."; `[\da-z\.-]`, which is matching a single digit from 0-9, any character a-z (case senstive), and the characters "." and "-".; `[a-z\.]` matches any character a-z(case senstive) and the character ".". 
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Greedy and Lazy Match
This regrex includes greedy matches. Since it includes the `+` Quantifier, it will match as many times as possible giving back as needed. Another greedy Quantifier used in this regex is `{}` when matching `{2,6} for the last capture group.
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`  

### Resources
https://regexlearn.com/learn/regex101  
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions  
https://www.w3schools.com/js/js_regexp.asp  
https://javascript.info/regexp-greedy-and-lazy  
https://www.regular-expressions.info/email.html  

## Author
You can view my projects at https://github.com/wolfjfly.

^ matches the starting of the sentence.   
[a-zA-Z0-9+_.-] matches one character from the English alphabet (both cases), digits, “+”, “_”, “.” and, “-” before the @ symbol.   
+ indicates the repetition of the above-mentioned set of characters one or more times.   
@ matches itself.   
[a-zA-Z0-9.-] matches one character from the English alphabet (both cases), digits, “.” and “–” after the @ symbol.   
$ indicates the end of the sentence.   
# Match an Email - Regex Tutorial    
