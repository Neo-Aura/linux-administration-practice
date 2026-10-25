# Basic Linux Commands

## 1. Introduction

These notes cover common Linux commands used for navigation, file management, system information, and troubleshooting.

## 2. Navigation Commands

### `pwd`
Displays the current working directory.

```bash
pwd
```

### `ls`
Lists files and directories.

```bash
ls
ls -la
```

### `cd`
Changes the current directory.

```bash
cd /home
cd ..
cd ~
```

## 3. File and Directory Management

### `mkdir`
Creates a directory.

```bash
mkdir practice
```

### `touch`
Creates an empty file if it does not exist.

```bash
touch notes.txt
```

### `cp`
Copies files.

```bash
cp notes.txt notes-backup.txt
```

### `mv`
Moves or renames files.

```bash
mv notes.txt linux-notes.txt
```

### `rm`
Removes files. Use carefully.

```bash
rm linux-notes.txt
```

## 4. Viewing File Contents

```bash
cat notes.txt
less notes.txt
head notes.txt
tail notes.txt
```

- `cat` displays file contents.
- `less` allows scrolling through a file.
- `head` displays the first lines.
- `tail` displays the last lines.

## 5. System Information

```bash
whoami
hostname
uname -a
date
df -h
free -h
```

- `whoami` displays the current username.
- `hostname` displays the system hostname.
- `uname -a` displays kernel and system information.
- `df -h` displays filesystem disk usage.
- `free -h` displays memory usage.

## 6. Searching

```bash
find . -name "*.txt"
grep "error" application.log
```

- `find` searches for files and directories.
- `grep` searches text for matching patterns.

## 7. Practice Tasks

1. Display your current directory.
2. Create a directory named `linux-lab`.
3. Create a file named `practice.txt` inside it.
4. Write some text into the file and display its contents.
5. Find all `.txt` files in your practice directory.
6. Check disk usage and available memory.

## 8. Learning Notes

Add your own tested examples, command output, and troubleshooting observations as you practice.

**Safety:** Practice file deletion commands only inside a test directory. Avoid using destructive commands on important system files.
