# Regex: Email Patterns
Regular Expressions, also known as "Regex," is a tool in web development ensuring that the data we come across follows certain patterns and standards. In a world where practically every online platform requires user registration, email pattern matching is one of the most common uses for regex. Understanding regex patterns is crucial whether you're trying to verify email inputs in a form or filter through a big dataset to retrieve email addresses. This lesson provides a step-by-step explanation of its components. 

## Summary
The regex pattern: 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` 

is designed to validate email addresses. It ensures that:
1. The email starts with a combination of letters, numbers, underscores, dots, or hyphens.
2. Followed by the "@" symbol.
3. After which, there's the domain part that can include numbers and letters.
4. Finally, it checks for a domain extension like ".com" or ".org" that is between 2 to 6 characters long.

## Table of Contents
- [Regex Components](#regex-components)
- [Anchors](#anchors)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [Flags](#flags)
- [Grouping Constructs](#grouping-constructs)
- [OR Operator](#or-operator)
- [Character Escapes](#character-escapes)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Author](#author)

## Regex Components
Anchors, quantifiers, meta escape characters, character classes, single character matches, grouping and capturing, and bracket expression are the regex elements that make up this specific expression. Referring to the tutorial's example: The anchors are `^` and `$`, the quantifiers are `+` and `{2, 6}`, the meta escape character is `\d`, the character classes are `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]`, the single character matches are `_`, `\.`, `-`, the way our regex utilizes grouping and capturing is with `()`, and the brakcet expression is designated by `[]`.

## Anchors
In regex, anchors pinpoint the beginning and end of the expression. For this specific expression, `^` indicates the start, while `$` signifies the end.

## Bracket Expressions
In regex, square brackets denote a range of characters to match; for example, `[a-z]` matches lowercase letters, `[0-9]` matches numbers, and `[_-]` matches underscores or hyphens. When combined as `[a-z0-9_-]`, it matches strings with any mix of these characters.

## Quantifiers
Quantifiers are meta-characters in regex that adjust the preceding character or group, dictating how many of those instances to look for consecutively. They set clear guidelines on how many of a certain character or group of characters should be found. The `*` symbol matches the preceding character zero or more times, the `+` sign matches one or more of the preceding character, and the `?` indicates the preceding character might appear zero or once. Using `{n,x}`, you can define a specific range for matches, as seen in the "Matching an Email" regex where `{2,6}` checks for a domain extension like ".com" or ".org" that is between 2 to 6 characters long.

## Quantifiers
Quantifiers in regex, such as *, +, and ?, dictate the frequency of a character or group's occurrence. In the context of the regex pattern we're discussing, these quantifiers help specify the number of desired matches. Their function varies: * captures zero or more times, + captures at least once, and ? captures zero or once.

## Grouping Constructs
Regex uses `()` (grouping constructs) to break up complex patterns into subexpressions. These subexpressions allow checking different parts of a string for specific requirements. Two types of grouping constructs exist: capturing and non-capturing. Capturing groups capture matched characters for potential reuse (with numbered backreferences), while non-capturing groups do not. These `()` define distinct groups in a regex expression, such as capturing characters before `@`, before `.`, and from `.` to the end.

## OR Operator
In regular expressions, the OR operator (`|`) allows you to search for multiple options, and you can use it within bracket expressions or grouping constructs to match different patterns.

## Character Escapes
Regex uses backslash (`\`) which serves to escape special characters, ensuring they are treated as literal characters rather than having their usual special meaning. However, inside bracket expressions, including the backslash, all special characters lose their special significance.

## Character Classes
Character classes are elements in a regex expression that define specific sets of characters for pattern matching. In the provided regex, three character classes are used: `[a-z0-9_.-]`, `[\da-z.-]`, and `[a-z.]`. The first class matches lowercase letters, digits, underscore, period, and hyphen. The second class matches digits, lowercase letters, period, and hyphen. The third class matches lowercase letters and period. For example, `[a-z0-9_.-]` matches characters from 'a-z', '0-9', underscore, period, and hyphen. Similarly, `[\da-z.-]` matches digits, lowercase letters, period, and hyphen. Additionally, `[a-z.]` matches lowercase letters and period. Other examples of single characters in regex include `\d` for any digit, `\w` for any alphanumeric character, and `\s` for any whitespace character like space or tab.

## Flags
Regex flags are used to alter the behavior of expressions, such as enabling case insensitivity, finding all matches, enabling multiline mode, allowing a dot to match newline characters, enabling full Unicode support, and activating "sticky" mode. JavaScript offers six flags: i, g, m, s, u, and y.

## Author
[Juan Piedra](https://github.com/juan-piedra), a bootcamp student with the ambition to become a great Software Engineer.