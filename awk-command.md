**Typical Uses of AWK**

Myriad of tasks can be done with AWK. Listed below are just a few of them −

1. Text processing,
2. Producing formatted text reports,
3. Performing arithmetic operations,
4. Performing string operations, and many more.

**Syntax:**

awk options 'selection _criteria {action }' input-file > output-file


| Commad                                         | Description                                           |
|------------------------------------------------|-------------------------------------------------------|
| awk '{print}' file-name.txt                    | Awk prints every line of data from the specified file |
| awk '/string/ {print}' file-name.txt           | Print the lines which match the given pattern         |
| awk '{print $1,$4}' file-name.txt              | Prints specific colums from the file                  |
| awk '{print NR,$0}' file-name.txt              | Display line numbers                                  |
| awk '{print $1,$NF}' file-name.txt             | Built-in NF variable to print the last line           |
| awk 'NR==3, NR==6 {print NR,$0}' file-name.txt | Print line range                                      |
| awk '{print NR "- " $1 }' file-name.txt        | Print first like with line number seperated by –      |
| awk 'END { print NR }' file-name.txt           | Count number of lines                                 |

