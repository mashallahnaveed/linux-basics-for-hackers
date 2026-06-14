#  Chapter 10: Filesystem and Storage Device Management

## Introduction

Linux provides powerful tools for managing filesystems, partitions, and storage devices. As a cybersecurity professional, understanding storage devices and filesystems is important for system administration, digital forensics, and incident response.

This chapter focuses on:
- Storage devices
- Partitions
- Filesystems
- Mounting and unmounting devices
- Checking disk information

---

#  Understanding Storage Devices

Storage devices are hardware used to store data.

Examples:
- Hard Disk Drives (HDD)
- Solid State Drives (SSD)
- USB Flash Drives
- SD Cards

In Linux, storage devices are represented as files inside the `/dev` directory.

Examples:

```bash
/dev/sda
/dev/sdb
/dev/sdc
````

### Naming Convention

* `sda` → First storage device
* `sdb` → Second storage device
* `sdc` → Third storage device

Partitions are represented as:

```bash
/dev/sda1
/dev/sda2
/dev/sdb1
```

---

#  Filesystems

A filesystem determines how data is organized and stored on a disk.

Common Linux filesystems:

| Filesystem | Description                  |
| ---------- | ---------------------------- |
| ext2       | Older Linux filesystem       |
| ext3       | Journaling filesystem        |
| ext4       | Most common Linux filesystem |
| FAT32      | Compatible with Windows      |
| NTFS       | Windows filesystem           |

---

#  Viewing Storage Devices

## List Block Devices

```bash
lsblk
```

Displays:

* Storage devices
* Partitions
* Mount points
* Device sizes

Example Output:

```bash
sda      100G
├─sda1    99G
└─sda2     1G
```

---

#  Viewing Disk Usage

## Display Disk Information

```bash
df -h
```

### Explanation

* `df` → Disk Free
* `-h` → Human-readable format

Displays:

* Total storage
* Used storage
* Available storage

---

# Checking Directory Size

```bash
du -h
```

### Explanation

* `du` → Disk Usage
* `-h` → Human-readable format

Shows storage used by files and directories.

---

#  Mounting Filesystems

Before Linux can access a storage device, it must be mounted.

## Mount a Device

```bash
mount /dev/sdb1 /mnt
```

### Explanation

* `/dev/sdb1` → Device
* `/mnt` → Mount point

The device becomes accessible through `/mnt`.

---

# Unmounting Filesystems

To safely remove a device:

```bash
umount /dev/sdb1
```

or

```bash
umount /mnt
```

### Why Unmount?

Prevents:

* Data corruption
* Incomplete writes
* File damage

---

# Identifying Filesystems

Display filesystem information:

```bash
fdisk -l
```

### Displays:

* Disks
* Partitions
* Filesystem information
* Partition sizes

---

# Creating Filesystems

Create an ext4 filesystem:

```bash
mkfs.ext4 /dev/sdb1
```

### Warning

This command erases all existing data on the partition.

---

# Checking Filesystem Integrity

Linux provides tools to check and repair filesystems.

## Filesystem Check

```bash
fsck /dev/sdb1
```

### Purpose

* Detect filesystem errors
* Repair corrupted filesystems
* Verify filesystem integrity

---

# Understanding Inodes

An inode stores information about a file:

* Owner
* Permissions
* File size
* Creation date
* Location on disk

Each file in Linux has a unique inode number.

---

# Viewing Inode Information

```bash
ls -i
```

Example:

```bash
12345 file.txt
```

Where:

* `12345` = inode number

---

# Viewing Detailed Filesystem Information

```bash
dumpe2fs /dev/sdb1
```

Displays:

* Filesystem details
* Inode information
* Block information
* Mount information

---

#  Importance in Cybersecurity

Filesystem and storage management are important because they help:

* Analyze storage devices
* Recover data
* Investigate incidents
* Manage forensic images
* Verify filesystem integrity
* Monitor disk usage

---

#  Key Points to Remember

* Storage devices are located in `/dev`.
* `lsblk` displays disks and partitions.
* `df -h` displays disk usage.
* `du -h` displays directory size.
* Filesystems organize data on storage devices.
* `mount` connects a device to the filesystem.
* `umount` safely disconnects a device.
* `fdisk -l` displays partition information.
* `mkfs.ext4` creates an ext4 filesystem.
* `fsck` checks filesystem integrity.
* Inodes store file metadata.
* `ls -i` displays inode numbers.

---

#  Quick Revision Commands

```bash
lsblk

df -h

du -h

fdisk -l

mount /dev/sdb1 /mnt

umount /dev/sdb1

mkfs.ext4 /dev/sdb1

fsck /dev/sdb1

ls -i

dumpe2fs /dev/sdb1
```

---
```

