SED can be used in many different ways, such as:

1. Text substitution,
2. Selective printing of text files,
3. In-a-place editing of text files,
4. Non-interactive editing of text files, and many more.

**SED is available by default on most GNU/Linux distributions. If not, then install SED on Debian based GNU/Linux using apt package manager as follows:**

$ sudo apt-get install sed 

**After installation, ensure that SED is accessible via command line.**

$ sed --version

**Syntax:**

sed OPTIONS... [SCRIPT] [INPUTFILE...] 

| Command                               | Description                                                |
|---------------------------------------|------------------------------------------------------------|
| sed 's/unix/linux/' file-name.txt     | Replace word unix with linux and show output               |
| sed 's/unix/linux/2' file-name.txt    | Replace nth occurrence of a pattern in a line              |
| sed 's/unix/linux/g' file-name.txt    | Replacing all the occurrence of the pattern in a line      |
| sed 's/unix/linux/3g' file-name.txt   | Replacing from nth occurrence to all occurrences in a line |
| sed '3 s/unix/linux/' file-name.txt   | Replacing string on a specific line number                 |
| sed '1,3 s/unix/linux/' file-name.txt | Replacing string on a range of lines                       |
| sed -n 's/unix/linux/p' file-name.txt | Print only replaced lines                                  |
| sed '$d' file-name.txt                | To Delete a last line                                      |
| sed '3,6d' file-name.txt              | To Delete line from range x to y                           |
| sed '12,$d' file-name.txt             | To Delete from nth to last line                            |
| sed '/abc/d' file-name.txt            | To Delete pattern matching line                            |
| sed -i 's/unix/linux/g' file-name.txt | To replace a string infile                                 |


