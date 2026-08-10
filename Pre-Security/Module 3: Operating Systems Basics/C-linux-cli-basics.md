# C. Linux CLI Basics

## Terminal

The terminal is a text-based interface for controlling and interacting with a Linux system.

Cybersecurity professionals commonly use the terminal because:

- It is faster than using graphical interfaces for many tasks.
- It provides more control over the system.
- Many Linux and cybersecurity tools are primarily operated through the CLI.

---

## Common Linux Commands

### 1. `pwd`

`pwd` stands for **"print working directory."**

It displays the path of the directory you are currently in.

    pwd

---

### 2. `ls`

The `ls` command lists the contents of the current directory.

    ls

---

### 3. `ls -l`

The `ls -l` command displays detailed information about files and directories, including:

- File permissions
- Ownership
- File size
- Modification date
- File name

    ls -l

---

### 4. Hidden Files — `ls -a`

The `ls -a` command displays all files in the directory, including hidden files.

    ls -a

In Linux, hidden files normally begin with a `.` (dot), for example:

    .config
    .bashrc

Hidden files are not necessarily secret. Linux simply hides them from the normal `ls` output by default.

---

### 5. `cd`

The `cd` command is used to change directories and move through the filesystem.

    cd <directory>

#### Go Back One Level

The `..` notation represents the parent directory.

    cd ..

This moves you one level back in the filesystem.

---

### 6. `find`

The `find` utility is used to locate files within the filesystem.

    find <starting-point> -name <filename>

Example:

    find /home -name "notes.txt"

This searches for `notes.txt` starting from the `/home` directory.

---

### 7. `cat`

The `cat` command is commonly used to read and display the contents of a file.

    cat <filename>

Example:

    cat notes.txt

---

### 8. `whoami`

The `whoami` command displays the username of the currently logged-in user.

    whoami

This is particularly useful when working with multiple user accounts or during cybersecurity labs.

---

### 9. `uname -a`

The `uname -a` command displays detailed information about the system.

    uname -a

It can provide information about:

- Operating system/kernel
- Hostname
- Kernel version
- System architecture

Example output:

    Linux <hostname> <kernel-version> ... x86_64 GNU/Linux

#### Understanding the Output

- **Linux** — The system is running the Linux kernel.
- **Hostname** — The name of the computer.
- **Kernel version** — The version of the Linux kernel installed.
- **x86_64** — The system architecture is 64-bit.
- **GNU/Linux** — Indicates the Linux/GNU operating-system environment.

---

### 10. Check Disk & Storage Information — `df -h`

The `df` command displays information about available and used disk space.

The `-h` option means **"human-readable."**

It displays storage sizes in easier-to-read formats such as:

    2G
    500M

Command:

    df -h

Example output:

    Filesystem      Size  Used  Avail  Use%  Mounted on
    /dev/...        20G   12G    8G    60%   /
    tmpfs           1.9G   0     1.9G    0%   /dev/shm

#### Understanding the Output

- **Filesystem** — The filesystem or storage device.
- **Size** — Total size of the filesystem.
- **Used** — Space currently being used.
- **Avail** — Available free space.
- **Use%** — Percentage of space currently being used.
- **Mounted on** — The location where the filesystem is accessible.

`df -h` is useful for quickly checking whether a filesystem is running low on storage.

---

### 11. Reading System Files

Linux stores important system information in files, many of which can be viewed directly from the terminal.

#### `/etc` Directory

The `/etc` directory contains many system configuration and informational files.

For example:

    cd /etc

---

#### `/etc/issue`

The `/etc/issue` file can contain information displayed before login.

It can be read using:

    cat /etc/issue

---

#### `/etc/os-release`

The `/etc/os-release` file provides information about the Linux distribution.

    cat /etc/os-release

It can provide information such as:

- Distribution name
- Version
- Distribution ID

---

## Command Summary

| Command | Purpose |
|---|---|
| `pwd` | Show the current working directory |
| `ls` | List directory contents |
| `ls -l` | List files with detailed information |
| `ls -a` | Show hidden files |
| `cd <directory>` | Change directory |
| `cd ..` | Move to the parent directory |
| `find` | Locate files in the filesystem |
| `cat` | Read/display file contents |
| `whoami` | Display the current username |
| `uname -a` | Display detailed system information |
| `df -h` | Display disk/storage usage in human-readable format |
| `cat /etc/issue` | Read system issue/login information |
| `cat /etc/os-release` | Display Linux distribution information |
