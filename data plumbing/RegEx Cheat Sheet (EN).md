
# Reference Sheet for Regular Expressions (Bash-Compatible)

## Practice Text

_"Giovanni Bianchi, born on 12/11/1990, purchased the train ticket IT456 to Milan on 01/06/2025 at 08:45.  
He used the credit card with the number 4111-1111-1111-1111 for a total of €120.  
Please note the “rentrée” fee is €250.  
For assistance, please contact us at: giovanni.bianchi@example.com (ascii characters), 予約@example.com (Japanese, unicode characters) or 订单号码 (Chinese, unicode characters).  
The transaction code is TXN987654321. The booking was made at 16:20 on 15/03/2025."_

---

## 1. Basic Character Matching

| Regex Command | Explanation | Example Match (Es: "Giovanni Bianchi, born on 12/11/1990, left at 08:45.")|
|--------------|-------------|--------------|
| `abc` | Matches exactly "abc". | No match |
| `a\|b` | Matches "a" or "b". | `a`, `b` |
| `.` | Matches any single character. | Matches all characters except newlines |
| `[0-9]` | Matches any digit (0-9). | `1`, `2`, `5` |
| `[a-zA-Z0-9_]` | Matches any alphanumeric character. | `G`, `B`, `i`, `a` |
| `[[:space:]]` | Matches any whitespace character. | Spaces, tabs, newlines |
| `[^0-9]` | Matches any non-digit. | Letters, punctuation |

---

## 2. Character Sets and Ranges

| Regex Command | Explanation | Example Match |
|--------------|-------------|--------------|
| `[aeiou]` | Matches any vowel. | `o`, `i`, `a` |
| `[^aeiou]` | Matches any character that is NOT a vowel. | `G`, `B`, `n`, `c` |
| `[a-z]` | Matches any lowercase letter. | `a`, `b`, `c` |
| `[A-Z]` | Matches any uppercase letter. | `G`, `B`, `I`, `T` |
| `[0-9]` | Matches any digit. | `1`, `2`, `3` |
| `[a-zA-Z0-9]` | Matches any letter or digit. | `G`, `i`, `o` |
| `[13579]` | Matches any odd digit. | `1`, `3`, `5` |

---

## 3. Anchors (Position-Based Matching)

| Regex Command | Explanation | Example Match |
|--------------|-------------|--------------|
| `^Hello` | Matches "Hello" at the beginning of a line. | No match |
| `world$` | Matches "world" at the end of a line. | No match |
| `\<word\>` | Matches the word "word" with boundaries. | No match |
| `\Bword\B` | Matches "word" NOT at word boundaries. | No match |

---

## 4. Quantifiers (Repetition Operators)

| Regex Command | Explanation | Example Match |
|--------------|-------------|--------------|
| `a*` | Matches "a" zero or more times. | ``, `a`, `aa` |
| `a+` | Matches "a" one or more times. | `a`, `aa` |
| `a?` | Matches "a" zero or one time. | ``, `a` |
| `a\{3\}` | Matches exactly three "a"s. | No match |
| `a\{2,4\}` | Matches between 2 and 4 "a"s. | `aa`, `aaa` |
| `a\{2,\}` | Matches at least 2 "a"s. | `aa`, `aaa` |

---

## 5. Grouping and Capturing

| Regex Command | Explanation | Example Match |
|--------------|-------------|--------------|
| `\(abc\)` | Captures "abc" as a group. | No match |
| `\(abc\)+` | Matches one or more occurrences of "abc". | No match |
| `\(a\|b\)c` | Matches "ac" or "bc". | No match |
| `\(?:abc\)` | Non-capturing group. | No match |

---

## 6. Lookahead and Lookbehind (Not supported in Bash)

Lookahead and Lookbehind are **not** natively supported in Bash regex.

---

## 7. Escaping Special Characters

| Regex Command | Explanation | Example Match |
|--------------|-------------|--------------|
| `\.` | Matches a literal dot `.` | `.` |
| `\*` | Matches a literal asterisk `*` | `*` |
| `\?` | Matches a literal question mark `?` | `?` |
| `\|` | Matches a literal pipe `|` | `|` |
| `\(` | Matches an opening parenthesis `(` | `(` |
| `\[ ]` | Matches square brackets | `[` `]` |

---

## 8. Logical Operators

| Regex Command | Explanation | Example Match |
|--------------|-------------|--------------|
| `a\|b` | Matches "a" or "b". | `a`, `b` |
| `abc\|def` | Matches "abc" or "def". | No match |
| `cat.*dog` | Matches "cat" followed by anything and then "dog". | No match |
| `abc123` | Matches exactly "abc123". | No match |

---

## 9. Accented Words and Non-ASCII Characters

Bash regex does not support Unicode character classes (`\p{L}`), but you can match specific characters.

| Regex Command | Explanation | Example Match |
|--------------|-------------|--------------|
| `[a-zA-Z0-9_]` | Matches a word composed of ASCII alphanumeric characters. | `Giovanni`, `Bianchi` |
| `[éèêëàáâäôöòóùúûüçñ]` | Matches any single accented letter. | `é` in `rentrée` |
| `[^[:ascii:]]` | Matches any non-ASCII character. | `rentrée`, `予約`, `订单号码` |
| `[A-Za-z0-9._%+-]\+@[A-Za-z0-9.-]\+\.[A-Za-z]\{2,\}` | Matches an email address. | `giovanni.bianchi@example.com` |
| `[0-9]\{2\}/[0-9]\{2\}/[0-9]\{4\}` | Matches a date in DD/MM/YYYY format. | `12/11/1990` |
| `[0-9]\{4\}-[0-9]\{4\}-[0-9]\{4\}-[0-9]\{4\}` | Matches a credit card number format. | `4111-1111-1111-1111` |
| `[A-Z]\{2\}[0-9]\+` | Matches a code with two uppercase letters followed by digits. | `IT456`, `TXN987654321` |
| `[0-9]\{2\}:[0-9]\{2\}` | Matches a time in HH:MM format. | `08:45`, `16:20` |

---

### Notes on Bash Regex Compatibility:

- Bash does **not** support `\d`, `\w`, or `\s`. Instead, use `[0-9]`, `[a-zA-Z0-9_]`, and `[[:space:]]`.
- `{}` quantifiers **must** be escaped (`\{ \}`).
- Lookaheads and lookbehinds **are not supported** in Bash.
- Unicode character classes (`\p{L}`) are **not supported**.
- Use `grep -E` or `awk` for extended regex support.

---

This reference provides **Bash-compatible** regular expressions while maintaining the original structure. Let me know if you need any refinements! 🚀
