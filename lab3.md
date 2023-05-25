# Lab Report 3
***Note:*** I have asked Chat GPT to help formulate this lab report the following are the results!\
***Note:*** The outputs below are examples and may vary depending on the contents of the files and directories in the ``./technical`` directory.\
I have chosen the command grep for this task. grep is a command-line utility for searching plain-text data sets for lines that match a regular expression pattern. Here are four interesting command-line options or alternate ways to use grep:

- **'-i'** option: This option tells grep to ignore case when searching for matches.\
Source: [grep command in Unix/Linux](https://www.geeksforgeeks.org/grep-command-in-unixlinux/#)
```bash
grep -i "example" ./technical/example.txt 
grep -i "line" ./technical/example.txt ./technical/example2.txt
```
Outputs:
```bash
$ grep -i "example" ./technical/example.txt
This is an example file.
This is another example line.
$ grep -i "line" ./technical/example.txt ./technical/example2.txt
./technical/example.txt:This is another example line.
```
The above commands will search for the string "example" and "line" (case-insensitive) in the file example.txt and files example.txt and example2.txt in the ./technical directory respectively.

- **'-n'** option: This option tells grep to display the line numbers of the matched lines.\
Source: [How To Use grep Command In Linux / UNIX With Practical Examples](https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/)
```bash
grep -n "example" ./technical/example.txt
grep -n "grep" ./technical/*
```
Outputs:
```bash
$ grep -n "example" ./technical/example.txt
1:This is an example file.
3:This is another example line.
$ grep -n "grep" ./technical/*
./technical/example2.txt:3:This is a test for grep command.
```
The above commands will search for the string "example" and "grep" in the file example.txt and all files in the ./technical directory respectively, and display the line numbers of the matched lines.

- **'-r'** option: This option tells grep to search recursively in all directories under the given directory for the pattern.\
Source: [35 Practical Examples of Linux Find Command](https://www.tecmint.com/35-practical-examples-of-linux-find-command/)
```bash
grep -r "example" ./technical/
grep -r "command" ./technical/
```
Outputs:
```bash
$ grep -r "example" ./technical/
./technical/example.txt:This is an example file.
./technical/example.txt:This is another example line.
./technical/subdirectory/subexample.txt:This is a subdirectory example.
$ grep -r "command" ./technical/
./technical/example2.txt:This is a test for grep command.
```
The above commands will search for the string "example" and "command" in all files under the ./technical directory recursively.

- **'-v'** option: This option tells grep to search for lines that do not match the pattern.\
Source: [Linux grep command](https://www.computerhope.com/unix/ugrep.htm)
```bash
grep -v "example" ./technical/example.txt
grep -v "grep" ./technical/*
```
Outputs:
```bash
$ grep -v "example" ./technical/example.txt
This is a test for grep command.
$ grep -v "grep" ./technical/*
./technical/example.txt:This is an example file.
./technical/example.txt:This is another example line.
./technical/example.txt:This is a test for find command.
./technical/example.txt:This is a test for less command.
./technical/subdirectory/subexample.txt:This is a subdirectory example.
```
The above commands will search for lines in the file example.txt and all files in the ./technical directory that do not contain the string "example" and "grep", respectively.\
## The Prompt Provided to Chat GPT Below:
Consider the commands less, find, and grep. Choose one of them. Online, find 4 interesting command-line options or alternate ways to use the command you chose. For example, we saw the -name option for find in class. For each of those options, give 2 examples of using it on files and directories from ./technical. Show each example as a code block that shows the command and its output, and write a sentence or two about what it’s doing and why it’s useful.

That makes 8 total examples, all focused on a single command. There should be two examples each for four different command-line options. Many commands like these have pretty sophisticated behavior possible – it can take years to be exposed to and learn all of the possible tricks and inner workings.

Along with each option/mode you show, cite your source for how you found out about it as a URL or a description of where you found it.

To find information about the commands, a simple Web search like “find command-line options” will probably give decent results. There is also a built-in command on many systems called man (short for “manual”) that displays information about commands; you can use man grep, for example, to see a long listing of information about how grep works.
