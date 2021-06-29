# Regular Expressions in Python

At first import mudule re
```
import re
```

## Basic Patterns: Ordinary Characters


Ordinary characters can be used to perform simple exact matches:
```
pattern = r"Cookie"
sequence = "Cookie"
if re.match(pattern, sequence):
    print("Match!")
else: print("Not a match!")

```
will return : Match!

- The r before the string is called raw string literal. It changes how the string literal is interpreted. Such literals are stored as they appear.

For example, \ is just a backslash when prefixed with an r rather than being interpreted as an escape sequence. You will see what this means with special characters. Sometimes, the syntax involves backslash-escaped characters, and to prevent these characters from being interpreted as escape sequences; you use the raw r prefix.


## Wild Card Characters: Special Characters

- dot :
 Matches any single character except the newline character.
```
re.search(r'Co.k.e', 'Cookie').group()
'Cookie'
```

- ^ :  Matches the start of the string.

```
re.search(r'^Eat', "Eat cake!").group()

will return 'Eat'
```

- $ : Matches the end of string.

```

re.search(r'cake$', "Cake! Let's eat cake").group()

will return 'cake'

```

- (-): Range

```
re.search(r'[0-6]', 'Number: 5').group()

will return '5'
```

Another example :

```
## Matches any character except 5
re.search(r'Number: [^5]', 'Number: 0').group()

will return 'Number: 0'
```

- \ - Backslash.
Perhaps, the most diverse metacharacter!!

If the character following the backslash is a recognized escape character, then the special meaning of the term is taken (Scenario 1)
Else if the character following the \ is not a recognized escape character, then the \ is treated like any other character and passed through (Scenario 2).
\ can be used in front of all the metacharacters to remove their special meaning (Scenario 3).

```
## (Scenario 1) This treats '\s' as an escape character, '\s' defines a space
re.search(r'Not a\sregular character', 'Not a regular character').group()
'Not a regular character'
```

```
## (Scenario 2) '\' is treated as an ordinary character, because '\r' is not a recognized escape character
re.search(r'Just a \regular character', 'Just a \regular character').group()
'Just a \regular character'
```

```
## (Scenario 3) '\s' is escaped using an extra `\` so its interpreted as a literal string '\s'
re.search(r'Just a \\sregular character', 'Just a \sregular character').group()
'Just a \\sregular character'
```


- \d - Lowercase d. Matches decimal digit 0-9.
- \D - Uppercase d. Matches any character that is not a decimal digit.

# Example for \d
```
print("How many cookies do you want? ", re.search(r'\d+', '100 cookies').group())
How many cookies do you want?  100
```

## Repetitions

- +: Checks if the preceding character appears one or more times starting from that position.
```
re.search(r'Co+kie', 'Cooookie').group()
'Cooookie'
```

- *: Checks if the preceding character appears zero or more times starting from that position.
```
re.search(r'Ca*o*kie', 'Cookie').group()
'Cookie'

```

- ?: Checks if the preceding character appears exactly zero or one time starting from that position.

- {x} - Repeat exactly x number of times.

- {x,} - Repeat at least x times or more.

- {x, y} - Repeat at least x times but no more than y times.
```
re.search(r'\d{9,10}', '0987654321').group()
'0987654321'
```

## Grouping in Regular Expressions
The group feature of regular expression allows you to pick up parts of the matching text. Parts of a regular expression pattern bounded by parenthesis () are called groups
```
statement = 'Please contact us at: support@datacamp.com'
match = re.search(r'([\w\.-]+)@([\w\.-]+)', statement)
if statement:
  print("Email address:", match.group()) # The whole matched text
  print("Username:", match.group(1)) # The username (group 1)
  print("Host:", match.group(2)) # The host (group 2)

  ```

  ```
Email address: support@datacamp.com
Username: support
Host: datacamp.com

```


Another way of doing the same is with the usage of <> brackets instead. This will let you create named groups. Named groups will make your code more readable. The syntax for creating named group is: (?P<name>...). Replace the name part with the name you want to give to your group. The ... represent the rest of the matching syntax. See this in action using the same example as before...

```
statement = 'Please contact us at: support@datacamp.com'
match = re.search(r'(?P<email>(?P<username>[\w\.-]+)@(?P<host>[\w\.-]+))', statement)
if statement:
  print("Email address:", match.group('email'))
  print("Username:", match.group('username'))
  print("Host:", match.group('host'))
  ```
  ```
Email address: support@datacamp.com
Username: support
Host: datacamp.com

```