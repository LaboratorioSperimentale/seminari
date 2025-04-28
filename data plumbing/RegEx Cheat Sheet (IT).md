# Foglio di Riferimento per le Espressioni Regolari

PHP < 7.3 + global + multiline

## Practice Text
- _"Giovanni Bianchi, born on 12/11/1990, purchased the train ticket IT456 to Milan on 01/06/2025 at 08:45.  
  He used the credit card with the number 4111-1111-1111-1111 for a total of €120.  
  Please note the “rentrée” fee is €250.  
  For assistance, please contact us at: giovanni.bianchi@example.com (ascii characters), 予約@example.com (Japanese, unicode characters) or 订单号码 (Chinese, unicode characters).  
  The transaction code is TXN987654321. The booking was made at 16:20 on 15/03/2025."_

---

## 1. Corrispondenza di Caratteri di Base
- Le espressioni regolari di base corrispondono esattamente ai caratteri o sequenze di caratteri nel testo. Puoi utilizzare caratteri singoli, alternanze (usando `|`), o il punto `.` per rappresentare qualsiasi carattere. L'uso di questi comandi permette di cercare specifiche sequenze di lettere o numeri nel testo.

|Comando Regex|Spiegazione|Risultato della Regex|
|---|---|---|
|`abc`|Corrisponde esattamente alla stringa "abc".|Nessuna corrispondenza|
|`a\|b`|Corrisponde a "a" oppure "b".|`a`, `b`, `b`, `a`, `b`...|
|`.`|Corrisponde a qualsiasi carattere singolo tranne un ritorno a capo.|**Tutti i caratteri del testo** (esclusi gli spazi)|
|`\d`|Corrisponde a qualsiasi cifra (0-9).|`1`, `2`, `1`, `1`, `1`, `9`, `9`, `0`, `4`, `5`, `6`, `0`, `1`, `0`, `6`, `2`, `0`, `2`, `5`, `0`, `8`, `4`, `5`, `4`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `1`, `2`, `0`, `2`, `5`, `0`, `2`, `5`, `0`, `9`, `8`, `7`, `6`, `5`, `4`, `3`, `2`, `1`, `1`, `6`, `2`, `0`, `1`, `5`, `0`, `3`, `2`, `0`, `2`, `5`|
|`\w`|Corrisponde a qualsiasi carattere di parola (lettera, cifra, trattino basso).|`Giovanni`, `Bianchi`, `born`, `on`, `12`, `11`, `1990`, `purchased`, `the`, `train`, `ticket`, `IT456`, `to`, `Milan`, `on`, `01`, `06`, `2025`, `at`, `08`, `45`, `He`, `used`, `the`, `credit`, `card`, `with`, `the`, `number`, `4111`, `1111`, `1111`, `1111`, `for`, `a`, `total`, `of`, `120`, `Please`, `note`, `the`, `rentrée`, `fee`, `is`, `250`, `For`, `assistance`, `please`, `contact`, `us`, `at`, `giovanni`, `bianchi`, `example`, `com`, `ascii`, `characters`, `Japanese`, `unicode`, `characters`, `Chinese`, `unicode`, `characters`, `The`, `transaction`, `code`, `is`, `TXN987654321`, `The`, `booking`, `was`, `made`, `at`, `16`, `20`, `on`, `15`, `03`, `2025`|
|`\s`|Corrisponde a qualsiasi carattere di spazio.|**Tutti gli spazi e i ritorni a capo**|
|`\D`|Corrisponde a qualsiasi carattere che non sia una cifra.|**Tutti i caratteri non numerici**|
|`\W`|Corrisponde a qualsiasi carattere non di parola.|`,`, , `,`, , , , `-`, `-`, `-`, `-`, , `€`, `.`, , `“`, `”`, `€`, `.`, `@`, `@`, `(`, `)`, `(`, `)`, `(`, `)`, `.`|

---

## 2. Set di Caratteri e Intervalli
- I set di caratteri sono molto utili quando si vuole fare una corrispondenza su un insieme di caratteri specifici. Possono essere usati anche per definire intervalli, come ad esempio `a-z` per tutte le lettere minuscole. L'uso di `[^ ]` permette di escludere determinati caratteri.

