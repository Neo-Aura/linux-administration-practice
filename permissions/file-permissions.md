# Linux File Permissions

## 1. Overview

Linux file permissions control who can read, modify, or execute files and directories.

There are three permission categories:

- **User (u):** The file owner
- **Group (g):** Users in the file's group
- **Others (o):** Everyone else

## 2. Permission Types

| Permission | Symbol | Numeric Value |
|---|---|---:|
| Read | r | 4 |
| Write | w | 2 |
| Execute | x | 1 |
| No permission | - | 0 |

## 3. Check Permissions

Use `ls -l` to view file permissions.

```bash
ls -l
```

Example output:

```text
-rw-r--r-- 1 user user 120 Oct 25 10:00 notes.txt
```

The permission string `-rw-r--r--` means:

- Owner: read and write
- Group: read only
- Others: read only

## 4. Change Permissions with chmod

Give the owner read, write, and execute permissions:

```bash
chmod 700 script.sh
```

Give the owner read/write permissions and allow the group and others to read:

```bash
chmod 644 notes.txt
```

Add execute permission for the owner:

```bash
chmod u+x script.sh
```

## 5. Change File Ownership

Check the current owner and group:

```bash
ls -l notes.txt
```

Change ownership using `chown` (requires appropriate privileges):

```bash
sudo chown newuser:newgroup notes.txt
```

Use example usernames and groups that exist on your own test system.

## 6. Practice Tasks

1. Create a file named `practice.txt`.
2. Check its permissions with `ls -l`.
3. Change its permissions to `600`.
4. Change them to `644`.
5. Explain the difference between these two permission settings.
6. Create a test script and add execute permission for its owner.

## 7. Key Learning

Use `chmod` to modify permissions and `chown` to change ownership. Apply permission changes carefully, especially on production systems.

**Learning status:** Update these notes with your own tested commands and observations.
