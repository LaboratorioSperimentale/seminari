# Reference Sheet for Regular Expressions

## Text for Exercise:
"Giovanni Bianchi, born on 12/11/1990, purchased the train ticket IT456 to Milan on 01/06/2025 at 08:45. He used the credit card with the number 4111-1111-1111-1111 for a total of €120. The provided email address is giovanni.bianchi@example.com. The transaction code is TXN987654321. The booking was made at 16:20 on 15/03/2025."

Use the service [https://regex101.com/](https://regex101.com/) to test your regular expressions.

---

## 1. Basic Character Matching
Basic regular expressions match exact characters or sequences of characters in the text. You can use single characters, alternations (using `|`), or the dot `.` to represent any character. Using these commands allows you to search for specific sequences of letters or numbers in the text.

| Regex Command | Explanation | Regex Result |
|---------------|-------------|--------------|
| `abc`         | Matches exactly the string "abc". | No result (no "abc") |
| `a\|b`         | Matches either "a" or "b". | Matches all occurrences of the letter "a" and "b" in the text |
| `.`           | Matches any single character except a newline. | "G", "i", "o", "v", "a", "n", "n", "i", " ", "B", "i", "a", "n", "c", "h", "i", ",", " ", "n", "a", "t", "o", " ", "i", "l", " ", "1", "2", "/", "1", "1", "/", "1", "9", "9", "0", ","... |
| `\d`          | Matches any digit (0-9). | "1", "2", "1", "1", "1", "9", "9", "0", "0", "1", "0", "6", "2", "0", "2", "5", "0", "8", "4", "5", "4", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "2", "0", "9", "8", "7", "6", "5", "4", "3", "2", "1", "6", "2", "0", "1", "5", "0", "3", "2", "0", "2", "5" |
| `\w`          | Matches any word character (letter, digit, underscore). | "G", "i", "o", "v", "a", "n", "n", "i", "B", "i", "a", "n", "c", "h", "i", "1", "2", "1", "1", "1", "9", "9", "0", "1", "1", "0", "6", "2", "0", "2", "5", "0", "8", "4", "5", "4", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "2", "0", "9", "8", "7", "6", "5", "4", "3", "2", "1", "6", "2", "0", "1", "5", "0", "3", "2", "0", "2", "5" |
| `\s`          | Matches any space character (space, tab, newline). | " ", " ", " ", " ", " ", " ", " " |
| `\D`          | Matches any character that is not a digit. | "G", "i", "o", "v", "a", "n", "n", "i", " ", "B", "i", "a", "n", "c", "h", "i", ",", " ", "n", "a", "t", "o", " ", "i", "l", " ", "/", "/", "/", "/", ",", " ", "H", "a", " ", "a", "c", "q", "u", "i", "s", "t", "a", "t", "o", " ", "i", "l", " ", "b", "i", "g", "l", "i", "e", "t", "t", "o", " ", "d", "e", "l", " ", "t", "r", "e", "n", "o", " ", "I", "T", "f", "o", "r", " " |
| `\W`          | Matches any non-word character. | " ", ",", ".", "@", "-", "_", "$", "€", ":" |
| `\S`          | Matches any non-space character. | "G", "i", "o", "v", "a", "n", "n", "i", "B", "i", "a", "n", "c", "h", "i", "1", "2", "1", "1", "1", "9", "9", "0", "1", "1", "0", "6", "2", "0", "2", "5", "0", "8", "4", "5", "4", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "2", "0", "9", "8", "7", "6", "5", "4", "3", "2", "1", "6", "2", "0", "1", "5", "0", "3", "2", "0", "2", "5" |

---

## 2. Character Sets and Ranges
Character sets are very useful when you want to match a specific set of characters. They can also be used to define ranges, such as `a-z` for all lowercase letters. Using `[^ ]` allows you to exclude certain characters.

| Regex Command | Explanation | Regex Result |
|---------------|-------------|--------------|
| `[aeiou]`     | Matches any vowel. | "o", "a", "i", "a", "i", "o", "e", "i", "a", "o", "e", "o" |
| `[^aeiou]`    | Matches any character that is **NOT** a vowel. | "G", "v", "n", "n", "B", "n", "c", "h", "n", "t", "l", "1", "2", "1", "1", "1", "9", "9", "0", "/", "/", "/", ".", ",", " ", " ", " ", "n", "t", "l", "b", "g", "l", "t", "t", "s" |
| `[a-z]`       | Matches any lowercase letter from "a" to "z". | "i", "o", "v", "a", "n", "n", "i", "a", "i", "a", "i", "a", "t", "o", "i", "e", "s", "m", "a", "o", "t", "l", "i", "n", "i", "l", "i", "a", "o", "e", "o" |
| `[A-Z]`       | Matches any uppercase letter from "A" to "Z". | "G", "B", "I", "T" |
| `[0-9]`       | Matches any digit from "0" to "9". | "1", "2", "1", "1", "1", "9", "9", "0", "0", "1", "0", "6", "2", "0", "2", "5", "0", "8", "4", "5", "4", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "2", "0", "9", "8", "7", "6", "5", "4", "3", "2", "1", "6", "2", "0", "1", "5", "0", "3", "2", "0", "2", "5" |
| `[a-zA-Z0-9]` | Matches any letter or digit. | "G", "i", "o", "v", "a", "n", "n", "i", "B", "i", "a", "n", "c", "h", "i", "1", "2", "1", "1", "1", "9", "9", "0", "1", "1", "0", "6", "2", "0", "2", "5", "0", "8", "4", "5", "4", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "2", "0", "9", "8", "7", "6", "5", "4", "3", "2", "1", "6", "2", "0", "1", "5", "0", "3", "2", "0", "2", "5" |
| `[13579]`     | Matches any odd digit. | "1", "1", "1", "1", "1", "9", "9", "1", "5", "1", "3", "9", "7" |
| `[a-dm-q]`    | Matches any character between "a" and "d" or between "m" and "q". | "a", "b", "c", "d", "m", "n", "p" |

---

## 3. Special Characters
Special characters are used to match patterns based on specific rules. These can include matching any single character, matching the beginning or end of a string, or grouping patterns.

| Regex Command | Explanation | Regex Result |
|---------------|-------------|--------------|
| `^`           | Matches the beginning of the string. | "G" |
| `$`           | Matches the end of the string. | "e" |
| `*`           | Matches 0 or more occurrences of the preceding character. | "Giovanni" |
| `+`           | Matches 1 or more occurrences of the preceding character. | "i" |
| `?`           | Matches 0 or 1 occurrence of the preceding character. | "G" |
| `{n}`         | Matches exactly n occurrences of the preceding character. | "12" (matches "1" |
| `()`          | Groups expressions for applying quantifiers. | "Giovanni" (entire group matched) |
| `|`           | Acts as an OR operator to match either expression. | "Bianchi" or "Giovanni" |

---

---

## 4. Repetitions and Quantifiers
Quantifiers are used to specify how many times a character or a group of characters should be repeated. This allows you to match sequences of characters with varying lengths.

| Regex Command | Explanation | Regex Result |
|---------------|-------------|--------------|
| `a*`          | Matches zero or more occurrences of "a". | "a", "a", "a", "a", "a" |
| `a+`          | Matches one or more occurrences of "a". | "a", "a", "a", "a" |
| `a?`          | Matches zero or one occurrence of "a". | "a", "a", "a", "a", " " |
| `a{3}`        | Matches exactly three occurrences of "a". | No result (no group with three consecutive "a"s) |
| `a{2,4}`      | Matches between 2 and 4 occurrences of "a". | No result (no group with 2-4 consecutive "a"s) |
| `a{2,}`       | Matches at least 2 occurrences of "a". | No result (no group with at least 2 consecutive "a"s) |

---

## 5. Grouping and Capturing
Capture groups allow you to group parts of a regular expression and extract them separately. Groups are useful for applying quantifiers to multiple characters at once.

| Regex Command | Explanation | Regex Result |
|---------------|-------------|--------------|
| `(abc)`       | Captures "abc" as a group. | No result (no "abc" string) |
| `(abc|def)`   | Matches "abc" or "def". | No result (no "abc" or "def" present) |
| `(?:abc)`     | Matches "abc" but does **not capture** it. | No result (no "abc" string) |

---

## 6. Lookahead and Lookbehind
Lookahead and lookbehind allow matches based on a condition that occurs before or after a specific position in the text.

| Regex Command    | Explanation | Regex Result |
|------------------|-------------|--------------|
| `\d+(?= euros)`  | Matches digits followed by "euros". | No result (no "euros" string) |
| `(?<=@)\w+`      | Matches a sequence of letters preceded by "@" (e.g., an email domain). | "example" |
| `(?<!\$)\d+`     | Matches digits **not preceded** by the dollar sign. | "12", "11", "1990", "01", "06", "2025", "08", "45", "4111", "1111", "1111", "1111", "120", "987654321", "16", "20", "15", "03", "2025" |

---

## 7. Escaping Special Characters
Sometimes, you need to search for special symbols like the dot, asterisk, or dollar sign. In these cases, you must "escape" these characters using the backslash (`\`).

| Regex Command | Explanation | Regex Result |
|---------------|-------------|--------------|
| `\.`          | Matches a literal dot ".". | "." |
| `\*`          | Matches a literal asterisk "*". | "*" |
| `\?`          | Matches a literal question mark "?". | "?" |
| `\+`          | Matches a literal plus sign "+". | "+" |
| `\|`          | Matches a literal pipe "|" symbol. | "|" |
| `\(`, `\)`    | Matches literal parentheses "(" and ")". | "(", ")" |

---

## 8. Logical Operators
Logical operators are used in regular expressions to combine multiple search conditions. The main logical operators are **OR** (alternation) and **AND** (implicit overlap). These operators allow you to create more complex expressions that can match multiple patterns simultaneously.

- **OR (`|`)**: The `|` operator is used to match one of two (or more) conditions. For example, `a|b` matches "a" **or** "b".
- **AND (implicit)**: The AND operator is not explicitly written in regular expressions. Expressions combine multiple patterns simultaneously, so a match will occur only when both patterns are present in the string. For example, `abc123` will search for both "abc" and "123" consecutively.

| Regex Command | Explanation | Regex Result |
|---------------|-------------|--------------|
| `a|b`         | Matches "a" **or** "b". | "a", "b" |
| `abc|def`     | Matches "abc" **or** "def". | No result (no "abc" or "def" present) |
| `\d{3}-\d{2}-\d{4}|[A-Za-z]+` | Matches a sequence of digits in the format "xxx-xx-xxxx" **or** a sequence of letters. | "12-34-5678", "Giovanni", "Bianchi" |
| `cat.*dog`    | Matches "cat" followed by anything and then "dog". | No result (no "cat" and "dog" together) |
| `abc123`      | Matches exactly the string "abc123". | "abc123" |
| `\d{2,4}|[A-Za-z]{3,5}` | Matches a number of 2-4 digits **or** a word of 3-5 letters. | "12", "1990", "abc", "john", "apple" |