|Comando Regex|Spiegazione|Risultato della Regex|
|---|---|---|
|`[aeiou]`|Corrisponde a una qualsiasi vocale.|`o`, `i`, `a`, `o`, `i`, `a`, `o`, `i`, `o`, ...|
|`[^aeiou]`|Corrisponde a qualsiasi carattere che NON sia una vocale.|`G`, `v`, `n`, `n`, `B`, `n`, `c`, `h`, ...|
|`[a-z]`|Corrisponde a qualsiasi lettera minuscola da "a" a "z".|`i`, `o`, `v`, `a`, `n`, `n`, `i`, ...|
|`[A-Z]`|Corrisponde a qualsiasi lettera maiuscola da "A" a "Z".|`G`, `B`, `I`, `T`, `M`, `T`, `X`, `N`|
|`[0-9]`|Corrisponde a qualsiasi cifra da "0" a "9".|`1`, `2`, `1`, `1`, `1`, `9`, `9`, `0`, ...|
|`[a-zA-Z0-9]`|Corrisponde a qualsiasi lettera o cifra.|`G`, `i`, `o`, `v`, `a`, `n`, `n`, `i`, ...|
|`[13579]`|Corrisponde a qualsiasi cifra dispari.|`1`, `1`, `1`, `9`, `9`, `5`, `1`, `5`, `3`, `1`|
|`[a-dm-q]`|Corrisponde a qualsiasi lettera tra "a" e "d" OPPURE tra "m" e "q".|`b`, `n`, `d`, `m`, `m`, `m`, `m`, `p`, ...|

---

## 3. Ancore (Corrispondenza Basata sulla Posizione)
- Le ancore sono utilizzate per specificare la posizione in cui deve avvenire una corrispondenza, come l'inizio o la fine di una stringa. L'uso di ancore è utile per limitare la ricerca solo a determinati punti del testo.

|Comando Regex|Spiegazione|Risultato della Regex|
|---|---|---|
|`^Hello`|Corrisponde a "Hello" solo se si trova all'inizio della stringa.|Nessuna corrispondenza|
|`world$`|Corrisponde a "world" solo se si trova alla fine della stringa.|Nessuna corrispondenza|
|`\bword\b`|Corrisponde alla parola esatta "word" con confini di parola.|Nessuna corrispondenza|
|`\Bword\B`|Corrisponde a "word" solo se **non** è ai confini di parola.|Nessuna corrispondenza|

---

## 4. Ripetizioni e Quantificatori
- I quantificatori sono utilizzati per specificare quante volte un carattere o un gruppo di caratteri deve essere ripetuto. Questo ti permette di fare corrispondenze con sequenze di caratteri di lunghezza variabile.

|Comando Regex|Spiegazione|Risultato della Regex|
|---|---|---|
|`a*`|Corrisponde a "a" ripetuto zero o più volte.|`a`, `aa`, `a`, `a`, `a`, `a`, ...|
|`a+`|Corrisponde a "a" ripetuto una o più volte.|`a`, `aa`, `a`, `a`, `a`, `a`, ...|
|`a?`|Corrisponde a "a" zero o una volta.|**Molteplici corrispondenze singole**|
|`a{3}`|Corrisponde esattamente a tre "a".|Nessuna corrispondenza|
|`a{2,4}`|Corrisponde tra 2 e 4 "a".|`aa`|
|`a{2,}`|Corrisponde ad almeno 2 "a".|`aa`|

---

## 5. Raggruppamento e Cattura
- I gruppi di cattura ti permettono di raggruppare parti di un'espressione regolare e di estrarle separatamente. I gruppi vengono utilizzati per applicare quantificatori a più caratteri contemporaneamente.

|Comando Regex|Spiegazione|Risultato della Regex|
|---|---|---|
|`(abc)`|Cattura "abc" come un gruppo.|Nessuna corrispondenza|
|`(abc\|def)`|Corrisponde a "abc" o "def".|Nessuna corrispondenza|
|`(?:abc)`|Corrisponde a "abc" ma **non lo cattura**.|Nessuna corrispondenza|

