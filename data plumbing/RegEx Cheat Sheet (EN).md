# Reference Sheet for Regular Expressions




# Regular Expressions Reference Sheet

## Practice Text

_"Giovanni Bianchi, born on 12/11/1990, purchased the train ticket IT456 to Milan on 01/06/2025 at 08:45.  
He used the credit card with the number 4111-1111-1111-1111 for a total of €120.  
Please note the “rentrée” fee is €250.  
For assistance, please contact us at: giovanni.bianchi@example.com (ascii characters), 予約@example.com (Japanese, unicode characters) or 订单号码 (Chinese, unicode characters).  
The transaction code is TXN987654321. The booking was made at 16:20 on 15/03/2025."_

---

## 1. Basic Character Matching

- Basic regular expressions match exact characters or sequences of characters in text. You can use individual characters, alternation (`|`), or the dot (`.`) to represent any character. Using these commands allows you to search for specific sequences of letters or numbers in the text.

|Regex Command|Explanation|Regex Result|
|---|---|---|
|`abc`|Matches exactly the string "abc".|Nessuna corrispondenza|
|`a\|b`|Matches "a" or "b".|`a`, `b`, `b`, `a`, `b`...|
|`.`|Matches any single character except a newline.|**All characters in the text** (excluding spaces)|
|`\d`|Matches any digit (0-9).|`1`, `2`, `1`, `1`, `1`, `9`, `9`, `0`, `4`, `5`, `6`, `0`, `1`, `0`, `6`, `2`, `0`, `2`, `5`, `0`, `8`, `4`, `5`, `4`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `2`, `0`, `2`, `5`, `0`, `2`, `5`, `0`, `9`, `8`, `7`, `6`, `5`, `4`, `3`, `2`, `1`, `1`, `6`, `2`, `0`, `1`, `5`, `0`, `3`, `2`, `0`, `2`, `5`|
|`\w`|Matches any word character (letter, digit, underscore).|`Giovanni`, `Bianchi`, `born`, `on`, `12`, `11`, `1990`, `purchased`, `the`, `train`, `ticket`, `IT456`, `to`, `Milan`, `on`, `01`, `06`, `2025`, `at`, `08`, `45`, `He`, `used`, `the`, `credit`, `card`, `with`, `the`, `number`, `4111`, `1111`, `1111`, `1111`, `for`, `a`, `total`, `of`, `120`, `Please`, `note`, `the`, `rentrée`, `fee`, `is`, `250`, `For`, `assistance`, `please`, `contact`, `us`, `at`, `giovanni`, `bianchi`, `example`, `com`, `ascii`, `characters`, `Japanese`, `unicode`, `characters`, `Chinese`, `unicode`, `characters`, `The`, `transaction`, `code`, `is`, `TXN987654321`, `The`, `booking`, `was`, `made`, `at`, `16`, `20`, `on`, `15`, `03`, `2025`|
|`\s`|Matches any whitespace character.|**All spaces and line breaks**|
|`\D`|Matches any non-digit character.|**All non-numeric characters**|
|`\W`|Matches any non-word character.|`,`, , `,`, , , , `-`, `-`, `-`, `-`, , `€`, `.`, , `“`, `”`, `€`, `.`, `@`, `@`, `(`, `)`, `(`, `)`, `(`, `)`, `.`|

---

## 2. Character Sets and Ranges

- Character sets are useful when you want to match a specific group of characters. You can also define ranges, such as `a-z` for all lowercase letters. Using `[^ ]` allows you to exclude certain characters.

|Regex Command|Explanation|Regex Result|
|---|---|---|
|`[aeiou]`|Matches any vowel.|`o`, `i`, `a`, `o`, `i`, `a`, `o`, `i`, `o`, ...|
|`[^aeiou]`|Matches any character that is NOT a vowel.|`G`, `v`, `n`, `n`, `B`, `n`, `c`, `h`, ...|
|`[a-z]`|Matches any lowercase letter from "a" to "z".|`i`, `o`, `v`, `a`, `n`, `n`, `i`, ...|
|`[A-Z]`|Matches any uppercase letter from "A" to "Z".|`G`, `B`, `I`, `T`, `M`, `T`, `X`, `N`|
|`[0-9]`|Matches any digit from "0" to "9".|`1`, `2`, `1`, `1`, `1`, `9`, `9`, `0`, ...|
|`[a-zA-Z0-9]`|Matches any letter or digit.|`G`, `i`, `o`, `v`, `a`, `n`, `n`, `i`, ...|
|`[13579]`|Matches any odd digit.|`1`, `1`, `1`, `9`, `9`, `5`, `1`, `5`, `3`, `1`|
|`[a-dm-q]`|Matches any letter between "a" and "d" OR between "m" and "q".|`b`, `n`, `d`, `m`, `m`, `m`, `m`, `p`, ...|

