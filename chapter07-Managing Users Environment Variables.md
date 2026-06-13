# 📘 Chapter 7: Managing Environment Variables in Linux

## 🎯 Introduction

Environment variables are special values stored by the operating system that affect how programs and processes run.

They provide information about:
- Current user
- Home directory
- Shell settings
- System paths
- Running environment

Environment variables help users customize their Linux environment and improve productivity.

---

# 🌍 What Are Environment Variables?

Environment variables are dynamic values used by the shell and applications.

Examples:
- Username
- Home directory location
- Default shell
- System executable paths

---

# 🔍 Viewing Environment Variables

## Display All Environment Variables

```bash
env
```

or

```bash
printenv
```

These commands display all currently defined environment variables.

---

# 📋 Common Environment Variables

## USER

Displays the current username.

```bash
echo $USER
```

Example Output:

```bash
kali
```

---

## HOME

Displays the user's home directory.

```bash
echo $HOME
```

Example Output:

```bash
/home/kali
```

---

## SHELL

Displays the current shell being used.

```bash
echo $SHELL
```

Example Output:

```bash
/bin/bash
```

---

## PATH

Displays directories Linux searches when executing commands.

```bash
echo $PATH
```

Example Output:

```bash
/usr/local/bin:/usr/bin:/bin
```

---

# 🛣️ Understanding PATH

The PATH variable tells Linux where to search for executable programs.

Without PATH:

```bash
/usr/bin/ls
```

With PATH:

```bash
ls
```

Linux automatically searches directories listed in PATH.

---

# ➕ Creating Environment Variables

Create a temporary variable:

```bash
MYNAME=Mashallah
```

Display it:

```bash
echo $MYNAME
```

Output:

```bash
Mashallah
```

---

# 📌 Exporting Variables

To make a variable available to child processes:

```bash
export MYNAME=Mashallah
```

Check:

```bash
echo $MYNAME
```

---

# ✏️ Modifying PATH

Add a new directory to PATH:

```bash
export PATH=$PATH:/home/kali/tools
```

This tells Linux to also search:

```bash
/home/kali/tools
```

for executable files.

---

# 🗑️ Removing Variables

Delete an environment variable:

```bash
unset MYNAME
```

Verify:

```bash
echo $MYNAME
```

No output means the variable has been removed.

---

# ⚙️ Making Variables Permanent

Temporary variables disappear after logout.

To make them permanent:

Open:

```bash
nano ~/.bashrc
```

Add:

```bash
export MYNAME=Mashallah
```

Save and reload:

```bash
source ~/.bashrc
```

Now the variable loads automatically whenever Bash starts.

---

# 🕵️ Environment Variables and Cybersecurity

Hackers frequently use environment variables to:

- Customize tools
- Hide files and scripts
- Modify executable paths
- Automate tasks
- Maintain persistence

Understanding environment variables helps security professionals detect suspicious system modifications.

---

# 🧠 Key Points to Remember

- Environment variables store system information.
- `env` displays all variables.
- `printenv` displays environment variables.
- `echo $VARIABLE` displays a variable's value.
- `PATH` tells Linux where to search for executables.
- `export` creates variables available to child processes.
- `unset` removes variables.
- Permanent variables are stored in `.bashrc`.

---

# 🚀 Quick Revision Commands

```bash
env
printenv

echo $USER
echo $HOME
echo $SHELL
echo $PATH

export MYNAME=Mashallah

unset MYNAME

nano ~/.bashrc

source ~/.bashrc
```
