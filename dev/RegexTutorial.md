# Regex Tutorial - Matching URLs

In this guide, we're gonna break down this regex pattern that matches URLs: ^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$. I've seen it used a lot in web dev to check if something's a URL and to pull URLs out of text. Pretty handy stuff!

## Summary
^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$
The regex pattern begins by matching the start of the string with ^. Following this, it looks for either http:// or https:// using (https?:\/\/)?, but this part is optional due to the ?. Next, it captures the subdomain and domain name with ([\da-z\.-]+), which matches one or more alphanumeric characters, dots, or hyphens. A literal dot is then matched using \.. The top-level domain, such as .com or country-code TLDs like .co.uk, is captured with ([a-z\.]{2,6}), which matches between 2 to 6 lowercase letters or dots. The pattern then seeks to capture the path, query, or fragment of the URL using ([\/\w \.-]*), which matches zero or more slashes, alphanumeric characters, spaces, dots, or hyphens. The trailing slash in the URL is made optional with \/?. Finally, the pattern ensures it matches the end of the string with $. In its entirety, this regex is adeptly crafted to match URLs, accommodating various structures and components commonly found in web addresses.

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