---

## 3. Anchors (Position-Based Matching)

- Anchors are used to specify where a match should occur, such as the start or end of a string. Using anchors helps limit searches to specific points in the text.

|Regex Command|Explanation|Regex Result|
|---|---|---|
|`^Hello`|Matches "Hello" only if it is at the beginning of the string.|Nessuna corrispondenza|
|`world$`|Matches "world" only if it is at the end of the string.|Nessuna corrispondenza|
|`\bword\b`|Matches the exact word "word" with word boundaries.|Nessuna corrispondenza|
|`\Bword\B`|Matches "word" only if **not** at word boundaries.|Nessuna corrispondenza|

---

## 4. Quantifiers (Repetition Operators)

- Quantifiers define how many times a character, group, or pattern should appear. They help match repeated sequences efficiently.

|Regex Command|Explanation|Regex Result|
|---|---|---|
|`a*`|Matches "a" repeated zero or more times.|``, `a`,`` , `a`, ``, `a`, `a`,`` , ...|
|`a+`|Matches "a" repeated one or more times.|`a`, `a`, `a`, `a`, `a`, `a`, `a`|
|`a?`|Matches "a" zero or one time.|``, `a`,`` , `a`, ``, `a`,`` , `a`, ...|
|`a{3}`|Matches exactly three occurrences of "a".|Nessuna corrispondenza|
|`a{2,4}`|Matches between 2 and 4 occurrences of "a".|`aa`, `aa`|
|`a{2,}`|Matches at least 2 occurrences of "a".|`aa`, `aaa`, `aaa`|

---

## 5. Grouping and Capturing

- Parentheses `()` are used to group expressions. This allows you to apply quantifiers to entire groups and capture specific parts of a match.

