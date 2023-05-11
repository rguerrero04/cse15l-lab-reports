# Lab Report 3
***Note:*** I have asked Chat GPT to help formulate this lab report the following are the results!\
I have chosen the command grep for this task. grep is a command-line utility for searching plain-text data sets for lines that match a regular expression pattern. Here are four interesting command-line options or alternate ways to use grep:

- **'-i'** option: This option tells grep to ignore case when searching for matches.\
Source: https://www.geeksforgeeks.org/grep-command-in-unix-linux/
```bash
grep -i "example" ./technical/example.txt
grep -i "line" ./technical/example.txt ./technical/example2.txt
```
The above commands will search for the string "example" and "line" (case-insensitive) in the file example.txt and files example.txt and example2.txt in the ./technical directory respectively.

- **'-n'** option: This option tells grep to display the line numbers of the matched lines.\
Source: https://www.cyberciti.biz/faq/how-to-grep-line-number-on-linux-unix/
```bash
grep -n "example" ./technical/example.txt
grep -n "grep" ./technical/*
```
The above commands will search for the string "example" and "grep" in the file example.txt and all files in the ./technical directory respectively, and display the line numbers of the matched lines.

- **'-r'** option: This option tells grep to search recursively in all directories under the given directory for the pattern.\
Source: https://www.tecmint.com/35-practical-examples-of-linux-find-command/
```bash
grep -r "example" ./technical/
grep -r "command" ./technical/
```
The above commands will search for the string "example" and "command" in all files under the ./technical directory recursively.

- **'-v'** option: This option tells grep to search for lines that do not match the pattern.\
Source: https://www.computerhope.com/unix/ugrep.htm
```bash
grep -v "example" ./technical/example.txt
grep -v "grep" ./technical/*
```
The above commands will search for lines in the file example.txt and all files in the ./technical directory that do not contain the string "example" and "grep", respectively.
