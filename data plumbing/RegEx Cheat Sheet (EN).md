# Regular Expressions Cheat Sheet 



## 1. Basic Character Matching
Regular expressions primarily work by matching characters in a string. This section covers the most fundamental patterns used to find exact sequences, alternative characters, or any character.

| Regex Command | Explanation |
|--------------|-------------|
| `abc`        | Matches the exact string "abc". |
| `a|b`        | Matches either "a" or "b". |
| `.`          | Matches any single character except a newline. |
| `\d`         | Matches any digit (0-9). |
| `\w`         | Matches any word character (letter, digit, underscore). |
| `\s`         | Matches any whitespace character (space, tab, newline). |
| `\D`         | Matches any non-digit character. |
| `\W`         | Matches any non-word character. |
| `\S`         | Matches any non-whitespace character. |

---

## 2. Character Sets and Ranges
Character sets and ranges allow you to specify multiple possible characters at a certain position in a string. Use brackets `[ ]` to define a set of characters to match.

| Regex Command | Explanation |
|--------------|-------------|
| `[aeiou]`    | Matches any single vowel. |
| `[^aeiou]`   | Matches any single character that is NOT a vowel. |
| `[a-z]`      | Matches any lowercase letter from "a" to "z". |
| `[A-Z]`      | Matches any uppercase letter from "A" to "Z". |
| `[0-9]`      | Matches any digit from "0" to "9". |
| `[a-zA-Z0-9]`| Matches any letter or digit. |
| `[13579]`    | Matches any odd digit. |
| `[a-dm-q]`   | Matches any letter from "a" to "d" OR "m" to "q". |

---

## 3. Anchors (Position-Based Matching)
**Grammar Explanation:**
- Anchors do not match characters but rather positions in the text.
- The `^` symbol ensures that the match occurs **at the start of a string**.
- The `$` symbol ensures that the match occurs **at the end of a string**.
- The `\b` and `\B` symbols define **word boundaries**, allowing you to match full words.

| Regex Command  | Explanation |
|---------------|-------------|
| `^Hello`      | Matches "Hello" at the start of a string. |
| `world$`      | Matches "world" at the end of a string. |
| `\bword\b`    | Matches the exact word "word" with word boundaries. |
| `\Bword\B`    | Matches "word" only if it is NOT at a word boundary. |

---

## 4. Repetitions and Quantifiers
**Grammar Explanation:**
- **Quantifiers** determine **how many times** a character or group should appear in a match.
- `*` means **zero or more** repetitions (e.g., `ba*` matches `b`, `ba`, `baa`, `baaa`...).
- `+` means **one or more** repetitions (e.g., `ba+` matches `ba`, `baa`, but not `b`).
- `?` means **zero or one** occurrence (e.g., `colou?r` matches both `color` and `colour`).
- `{n}` specifies an **exact number** of occurrences.
- `{n,}` means **at least** `n` occurrences.
- `{n,m}` means **between** `n` and `m` occurrences.

| Regex Command | Explanation |
|--------------|-------------|
| `a*`         | Matches "a" repeated zero or more times. |
| `a+`         | Matches "a" repeated one or more times. |
| `a?`         | Matches "a" zero or one time. |
| `a{3}`       | Matches exactly three "a"s (e.g., "aaa"). |
| `a{2,4}`     | Matches between 2 and 4 "a"s (e.g., "aa", "aaa", "aaaa"). |
| `a{2,}`      | Matches at least 2 "a"s. |
| `a*?`        | Lazy version: matches as few "a"s as possible. |
| `a+?`        | Lazy version: matches at least one "a", but as few as possible. |

---

## 5. Grouping and Capturing
**Grammar Explanation:**
- Parentheses `( )` **group characters together** to apply quantifiers or capture matched text.
- `(abc)` captures "abc" as a **group** for later use.
- `(?:abc)` is a **non-capturing group**, meaning it groups text but does not store it.
- `\1`, `\2`, etc., refer to **previously captured groups**.
- Useful for **extracting** data from text, such as dates, phone numbers, and names.

| Regex Command  | Explanation |
|---------------|-------------|
| `(abc)`       | Captures "abc" as a group. |
| `(abc|def)`   | Matches either "abc" or "def". |
| `(\d{3})-(\d{2})-(\d{4})` | Captures parts of a phone number (e.g., "123-45-6789"). |
| `(?:abc)`     | Matches "abc" but does NOT capture it. |
| `\b(\w+)\s+\1\b` | Matches repeated words (e.g., "hello hello"). |

---

## 6. Lookaheads and Lookbehinds
**Grammar Explanation:**
- Lookaheads and lookbehinds **assert** that a pattern exists before or after a match **without including it in the match**.
- `(?=...)` (positive lookahead) ensures that something **is present** after a match.
- `(?!...)` (negative lookahead) ensures that something **is NOT present** after a match.
- `(?<=...)` (positive lookbehind) ensures that something **is present** before a match.
- `(?<!...)` (negative lookbehind) ensures that something **is NOT present** before a match.

| Regex Command       | Explanation |
|--------------------|-------------|
| `\d+(?= euros)`   | Matches digits followed by "euros" (e.g., "100 euros"). |
| `\d+(?! euros)`   | Matches digits NOT followed by "euros". |
| `(?<=\$)\d+`      | Matches digits preceded by a dollar sign (e.g., "$100"). |
| `(?<!\$)\d+`      | Matches digits NOT preceded by a dollar sign. |

---

## 7. Escaping Special Characters
**Grammar Explanation:**
- Some characters (`.`, `*`, `+`, `?`, `|`, `()`, `{}`, `[]`) have **special meanings** in regex.
- To match them **literally**, you must use a **backslash (`\`)** before them.
- This is necessary when searching for punctuation marks, special symbols, or mathematical operators.

| Regex Command   | Explanation |
|---------------|-------------|
| `\.`         | Matches a literal period "." |
| `\*`         | Matches a literal asterisk "*" |
| `\?`         | Matches a literal question mark "?" |
| `\+`         | Matches a literal plus sign "+" |
| `\|`         | Matches a literal pipe "|" |
| `\(`, `\)`   | Matches literal parentheses "(" and ")" |
