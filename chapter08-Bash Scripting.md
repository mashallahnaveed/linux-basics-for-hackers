#  Chapter 8: Bash Scripting

##  Introduction

Bash (Bourne Again Shell) is the default command-line shell in most Linux distributions.

A Bash script is a file containing Linux commands that are executed automatically, allowing users to automate repetitive tasks.

---

# Why Learn Bash Scripting?

Bash scripting helps:

* Automate tasks
* Save time
* Manage systems efficiently
* Create security tools
* Perform penetration testing activities

---

#  What is a Bash Script?

A Bash script is simply a text file containing Linux commands.

Example:

```bash
#!/bin/bash

echo "Hello World"
```

### Explanation:

* `#!/bin/bash` → Shebang (tells Linux to use Bash interpreter)
* `echo` → Prints text to the screen

---

#  Creating Your First Script

Create a script:

```bash
nano hello.sh
```

Add:

```bash
#!/bin/bash

echo "Hello Hackers!"
```

Save and exit.

---

#  Setting Execute Permissions

Scripts must have execute permissions before running.

```bash
chmod +x hello.sh
```

### Explanation:

* `chmod` → Change permissions
* `+x` → Add execute permission

---

#  Running a Script

Execute the script:

```bash
./hello.sh
```

Output:

```bash
Hello Hackers!
```

---

#  Variables in Bash

Variables store data.

Example:

```bash
#!/bin/bash

name="Mashallah"

echo $name
```

Output:

```bash
Mashallah
```

---

#  User Input

Accept input from users:

```bash
#!/bin/bash

echo "Enter your name:"
read name

echo "Welcome $name"
```

### Commands:

* `read` → Accept user input
* `echo` → Display output

---

#  Using Variables in Scripts

Example:

```bash
#!/bin/bash

echo "Enter Target IP:"
read ip

echo "Target IP is $ip"
```

Output depends on user input.

---

#  Conditional Statements

## If Statement

```bash
#!/bin/bash

if [ 5 -gt 3 ]
then
    echo "True"
fi
```

### Common Operators

| Operator | Meaning          |
| -------- | ---------------- |
| -eq      | Equal            |
| -ne      | Not Equal        |
| -gt      | Greater Than     |
| -lt      | Less Than        |
| -ge      | Greater or Equal |
| -le      | Less or Equal    |

---

#  Loops

## For Loop

```bash
for i in 1 2 3 4 5
do
    echo $i
done
```

Output:

```bash
1
2
3
4
5
```

---

## While Loop

```bash
count=1

while [ $count -le 5 ]
do
    echo $count
    count=$((count+1))
done
```

---

#  Simple Port Scanner Script

Example:

```bash
#!/bin/bash

echo "Enter IP Address:"
read ip

nmap $ip
```

### Purpose:

* Takes target IP address
* Scans open ports using Nmap

---

#  Useful Bash Commands

### Echo

```bash
echo "Hello"
```

Displays text.

---

### Read

```bash
read variable
```

Stores user input.

---

### Sleep

```bash
sleep 5
```

Pauses execution for 5 seconds.

---

### Exit

```bash
exit
```

Stops script execution.

---

#  Bash Scripting in Cybersecurity

Bash scripts are used for:

* Port scanning
* Log analysis
* User management
* Network monitoring
* Automation of security tasks
* Reconnaissance

Many penetration testing tools use Bash scripts behind the scenes.

---

#  Key Points to Remember

* Bash is the default Linux shell.
* Scripts automate repetitive tasks.
* `#!/bin/bash` defines the interpreter.
* `chmod +x` makes scripts executable.
* `./script.sh` runs a script.
* Variables store data.
* `read` accepts user input.
* `if` performs conditional checks.
* Loops repeat actions.
* Bash scripting is heavily used in cybersecurity.

---

#  Quick Revision Commands

```bash
nano script.sh

chmod +x script.sh

./script.sh

echo

read

if

for

while

sleep

exit
```

These notes cover the main concepts from Chapter 8 and are perfect for both GitHub documentation and quiz preparation. 🚀
