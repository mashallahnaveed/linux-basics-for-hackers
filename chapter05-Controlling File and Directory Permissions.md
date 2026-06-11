# 📘 Chapter 5: Controlling File and Directory Permissions

## 🎯 Objective

Learn how Linux controls access to files and directories using permissions, ownership, and special privilege settings.

---

## 👥 Types of Users

Linux categorizes users into three groups:

| User Type  | Description                 |
| ---------- | --------------------------- |
| User (u)   | Owner of the file           |
| Group (g)  | Members of the file's group |
| Others (o) | Everyone else on the system |

---

## 📋 Viewing Permissions

Use the following command to view file permissions:

```bash
ls -l
```

### Example Output

```bash
-rwxr-xr-- 1 kali kali 1024 file.txt
```

### Permission Breakdown

```text
-rwxr-xr--
│││ │││ │││
│││ │││ │└└─ Others
│││ └└└──── Group
└└└──────── User (Owner)
```

---

## 🔑 Permission Types

| Symbol | Meaning       |
| ------ | ------------- |
| r      | Read          |
| w      | Write         |
| x      | Execute       |
| -      | No Permission |

### Numerical Values

| Permission  | Value |
| ----------- | ----- |
| Read (r)    | 4     |
| Write (w)   | 2     |
| Execute (x) | 1     |

---

## 🛠 Changing Permissions with chmod

### Syntax

```bash
chmod permissions filename
```

### Example

```bash
chmod 755 script.sh
```

### Permission Values

| Value | Meaning                           |
| ----- | --------------------------------- |
| 777   | Full permissions                  |
| 755   | Owner full, others read & execute |
| 700   | Owner only                        |
| 644   | Owner read/write, others read     |

---

## 🔄 Symbolic Method (UGO)

### UGO Meaning

| Symbol | Description |
| ------ | ----------- |
| u      | User        |
| g      | Group       |
| o      | Others      |
| a      | All         |

### Examples

Give execute permission to owner:

```bash
chmod u+x script.sh
```

Remove write permission from group:

```bash
chmod g-w file.txt
```

Give read permission to everyone:

```bash
chmod a+r file.txt
```

---

## 👑 Changing Ownership

### Change File Owner

```bash
sudo chown username filename
```

Example:

```bash
sudo chown kali file.txt
```

---

## 👥 Change Group Ownership

```bash
sudo chgrp groupname filename
```

Example:

```bash
sudo chgrp admin file.txt
```

---

## 🔐 Special Permissions

### SUID (Set User ID)

Allows a user to run a file with the owner's privileges.

```bash
chmod u+s filename
```

Example:

```bash
chmod u+s mytool
```

---

### SGID (Set Group ID)

Runs a file with the group's privileges.

```bash
chmod g+s filename
```

---

### Sticky Bit

Prevents users from deleting files owned by others inside shared directories.

```bash
chmod +t directory
```

Example:

```bash
chmod +t /tmp
```

---

## ⚠ Security Considerations

* Avoid giving unnecessary permissions.
* Never use `777` unless absolutely necessary.
* Regularly review file permissions.
* Misconfigured permissions can lead to privilege escalation attacks.

---

## 📚 Important Commands Summary

```bash
ls -l                    # View permissions
chmod 755 file           # Change permissions
chmod u+x file           # Add execute permission
chown user file          # Change owner
chgrp group file         # Change group
chmod u+s file           # Set SUID
chmod g+s file           # Set SGID
chmod +t directory       # Set Sticky Bit
```

---

## ✅ Key Takeaways

* Linux uses User, Group, and Others permission levels.
* Permissions are controlled using Read, Write, and Execute.
* `chmod` modifies permissions.
* `chown` and `chgrp` modify ownership.
* Special permissions (SUID, SGID, Sticky Bit) provide advanced access control.
* Proper permission management is essential for Linux security and privilege management.

---