|Regex Command|Explanation|Regex Result|
|---|---|---|
|`(abc)`|Captures "abc" as a group.|Nessuna corrispondenza|
|`(abc)+`|Matches one or more occurrences of "abc".|Nessuna corrispondenza|
|`(a|b)c`|Matches "ac" or "bc".|
|`(?:abc)`|Non-capturing group (matches "abc" but doesn't save it).|Nessuna corrispondenza|

---

## 6. Lookahead and Lookbehind

- Lookarounds allow you to match patterns **before** or **after** another pattern, without including them in the final match.

| Regex Command | Explanation                                                          | Regex Result                                         |
| ------------- | -------------------------------------------------------------------- | ---------------------------------------------------- |
| `(?=abc)`     | Positive lookahead: ensures "abc" follows but does not capture it.   | Nessuna corrispondenza                               |
| `(?!abc)`     | Negative lookahead: ensures "abc" does **not** follow.               | Matches before every character not followed by "abc" |
| `(?<=abc)`    | Positive lookbehind: ensures "abc" precedes but does not capture it. | Nessuna corrispondenza                               |
| `(?<!abc)`    | Negative lookbehind: ensures "abc" does **not** precede.             | Matches after every character not preceded by "abc"  |

---
## 7. Escaping Special Characters

- Some characters (`.`, `*`, `+`, `?`, `|`, `^`, `$`, `()`, `[]`, `{}`) have special meanings. Use `\` before them to match them literally.

| Regex Command | Explanation                            | Regex Result           |
| ------------- | -------------------------------------- | ---------------------- |
| `\.`          | Matches a literal dot `.`              | `.`, `.`, `.`          |
| `\*`          | Matches a literal asterisk `*`.        | Nessuna corrispondenza |
| `\?`          | Matches a literal question mark `?`.   | Nessuna corrispondenza |
| `\|`          | Matches a literal pipe `               | `.                     |
| `\(`          | Matches an opening parenthesis `(`.    | `(`, `(`, `(`          |
| `\[`          | Matches an opening square bracket `[`. | Nessuna corrispondenza |

---

## 8. Logical Operators

- Logical operators are used in regular expressions to combine multiple search conditions. The main logical operators are **OR** (alternation) and **AND** (implicit overlap). These operators allow you to create more complex expressions that can match multiple patterns simultaneously.

|Regex Command|Explanation|Regex Result|
|---|---|---|
|`a\|b`|Matches "a" or "b".|`a`, `b`, `b`, `a`, `b`, `b`, `b`, `a`, `a`, `b`...|
|`abc\|def`|Matches "abc" or "def".|Nessuna corrispondenza|
|`\d{3}-\d{2}-\d{4}\|[A-Za-z]+`|Matches a number in the format `000-00-0000` or a word with letters.|`Giovanni`, `Bianchi`, `born`, `on`, `purchased`, `the`, `train`, `ticket`, `to`, `Milan`, `on`, `at`, `He`, `used`, `the`, `credit`, `card`, `with`, `the`, `number`, `for`, `a`, `total`, `of`, `Please`, `note`, `the`, `rentrée`, `fee`, `is`, `For`, `assistance`, `please`, `contact`, `us`, `at`, `ascii`, `characters`, `Japanese`, `unicode`, `characters`, `Chinese`, `unicode`, `characters`, `The`, `transaction`, `code`, `is`, `The`, `booking`, `was`, `made`, `at`, `on`|
|`cat.*dog`|Matches "cat" followed by anything and then "dog".|Nessuna corrispondenza|
|`abc123`|Matches exactly the string "abc123".|Nessuna corrispondenza|
|`\d{2,4}\|[A-Za-z]{3,5}`|Matches numbers between 2 and 4 digits or words of 3-5 letters.|`born`, `on`, `the`, `train`, `IT456`, `to`, `Milan`, `on`, `at`, `used`, `the`, `with`, `the`, `for`, `note`, `the`, `is`, `For`, `us`, `at`, `code`, `The`, `was`, `made`, `at`, `on`|

---

## 9. Accented Words and Non-ASCII Characters and a few more examples

- These regex patterns allow you to detect words with accented letters or special non-ASCII characters.

|Regex Command|Explanation|Regex Result|
|---|---|---|
|`\w+`|Matches a word composed of ASCII alphanumeric characters. **Does not capture accented or non-ASCII characters.**|`Giovanni`, `Bianchi`, `born`, `on`, `purchased`, `the`, `train`, `ticket`, `IT456`, `to`, `Milan`, `on`, `at`, `He`, `used`, `the`, `credit`, `card`, `with`, `the`, `number`, `for`, `a`, `total`, `of`, `Please`, `note`, `the`, `is`, `For`, `assistance`, `please`, `contact`, `us`, `at`, `ascii`, `characters`, `Japanese`, `unicode`, `characters`, `Chinese`, `unicode`, `characters`, `The`, `transaction`, `code`, `is`, `The`, `booking`, `was`, `made`, `at`, `on`|
|`\b\w*[éèêëàáâäôöòóùúûüçñ]\w*\b`|Matches words that contain at least one accented letter.|`rentrée`|
|`[^\x00-\x7F]+`|Matches any non-ASCII character.|`rentrée`, `予約`, `订单号码`|
|`\p{L}+`|Matches words that contain letters, including accented ones (Unicode support).|`Giovanni`, `Bianchi`, `born`, `on`, `purchased`, `the`, `train`, `ticket`, `IT456`, `to`, `Milan`, `on`, `at`, `He`, `used`, `the`, `credit`, `card`, `with`, `the`, `number`, `for`, `a`, `total`, `of`, `Please`, `note`, `the`, `rentrée`, `fee`, `is`, `For`, `assistance`, `please`, `contact`, `us`, `at`, `ascii`, `characters`, `Japanese`, `unicode`, `characters`, `Chinese`, `unicode`, `characters`, `The`, `transaction`, `code`, `is`, `The`, `booking`, `was`, `made`, `at`, `on`, `予約`, `订单号码`|
|`\p{Latin}+`|Matches only Latin words (excludes Asian characters).|`Giovanni`, `Bianchi`, `born`, `on`, `purchased`, `the`, `train`, `ticket`, `IT456`, `to`, `Milan`, `on`, `at`, `He`, `used`, `the`, `credit`, `card`, `with`, `the`, `number`, `for`, `a`, `total`, `of`, `Please`, `note`, `the`, `rentrée`, `fee`, `is`, `For`, `assistance`, `please`, `contact`, `us`, `at`, `ascii`, `characters`, `Japanese`, `unicode`, `characters`, `Chinese`, `unicode`, `characters`, `The`, `transaction`, `code`, `is`, `The`, `booking`, `was`, `made`, `at`, `on`|
|`\p{Han}+`|Matches Chinese characters.|`订单号码`|
|`\p{Hiragana}+\|\p{Katakana}+`|Matches Japanese characters in Hiragana or Katakana.|Nessuna corrispondenza|
|`\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}\b`|Matches an email address.|`giovanni.bianchi@example.com`, `予約@example.com`|
|`\b\d{2}/\d{2}/\d{4}\b`|Matches a date in the format DD/MM/YYYY.|`12/11/1990`, `01/06/2025`, `15/03/2025`|
|`\b\d{4}-\d{4}-\d{4}-\d{4}\b`|Matches a credit card number format.|`4111-1111-1111-1111`|
|`\b[A-Z]{2}\d+\b`|Matches a code with two uppercase letters followed by digits.|`IT456`, `TXN987654321`|
|`\b\d{2}:\d{2}\b`|Matches a time in HH:MM format.|`08:45`, `16:20`|

---
