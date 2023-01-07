# Regex Tutorial / Computer Science Challenge 17
This tutorial will walk through how regex can be applied to match email addresses using the expression  
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` 

## ***_Summary_***

***Regex*** is short for ***Regular Expression***.  
A regular expression is a sequence of characters that forms a search pattern.  
When you search for data in a text, you can use this search pattern to describe what you are searching for.  
A regular expression can be a single character, or a more complicated pattern.  
Regular expressions can be used to perform all types of text search and text replace operations.
  
## Table of Contents

- [RFC 5322 Standard](#rfc-5322-standard)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Sets](#character-sets)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Resources](#resources)

## ***_Regex Components_***  
<br>   

### ***_RFC 5322 Standard_***
The official standard is known as RFC 5322. It describes the syntax that valid email addresses must adhere to.  
RFC 5322 leaves the domain name part open to implementation-specific choices that won’t work on the Internet today.  
The regex implements the “preferred” syntax from RFC 1035 which is one of the recommendations in RFC 5322.
***It is not recomended to implement the RFC 5322 standard in your code. However you should be aware, that there is an official standard***.   
<br>  

### ***_Anchors_***
The anchors used in this regex expression are `^ `, which indicates the beginning of the string and `$` to indicate the ending of the string.  
/ `^` ([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6}) `$` /  
<br>    

### ***_Quantifiers_***
Quantifiers in this regex includes the `+` operator, which will connect the users email name + email service + `.com`. Another quantifier for this regex includes `{2,6}`, which will allow a match range of 2-6 characters for the character set of `[a-z\.]`.  
/^([a-z0-9_\.-] `+` )@([\da-z\.-]+)\.( `[a-z\.]` `{2,6}` )$/  
<br>  

### ***_Character Classes_***
The character class in this expression is `\d`,  
/^([a-z0-9_\.-]+)@([ `\d` a-z\.-]+)\.([a-z\.]{2,6})$/  
which matches a single characters that is a digit from 0-9.  
<br>  

### ***_Grouping and Capturing_***
Capturing the first group in this expression is `([a-z0-9_\.-]+)` that matches the user email name. The second group that is being captured is `([\da-z\.-]+)` which will match the email service. The last group being captured is `([a-z\.]{2,6})` to get the `.com`.  
/^ `([a-z0-9_\.-]+)` @ `([\da-z\.-]+)` \. `([a-z\.]{2,6})` $/  
<br>  

### ***_Bracket Expressions_***
Bracked expressios for email validation includes the character sets of `[a-z0-9_\.-]`, which is matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters  `_`  ,  `-`  , and  `.` ; `[\da-z\.-]`, which is matching a single digit from 0-9, any character a-z (case senstive), and the characters   `.`   and `-`  . `[a-z\.]` matches any character a-z(case senstive) and the character   `.`  .  
/^( `[a-z0-9_\.-]` +)@( `[\da-z\.-]` +)\.( `[a-z\.]` {2,6})$/  
<br>  

### ***_Greedy and Lazy Match_***
This regrex includes greedy matches. Since it includes the `+` Quantifier, it will match as many times as possible giving back as needed. Another greedy Quantifier used in this regex is `{}` when matching `{2,6}` for the last capture group.  
/^([a-z0-9_\.-] `+` )@([\da-z\.-] `+` )\.([a-z\.] `{2,6}` )$/  
<br>   

### ***_Resources_***
https://regexlearn.com/learn/regex101  
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions  
https://www.w3schools.com/js/js_regexp.asp  
https://javascript.info/regexp-greedy-and-lazy  
https://www.regular-expressions.info/email.html  
<br>  

## ***_GitHubGist_***
https://gist.github.com/wolfjfly