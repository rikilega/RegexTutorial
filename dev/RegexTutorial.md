# Regex Tutorial - Matching URLs

In this guide, we're gonna break down this regex pattern that matches URLs: `^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$` I've seen it used a lot in web dev to check if something's a URL and to pull URLs out of text. Pretty handy stuff!

## Summary

`^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`

The regex pattern begins by matching the start of the string with `^`. Following this, it looks for either `http://` or `https://` using `(https?:\/\/)?`, but this part is optional due to the `?`. Next, it captures the subdomain and domain name with `([\da-z\.-]+)`, which matches one or more alphanumeric characters, dots, or hyphens. A literal dot is then matched using `\.`. The top-level domain, such as `.com` or country-code TLDs like `.co.uk`, is captured with `([a-z\.]{2,6})`, which matches between 2 to 6 lowercase letters or dots. The pattern then seeks to capture the path, query, or fragment of the URL using `([\/\w \.-]*)`, which matches zero or more slashes, alphanumeric characters, spaces, dots, or hyphens. The trailing slash in the URL is made optional with `\/?`. Finally, the pattern ensures it matches the end of the string with `$`. In its entirety, this regex is adeptly crafted to match URLs, accommodating various structures and components commonly found in web addresses. I will run through each of the elements for our example below.


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
Anchors are used to specify the position of the pattern in relation to a line of text.

^ denotes the start of a line.
$ denotes the end of a line.
In our URL regex, ^ and $ are used to match the entire line. This means the pattern will only match if the entire line is a URL
### Quantifiers
Quantifiers
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.

? means the preceding item is optional and will be matched, at most, once.
* means the preceding item will be matched zero or more times.
+ means the preceding item will be matched one or more times.
In our URL regex, (https?:\/\/)? means http:// or https:// is optional.

### Character Classes
Character classes match one character out of a set of characters.

\d matches any digit (equivalent to [0-9]).
a-z matches any lowercase letter.
A-Z matches any uppercase letter.
. matches any character except newline.
In our URL regex, [\da-z\.-]+ matches one or more alphanumeric characters, dots, or hyphens.

### Grouping and Capturing
Grouping and Capturing
Parentheses () are used for grouping and capturing.

Groups allow us to apply quantifiers to entire patterns, or to restrict alternation to part of the pattern.
Captured groups are automatically assigned a number and can be referenced with \n.
In our URL regex, ([\da-z\.-]+) is a group that matches the domain name.
### Bracket Expressions
Bracket Expressions
Bracket expressions [...] match a single character out of the set of characters enclosed by the brackets.

In our URL regex, [a-z\.]{2,6} matches a string of 2 to 6 lowercase letters or dots.
### Greedy and Lazy Match
Greedy and Lazy Match
Greedy quantifiers match as many instances of the pattern as possible.
Lazy quantifiers match asfew instances of the pattern as possible.
In our URL regex, * is a greedy quantifier. It matches as many instances of the preceding pattern as possible. For example, ([\/\w \.-]*) matches any number of slashes, alphanumeric characters, spaces, dots, or hyphens.

## Author

[Richard Aspinall](https://github.com/rikilega), is a developer with 5 months of experience. If you would like to reach him for any reason please feel free to contact him at [rikilega](https://github.com/rikilega).