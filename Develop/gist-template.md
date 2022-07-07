# Title (Learning Regex)

A Regular expression or (Regex) is a string of text that allows you to create patterns that help manage, locate, and match text.They started in the 1940s as a way to describe regular languages, but they really bursted onto the programming world during the 1970s.  Regular expressions are used in search engines, in search and replace dialogs of word processors and text editors. In this tutorial we will take a deeper look at Regex and understand how they work.




## Summary

In this tutorial we are going to break down the email regex below. We will break down the different parts of the Regex from the Anchors, Quantifiers, Character Classes, Grouping and Capturing, and Bracket Expressions. We will learn how we get from the email regex below to jl20@gmail.com


/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)


## Regex Components

### Anchors

Anchors have special meaning in regular expressions. Anchors are at the beginning and end of the regex. They are a special character as they do not match any of the characters in the Regex. Instead, they are position before or after characters. So in the case of this email regex example:

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/

"^" is the caret anchor signifies the beginning of the text.
"$" is the dollar anchor signifies the end of the text.
We often use anchors to check if a string fully matches the pattern. We will discuss what goes between the anchors further along in this tutorial.

### Quantifiers

Quantifiers match a number of instances of a character, group, or character class in a string.
Quantifiers take will tkae any symbol or group of symbols and multiply it by the quantity you're looking for. From the example above the quantifier in our case will be "{2,6}". In the example before the Quantifier we see "a-z" and "." . So in our case the string has to have between 2 and 6 characters containing either 'a-z' character, '', or '.'




### OR Operator

The OR operator is defined in the regex using "|". This is typically used for a set of operands is true if and only if one or more of its operands is true.  Lets take a look at this example  "/^#?([a-f0-9]{6}|[a-f0-9]{3})$/". This shows an OR Operater is being used because ' | ' means that the search engine wants to find hex codes that are either 6 or 3 digits or letters.





### Character Classes

Character classes distinguish kinds of characters such as, for example, distinguishing between letters and digits. In our email regex above we can see "\d". Chararacter sets are defined by a \ followed by a letter to represent either a digit, letter, symbol, or a period. In our email regex we see a \d class meaning that the regex will have to match a single digit or character from 0-9.


### Flags
A flag variable, in its simplest form, is a variable you define to have one value until some condition is true, in which case you change the variable's value. It is a variable you can use to control the flow of a function or statement, allowing you to check for certain conditions while your function progresses. An example of a flag would be the g variable which means global search.



### Grouping and Capturing

Grouping is defined using "()" to seperate elements calling the array according to the string values of the testing functions. In simpler terms it is dividing the arrays using a parenthesis. Let's take a look at our email regex from above " /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/". As you can see we have 3 groups ([a-z0-9_.-]+), ([\da-z.-]+), and ([a-z.]{2,6}). We can also see that the "@" and "." symbol are not in any of the groups. Emails have a an "@" symbol then having the email provider after. So after the @ symbol we will get the service provider in the following group. This is similar with the "." symbol which is after the service provider. So to break this down a little further the first group "([a-z0-9_.-]+)" would be the first part of your email address, second group "([\da-z.-]+)" would be the "yahoo" or "gmail", and the last group would usually be the "com".




### Bracket Expressions

Bracket Expressions tell a set of characters to match. Any individual character between the brackets will match. You can also use a hyphen to define a set. From we see both ranges [0-9] and [a-z]. For the first bracket this means the expression will search for any digit between 0-9 and for the second bracks the regex will try to serach all alphabetical letters that match between a and z.

### Greedy and Lazy Match

"Greedy" means match the longest possible string and "Lazy" means match the shortest possible string. Our email Regex does not have a Greedy or Lazy match.





## Author

Jide Adesanya
Github: https://github.com/Jide1012


