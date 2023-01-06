# Further On Bash
## Regular Expressions! /regex/
- How do this site know that our input is not email?
- Most filter Validation on any platform done by Regular 
expression/regex/.
- They are patterns that helps to filter so texts,space,tabs & 
symbols.
- Like telegram or other platforms filtering links inside 
group, filtering some bad words.. All are regex.
- Regex is PATTERN!
- Regex are used on linux tools called grep,awk and sed
To exercise this we can simply use vscode search tool.
- And don’t forget to turn the regex button on
- The pattern is same but the implementation may differ on programming languages.
- On Python,
## Metacharacters 
- Those are regex pattern symbols for filter.
- They are :
### Dot ( . )
- Used to get All the line except new lines
- Syntax: .
    - This means give me all lines except the new lines
### Caret ( ^ ) - Assertion 
- Used to get line that start with pattern
- Syntax: ^hello
    - This means lines that start with hello
### Dollar sign( $ ) - Assertion 
- Used to get line that ends with some pattern.
- Syntax: hello$
    - That ends with hello$     
### Plus ( + ) - Quantity 
- Used to get line that have pattern that occurs 1 and more times.
- Syntax: hellos+
    - A text hello that have s at least 1 times and more.   
### Asteriks ( * ) - Quantity 
- Used to get line that have pattern that occurs 0 and more times.
- Syntax: hellos*
    - A text hello that have s at least 0 times and more.
### Question mark ( ? ) - Quantity 
- Used to get line that have pattern that occurs 0 and 1 times.
- Syntax: hellos?
    - A text hello that have s at least 0 time or 1 time.


#### We need to get texts that starts with n and ends with com 
including all the texts between those 2 expressions… 
- STart with n = ^n
- End with com = com$
- All Test between them = .* , .+
- We can do it in 1 line
- ^n.*com$



### Curly Bracket ( { min , max} ) - Quantity
- Used to get line that have pattern that occurs min and max times.it is custom
- Syntax: hellos{1,3}
    - A text hello that have s at least 0 times and more.
        - {1,} = plus sign
        - {0,} = asterisk
        - {0,1} = what..
## We need to get texts that starts with n and ends with com 
including the texts that have 7-13 character between those 2 
expressions… 
- STart with n = ^n
- End with com = com$
- 7-10 character = .{7,13}
- We can do it in 1 line
- ^n.{7,13}com$
### \w 
- Used to get Alphanumeric 
- Syntax: \w
    - All texts except newlines and symbols
### \W 
- Used to get All except Alphanumeric 
- Syntax: \W
### \s 
- Used to get whitespace.
- Syntax: \s
### \S 
- Used to get all except whitespace.
- Syntax: \S
### \d 
- Used to get Digits/numbers/
- Syntax: \d
### \D 
- Used to get all except Digits/numbers/
- Syntax: \D
### Pipe ( | ) - OR
- Used to search 2 different things.
- Syntax: a|b    
### Escape ( \ ) 
- Used to search symbols that are metacharacters.
- Syntax: \sign 
### Square Brackets ( [ ] ) - Custom pattern
- Used to Create your own patterns
- Syntax: [pattern]
## Bash regex
- You can use it on awk, sed, but for today i will show you using grep.
## Bash else if
- To do more than 1 comparing.
- It is same with python is is “elif”
## Loops
- On Bash, there are 3 types of Loops

         a. For loop 

         b. While Loop 
         
         c. Until Loop
         
## For loops
- The iteration may be different here. We can use arrays like list on 
python but we dont have range in bash but we can do {a..b} this 
iterates from a to b    

## For Loop with increment/decrement
- Same with index slicing but here if for looping.
### Continue Statement
- Is A function that helps to break the loop there and start if from the up 
again.
### Until loop
- It is same but this one exits the loop when the expression is true.
- The name until means እስከ
- When you have function and the arguments will be $1, $2 ….
- If we use $? it will call the return value.
## BASH and Linux
- We can run linux commands inside our bash
    >> You can run bash codesin 1 line.
    >> You can access files in current directory using * sign 
## Interaction with linux
- You can interact with linux terminal using bash.
- For this our codes are bash so, your terminal have to be on bash
- Command: /bin/BASH
### For loop on terminal