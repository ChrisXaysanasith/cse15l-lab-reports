# Lab Report 3

## Bugs and Commands

**grep -r**
look for all files in the current directory and in its subdirectories 
'shoot' technical/911report

**grep -c**
search and display the total number of times
* 'shoot'
technical/911report/chapter-1.txt

**grep -iw** 
searching only the word
* "is" 
technical/911report/chapter-1.txt

**grep -n**
Display the matched lines and their line numbers
* "9/11" 
technical/911report/chapter-1.txt



find ./technical/911report/ -name "chapter-[0-12].txt"
find ./technical/911report/ -name "chapter"

**Citation:**

ChatGPT - "what commands can i use with -name"

**ChatGPT output:**

"-name "file[0-9].txt": Use square brackets to match a single character from a specified range. This matches names like "file0.txt," "file1.txt," etc."

https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/

https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/
