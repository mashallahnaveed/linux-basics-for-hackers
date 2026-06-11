# 📘 Chapter 4: Process Management & System Information in Linux

---

## 🎯 Introduction

A **process** is a program that is currently running on the system. Linux provides various commands to monitor, manage, and control processes. Understanding processes is important for system administration and cybersecurity.

---

# ⚙️ What is a Process?

A process is an active instance of a program.

Examples:

* Web browser running
* Text editor open
* Background services running on the system

Each process is assigned a unique **Process ID (PID)**.

---

# 📋 Viewing Running Processes

### Show Current User Processes

```bash
ps
```

Displays processes running in the current terminal session.

### Show All Processes

```bash
ps aux
```

Displays detailed information about all running processes.

---

# 📊 Monitoring Processes

### Real-Time Process Monitoring

```bash
top
```

Shows:

* CPU usage
* Memory usage
* Running processes
* System load

### Advanced Process Monitor

```bash
htop
```

Provides a more user-friendly and interactive interface than `top`.

> Note: `htop` may need to be installed separately.

---

# ❌ Terminating Processes

### Kill a Process

```bash
kill PID
```

Example:

```bash
kill 1234
```

Stops the process with PID 1234.

### Force Kill a Process

```bash
kill -9 PID
```

Example:

```bash
kill -9 1234
```

Forcefully terminates the process if it does not respond.

---

# 🔍 Finding Process Information

### Search for a Process

```bash
pgrep process_name
```

Example:

```bash
pgrep firefox
```

Returns the PID of the specified process.

### Display Process Tree

```bash
pstree
```

Shows parent-child relationships between processes.

---

# 💾 Disk Usage Information

### View Disk Space

```bash
df -h
```

Displays:

* Total storage
* Used storage
* Available storage

### Check Directory Size

```bash
du -h
```

Shows the size of files and directories.

---

# 🧠 Memory Information

### View RAM Usage

```bash
free -h
```

Displays:

* Total memory
* Used memory
* Free memory
* Swap memory

---

# 🖥️ System Information

### Display Kernel and System Information

```bash
uname -a
```

Shows:

* Kernel version
* System architecture
* Hostname

### Display Hostname

```bash
hostname
```

Shows the system's hostname.

---

# 📜 Command History

### View Previous Commands

```bash
history
```

Lists commands previously executed in the terminal.

### Repeat Last Command

```bash
!!
```

Executes the most recent command again.

---

# 🔐 Importance in Cybersecurity

Process management helps security professionals:

* Detect suspicious activities
* Monitor resource usage
* Identify malware processes
* Investigate system performance issues
* Manage running services securely

---

# 🧠 Key Points to Remember

* A process is a running program.
* Every process has a unique PID.
* `ps` displays running processes.
* `top` and `htop` monitor processes in real time.
* `kill` terminates a process.
* `kill -9` forcefully stops a process.
* `df -h` shows disk usage.
* `free -h` shows memory usage.
* `uname -a` displays system information.
* `history` shows previously executed commands.

---

## 🚀 Quick Revision Commands

```bash
ps
ps aux
top
htop
kill PID
kill -9 PID
pgrep process_name
pstree
df -h
du -h
free -h
uname -a
hostname
history
!!
```