---

## 6. Lookahead e Lookbehind
- Il lookahead e il lookbehind permettono di fare corrispondenze basate su una condizione che si trova prima o dopo una determinata posizione nel testo.

|Comando Regex|Spiegazione|Risultato della Regex|
|---|---|---|
|`\d+(?= euros)`|Corrisponde a cifre seguite da "euros".|Nessuna corrispondenza|
|`(?<=@)\w+`|Corrisponde a una sequenza di lettere precedute da "@" (ad esempio un dominio email).|`example`, `example`|
|`(?<!\$)\d+`|Corrisponde a cifre **non precedute** dal simbolo del dollaro.|`12`, `11`, `1990`, `456`, `01`, `06`, `2025`, `08`, `45`, `4111`, `1111`, `1111`, `1111`, `120`, `250`, `987654321`, `16`, `20`, `15`, `03`, `2025`|

---

## 7. Escape dei Caratteri Speciali
- A volte è necessario cercare simboli speciali come il punto, l'asterisco o il simbolo del dollaro. In questi casi, è necessario "escapare" questi caratteri utilizzando il backslash (`\`).

|Comando Regex|Spiegazione|Risultato della Regex|
|---|---|---|
|`\.`|Corrisponde a un punto "." letterale.|`.`, `.`, `.`, `.`, `.`, `.`, `.`|
|`\*`|Corrisponde a un asterisco "*" letterale.|Nessuna corrispondenza|
|`\?`|Corrisponde a un punto interrogativo "?" letterale.|Nessuna corrispondenza|
|`\+`|Corrisponde a un segno più "+" letterale.|Nessuna corrispondenza|
|`\|`|Corrisponde a un **pipe** "|"|
|`\(`, `\)`|Corrisponde a parentesi tonde "(" e ")" letterali.|`(`, `)`, `(`, `)`, `(`, `)`|

---

## 8. Operatori Logici
- Gli operatori logici vengono utilizzati nelle espressioni regolari per combinare più condizioni di ricerca. Gli operatori logici principali sono l'**OR** (alternanza) e l'**AND** (sovrapposizione implicita). Questi operatori ti permettono di creare espressioni più complesse che possono corrispondere a più pattern simultaneamente.

|Comando Regex|Spiegazione|Risultato della Regex|
|---|---|---|
|`a\|b`|Corrisponde a "a" oppure "b".|`a`, `b`, `b`, `a`, `b`, `b`, `b`, `a`, `a`, `b`...|
|`abc\|def`|Corrisponde a "abc" o "def".|Nessuna corrispondenza|
|`\d{3}-\d{2}-\d{4}\|[A-Za-z]+`|Corrisponde a un numero nel formato `000-00-0000` o a una parola con lettere.|`Giovanni`, `Bianchi`, `born`, `on`, `purchased`, `the`, `train`, `ticket`, `to`, `Milan`, `on`, `at`, `He`, `used`, `the`, `credit`, `card`, `with`, `the`, `number`, `for`, `a`, `total`, `of`, `Please`, `note`, `the`, `rentrée`, `fee`, `is`, `For`, `assistance`, `please`, `contact`, `us`, `at`, `ascii`, `characters`, `Japanese`, `unicode`, `characters`, `Chinese`, `unicode`, `characters`, `The`, `transaction`, `code`, `is`, `The`, `booking`, `was`, `made`, `at`, `on`|
|`cat.*dog`|Corrisponde a "cat" seguito da qualsiasi cosa e poi da "dog".|Nessuna corrispondenza|
|`abc123`|Corrisponde esattamente alla stringa "abc123".|Nessuna corrispondenza|
|`\d{2,4}\|[A-Za-z]{3,5}`|Corrisponde a numeri tra 2 e 4 cifre o parole di 3-5 lettere.|`born`, `on`, `the`, `train`, `IT456`, `to`, `Milan`, `on`, `at`, `used`, `the`, `with`, `the`, `for`, `note`, `the`, `is`, `For`, `us`, `at`, `code`, `The`, `was`, `made`, `at`, `on`|

