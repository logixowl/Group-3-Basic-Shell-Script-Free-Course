## Linux Regular Expressions

| No. | Metacharacter | Description |
| --- | --- | --- |
| 1 | ```.``` | Replaces any character |
| 2 | ```^``` | Matches start of string/represents characters not in the string |
| 3 | ```$``` | Matches end of string |
| 4 | ```?``` | Matches 0 or 1 preceding character |
| 5 | ```*``` | Matches 0 or more times preceding character |
| 6 | ```+``` | Matches 1 or more times preceding character |
| 7 | ```\``` | Represents special characters |
| 8 | ```()``` | Groups regular expressions |
| 9 | ```{n}``` | Matches preceding character appearing n times exactly |
| 10 | ```{n,}``` | Matches preceding character appearing n times or more |
| 11 | ```{n,m}``` | Matches preceding character appearing n times, but not more than n times |
| 12 | ```-``` | Represents the range. |
| 13 | ```\<``` | Matches empty string at the beginning of a word. |
| 14 | ```\>``` | Matches empty string at the end of a word. |

### အလုပ်လုပ်ပုံတူတဲ့ ပုံစံများ

| No. | regex | same with | desc |
| --- | --- | --- | --- |
| 1 | ```[[:alnum:]]``` | ```[a-z A-Z 0-9]``` | Alphanumeric |
| 2 | ```[[:alpha:]]``` | ```[a-z A-Z]``` | Alphabetic |
| 3 | ```[[:blank:]]``` | - | Blank characters (spaces or tabs) |
| 4 | ```[[:cntrl:]]``` | - | Control characters  |
| 5 | ```[[:digit:]]``` | ```[0-9]``` | Numbers |
| 6 | ```[[:graph:]]``` | - | Any visible characters (excludes whitespace) |
| 7 | ```[[:lower:]]``` | ```[a-z]``` | Lowercase letters |
| 8 | ```[[:print:]]``` | - | Printable characters (non-control characters) |
| 9 | ```[[:punct:]]``` | - | Punctuation characters |
| 10 | ```[[:space:]]``` | - | Whitespace |
| 11 | ```[[:upper:]]``` | ```[A-Z]``` | Uppercase letters |
| 12 | ```[[:xdigit:]]``` | ```[0-9 a-f A-F]``` | Hex digits |
