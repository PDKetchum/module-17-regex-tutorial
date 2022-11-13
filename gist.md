# module-17-regex-tutorial

As a web development student, for regex practice, I created a tutorial on how to understand regex search patterns.

## Summary

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

I will explaining a regex matching an email (shown above).
We can see that the regex has boundries set by the anchors `^` and `$`. There are 3 groups seperated by `()`. In the first group, the regex is looking to match `+` one or more times the below:

- `a-z` - Aphabet characters a-z
- `0-9` - Digits 0-9
- `_\.-` - Special characters \_.- (period escaped with slash)

The regex is then look for `@`

In the second group the regex is looking to match `+` one or more times the below:

- `\d` - Digits 0-9
- `a-z` - Aphabet characters a-z
- `\.-` - Special characters .- (period escaped with slash)

The regex is then look for `.` escaped with slash

In the third group regex is looking to match with a 2-6 character limit `{2,6}`

- `a-z` - Aphabet characters a-z
- `\.` - Special character . (period escaped with slash)

<br/>
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

Regexs are wrapped in slashed characters `/` because they are literals.

<br/>

### Anchors

`^` and `$` are Anchors. The `^` equates to the beginning of the string. The `$` equates the the end of the string.

<br/>

### Quantifiers

Quantifiers set the requirement on how many characters are in the pattern. They show up before the `$` anchor identified by curly brackets `{ }`.

- `{x}` - The characers match exactly `x` times
- `{x,}` - The characters match at least `x` times
- `{x,y}` - The characters match a minimum of `x` times and a maximum of `y` times

<br/>

### OR Operator

`|` is the OR operator. It is used to seperate 2 or more terms with in a group and the pattern matches either term. For example `(dogs|cats)`.

`^I like (dogs|cats).$`

"I like dogs." and "I like cats." both match.

<br/>

### Character Classes

Character Classes describe a set of characters. Below are a few common character classes.

- `.` - Matches all characters excluding newline character
- `\d` - Matches all digits between 0-9
- `\D` - Matches all characters that are not a digit
- `\w` - Matches all alphanumeric charaters including the underscore
- `\W` - Matches all non alphanumeric charaters including the underscore
- `\s` - Matches a single chracter that is a white space
- `\S` - Matches a single chracter that is not a white space
- `\` - The following character escapes their usual roles.

<br/>

### Flags

Flags descrive additional requirements or limits of a regex. Examples below.

- `i` - Ignores casing
- `g` - Searches for all occurences
- `s` - The wild character matches newlines also
- `m` - Matches every single line VS beginning and ending

<br/>

### Grouping and Capturing

When grouping a section of regex, you break the regex into different parts, each of with has their own paramemters. Regex are grouped with `()`.

<br/>

### Bracket Expressions

`[abc]` Matches the characters with in the brackets.
`[^abc]`Excludes the characters in the brackets.

<br/>

### Greedy and Lazy Match

Along side with quantifiers, quantifiers can be greedy or lazy. Greedy means they must macth as many times as possible. Lazy means it matches the least times possible.

- `*`— Matches the pattern zero or more times

- `+`— Matches the pattern one or more times

- `?`— Matches the pattern zero or one time
  <br/>

### Boundaries

Boundries anchor the regex to a begining and end of a string. Using Anchors explained above, we can se tthe boundries for a regex.
<br/>

## Author

Pachia Xiong is an Aspiring software engineer based in Saint Paul, MN.
GitHub: https://github.com/PDKetchum
