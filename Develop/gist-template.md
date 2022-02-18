# Regex Tutorial

Regex or regular expressions is a powerful tool that lets the user find text in a file. While this sounds a bit underwhelming at first, the extent to which you can narrow down your search is an invaluable tool when searching through a large amount of text. These expressions are bookended by `/`'s and are made of many different components, many of which are present in this tutorial.

## Summary

The regex that we are using for this tutorial is used for validating email addresses: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. This may look like an absolute mess, but it can be broken down into more bite sized components. The first portion `/^([a-z0-9_\.-]+)` looks at the username portion of the email, so everything before the `@` sign. Next we have the `@` itself followed by `([\da-z\.-]+)\.` which represents the site that the email is being sent. Lastly we have `([a-z\.]{2,6})$/` which looks at the domain, often this is `.com` but there is a wide variety of different domains that are valid. Now that we have an overview of our regex, we can get down to the nitty gritty of regular expressions.

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
* One type of anchor is the `^` or caret which tells the expression that this is the begining of what we are searching for. In our expression we can see this in the first chunk of code `/^([a-z0-9_\.-]+)`
* On the other end we have `$`, which marks the end of the search parameteres. This also appears in our regex, of course at the end `([a-z\.]{2,6})$/`.

### Quantifiers
* Quantifiers tell the expression to look for matches under certain conditions
* These can tell the expression to only look for so many characters. This would be the {} operators. In our expression the `{2,6}` tells the expression that we are looking for between 2 and 6 instances of a-z followed by a period.
* The + sign in a regular expression looks for something occuring one or more times. In our expression the + guarantees that we will accept data that is not blank, and gives us the ability to take in multiple singluar characters within a bound.

<!-- ### OR Operator
* The or operator allows an expression to look for what infront or behing it. So 1|2 would find any 1 or 2 in the data that is being worked with. -->

### Character Classes
* Class characters are sets of characters that the expression will look for.
* In our expression this is used multiple times, but lets just look at `[\da-z\.-]+`. The class characters in this portion are looking for digits(\d), any letter of the alphabet (a-z), a period (\.), and a hyphen (-). This will accept any one character that fits that criteria, and the + at the end will look for 1 or more instances of these parameters.

<!-- ### Flags
* Flags are ways to change the way in which the expression is searching.
* These flags can be used to ignore casing (i), look at multiple lines while ignoring line breaks (m), and (g) global which searches through all occurances. -->

### Grouping and Capturing
* Grouping allows for an expression to search specifically for what is in a group of parenthesis. This allows for regex code to get more or less specifc based on their needs.
* In our expression grouping is used multiple times to chop up and specify what we're looking for in every portion of the equation. In our expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` each set of parenthesis has different search parameters because an email is made up of different varying parts.

### Bracket Expressions
* Brackets denote that any one thing that matches, it will accept. For example when we see [a-z\.] that means the express will accept any letter a-z as well as a literal period. 

### Greedy and Lazy Match
* Greedy and lazy matches are used to let the expression know how many characters to look for.
* The greedy operators are ` * `, `+`, and `{}`. Our first operator ` * ` will accept 0 or more of the last operator it is attached to. This also works with the brackets to expand your search as seen in our expression. The `+` operator checks for 1 or more of the operator that precedes it. Lastly the brackets will give a range for how many instances it is looking for. So the {2,6} we see in the expression is saying to find between 2 and 6 characters that match [a-z\.].
* The lazy match works similarly, but in the opposite direction. For example the `?` operator will look for 0 or 1 of the previous operator. This means that it can skip over this section since 0 is a vaild number of results.

<!-- ### Boundaries
* Boundaries work a lot like the `$` and `^` operators in that they denote an exact match to whatever is inbetween them. These boundaries are `\b` and `\B`, `\b` will look for exactly what is sandwiched inbetween the set of boundaries and nothing before or after that. The capitol `\B` will invert this, looking at text that is surrounded by other characters.

### Back-references
* Back references look at previous matching groups and seaches for the same text as that group. For example the expression ([abc])\1 will look for a, b, or c followed by another search for a, b, or c. This lets expression define parameters once and then reuse them later if needed.

### Look-ahead and Look-behind
* Regex can also look for a character before or after a character of your choosing. For examle the line c(?=k) will only match if there is a c followed by specifically a k. To look infront of a character you use (?<=k). These can also be used with negation operators c(?!k) meaning you can search for c that is not followed by a by a k.  -->

## Author

* Hi, my name is Nick and I hope you enjoyed my Regex tutorial. I am an aspiring full stack developer looking to develop my coding and problem solving skills. 
* GitHub: https://github.com/NickNocc





