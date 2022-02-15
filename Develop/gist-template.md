# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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
* Anchors tell the expression where to begin and end a query.
* One type of anchor is the "^" or caret which tells the expression that this is the begining of what we are searching for.
* On the other end we have "$", which marks the end of the search parameteres.

### Quantifiers
* Quantifiers tell the expression to look for matches under certain conditions
* These can tell the expression to only look for so many characters. This would be the {} operators. In our expression the "{2,6}" tells the expression that we are looking for between 2 and 6 instances of a-z followed by a period.
* The + sign in a regular expression looks for something occuring one or more times. In our expression the + guarantees that we will accept data that is not blank, and gives us the ability to take in multiple singluar characters within a bound.


### OR Operator
* The or operator allows an expression to look for what infront or behing it. So 1|2 would find any 1 or 2 in the data that is being worked with.

### Character Classes
* Class characters are sets of characters that the expression will look for.
* In our expression this is used multiple times, but lets just look at [\da-z\.-]+. The class characters in this portion are looking for digits(\d), any letter of the alphabet (a-z), a period (\.), and a hyphen (-). This will accept any one character that fits that criteria, and the + at the end will look for 1 or more instances of these parameters.

### Flags
* Flags are ways to change the way in which the expression is searching.
* These flags can be used to ignore casing (i), look at multiple lines while ignoring line breaks (m), and (g) global which searches through all occurances.

### Grouping and Capturing
* Grouping allows for an expression to search specifically for what is in a group of parenthesis. This allows for regex code to get more or less specifc based on their needs.
* In our expression grouping is used multiple times to chop up and specify what we're looking for in every portion of the equation. In our expression /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ each set of parenthesis has different search parameters because an email is made up of different varying parts.

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)



432314213213123