---

## 9. Parole Accentate e Caratteri Non ASCII
- Queste regex permettono di individuare parole con lettere accentate o caratteri speciali non ASCII.

|Comando Regex|Spiegazione|Risultato della Regex|
|`\w+`|Corrisponde a una parola composta da caratteri alfanumerici ASCII. **Non cattura caratteri accentati o non ASCII.**|`Giovanni`, `Bianchi`, `born`, `on`, `purchased`, `the`, `train`, `ticket`, `IT456`, `to`, `Milan`, `on`, `at`, `He`, `used`, `the`, `credit`, `card`, `with`, `the`, `number`, `for`, `a`, `total`, `of`, `Please`, `note`, `the`, `is`, `For`, `assistance`, `please`, `contact`, `us`, `at`, `ascii`, `characters`, `Japanese`, `unicode`, `characters`, `Chinese`, `unicode`, `characters`, `The`, `transaction`, `code`, `is`, `The`, `booking`, `was`, `made`, `at`, `on`|
|`\b\w*[éèêëàáâäôöòóùúûüçñ]\w*\b`|Corrisponde a parole che contengono almeno una lettera accentata.|`rentrée`|
|`[^\x00-\x7F]+`|Corrisponde a qualsiasi carattere non ASCII.|`rentrée`, `予約`, `订单号码`|
|`\p{L}+`|Corrisponde a parole che contengono lettere, comprese quelle accentate (supporto Unicode).|`Giovanni`, `Bianchi`, `born`, `on`, `purchased`, `the`, `train`, `ticket`, `IT456`, `to`, `Milan`, `on`, `at`, `He`, `used`, `the`, `credit`, `card`, `with`, `the`, `number`, `for`, `a`, `total`, `of`, `Please`, `note`, `the`, `rentrée`, `fee`, `is`, `For`, `assistance`, `please`, `contact`, `us`, `at`, `ascii`, `characters`, `Japanese`, `unicode`, `characters`, `Chinese`, `unicode`, `characters`, `The`, `transaction`, `code`, `is`, `The`, `booking`, `was`, `made`, `at`, `on`, `予約`, `订单号码`|
|`\p{Latin}+`|Corrisponde solo a parole latine (esclude caratteri asiatici).|`Giovanni`, `Bianchi`, `born`, `on`, `purchased`, `the`, `train`, `ticket`, `IT456`, `to`, `Milan`, `on`, `at`, `He`, `used`, `the`, `credit`, `card`, `with`, `the`, `number`, `for`, `a`, `total`, `of`, `Please`, `note`, `the`, `rentrée`, `fee`, `is`, `For`, `assistance`, `please`, `contact`, `us`, `at`, `ascii`, `characters`, `Japanese`, `unicode`, `characters`, `Chinese`, `unicode`, `characters`, `The`, `transaction`, `code`, `is`, `The`, `booking`, `was`, `made`, `at`, `on`|
|`\p{Han}+`|Corrisponde a caratteri cinesi.|`订单号码`|
|`\p{Hiragana}+\|\p{Katakana}+`|Corrisponde a caratteri giapponesi in Hiragana o Katakana.|Nessuna corrispondenza|
|`\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}\b`|Corrisponde a un indirizzo email.|`giovanni.bianchi@example.com`, `予約@example.com`|
|`\b\d{2}/\d{2}/\d{4}\b`|Corrisponde a una data nel formato GG/MM/AAAA.|`12/11/1990`, `01/06/2025`, `15/03/2025`|
|`\b\d{4}-\d{4}-\d{4}-\d{4}\b`|Corrisponde a un numero di carta di credito.|`4111-1111-1111-1111`|
|`\b[A-Z]{2}\d+\b`|Corrisponde a un codice con due lettere maiuscole seguite da numeri.|`IT456`, `TXN987654321`|
| `\b\d{2}:\d{2}\b` | Corrisponde a un orario nel formato HH:MM. | `08:45`, `16:20` |
