# Matching a Hex Value

## Summary

By using this regex, i's possible to match hexadecimal values (hex values)

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

## Table of Contents

- [Matching a Hex Value](#matching-a-hex-value)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [OR Operator](#or-operator)
    - [Character Classes](#character-classes)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
    - [Greedy and Lazy Match](#greedy-and-lazy-match)
  - [Author](#author)

## Regex Components

### Anchors
Code: `/^#`

Description:

This anchor is used to mark what the expression begins with. In reference to hex values, Using the ^ anchor, it tells the expression that it must use the # character, which is used within Hex values.

Code: `$/`

Description:
Similar to the ^ anchor, the $ anchor tells the expression what it must end with, rather than begin with. In this example, it tells the expression that the end of the expression must match the structure of the hex value.

---

### Quantifiers
Code: `/^#?`

Description: 

By adding the ?, it marks a true/false statement with the preceeding anchor, meaning that the # used with most hex values is not necessary for the particular regex expression, but can be added if wanted. 

Code: `{}`

Examples: `[a-f0-9]{6}` and `[a-f0-9]{3}`

Description:

The quantifier tells the expression how many times the preceeding pattern must appear. Using the above examples, `[a-f0-9]{6}` means that there will be 6 instances of any character within the ranges indicated within the square brackets (a mix of 6 letters between a-f and numbers between 0-9). By adding in the second example, `[a-f0-9]{3}` directly after the first expression, it tells the regex that there will be 3 instances of that first expression.

---

### OR Operator

Code: `[a-f0-9]{6} | [a-f0-9]{3}`

Description:

By adding in the OR operator, it tells the expression that it will match with either version. This means that a match will return true if there is a combination of 6 characters between the ranges given `#1a2b3c`OR if there is a combination of 3 characters between the ranges `#aaa`.

---

### Character Classes

Code: `a-f0-9`

Description:

The Character classes indicate what is acceptable to be given to the match. In this example, since a hex value only contains letters between `a-f` and numbers between `0-9` this specific class puts those limits in place.

---

### Grouping and Capturing

Code: `([a-f0-9]{6} | [a-f0-9]{3})`

Description:

By encompassing the entire expression in `()`, it acts a way to group the expressions together.

---

### Bracket Expressions

Code: `[a-f0-9]`

Description: 

Adding the ranges into square brackets indicate that the regex will match a specific character pattern, and adding in the `-` will give a range of acceptable characters. In this example, the regex will take in any letters between `a-f` and any numbers between `0-9`.

---

### Greedy and Lazy Match

Greedy Code: `[a-f0-9]{6}`

Lazy Code: `[a-f0-9]{3}`

Description:

With these expressions, Greedy means that the expression will get the longest possible string of characters. In this example, that would be a 6 character string containing characters and numbers within the range. Conversly, Lazy means that the expression will get the shortest possible string of characters. In this example, the shortest would be a combination of 3 characters and numbers within the range. 

---

## Author

Author Name: Julian Benchimol
[GitHub Profile](https://github.com/julianbenchimol)
