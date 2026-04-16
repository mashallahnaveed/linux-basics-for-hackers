📘 Chapter 2: Text Manipulation

🧠 Overview

This chapter focuses on manipulating and analyzing text in Linux. These commands are essential for handling files, searching content, and processing data efficiently.

📂 Viewing Files

🔹 cat

Displays the entire content of a file.

cat filename.txt

Best for small files

Prints everything at once

🔹 head

Displays the first few lines of a file.

head filename.txt

Default: first 10 lines

head -n 5 filename.txt

Shows first 5 lines

🔹 tail

Displays the last few lines of a file.

tail filename.txt

Default: last 10 lines

tail -n 5 filename.txt

Shows last 5 lines

🔹 nl

Numbers the lines of a file.

nl filename.txt

Useful for debugging and referencing lines

🔍 Searching & Filtering Text

🔹 grep

Searches for specific patterns in a file.

grep "word" filename.txt

Displays lines containing "word"

grep -i "word" filename.txt

Case-insensitive search

grep -v "word" filename.txt

Shows lines that do NOT contain "word"

✏️ Editing Text

🔹 sed

Used for finding and replacing text.

sed 's/old/new/' filename.txt

Replaces first occurrence in each line

sed 's/old/new/g' filename.txt

Replaces all occurrences

📖 Viewing Large Files

🔹 more

Displays file content page by page.

more filename.txt

Space → next page

Enter → next line

🔹 less

Advanced file viewer.

less filename.txt

Scroll up/down

Search using /word

More flexible than more

🔗 Combining Commands (Piping)

🔹 |

Pass output of one command as input to another.

cat file.txt | grep "error"

Filters output of cat

head file.txt | tail -n 5

Extracts specific lines

⚡ Quick Summary

Command	Description

cat	Display full file

head	Show beginning of file

tail	Show end of file

nl	Number lines

grep	Search text

sed	Replace text

more	View file (basic)

less	View file (advanced)

💡 Pro Tip

These commands become powerful when combined. Mastering them is key for:

Ethical Hacking

Log Analysis

Automation
Data Processing
