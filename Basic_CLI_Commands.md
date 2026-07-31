# Basic CLI Commands

## What is CLI?

CLI (Command Line Interface) is a text-based interface that allows users to interact with the operating system by typing commands. Instead of clicking icons and buttons, users enter commands to perform tasks like creating files, managing folders, running programs, and controlling the system.

## Shell

A shell is a command-line interpreter that acts as a bridge between the user and the operating system. It understands the user's commands, sends them to the kernel for execution, and displays the output back to the user.

## Kernel

The kernel is the core part of the operating system. It receives commands from the shell, manages hardware resources like the CPU, memory, and storage, executes the requested tasks, and sends the results back to the user.


## Basic CLI Commands

### 1. View Command Documentation

Before using any command, we can read its documentation.

```bash
man ls
```

Exit the manual:

```bash
q
```

---

## 2. Check the Current Working Directory

```bash
pwd
```

Displays the current working directory.

---

## 3. Display the Current User

The `whoami` command displays the username of the currently logged-in user.

```bash
whoami
```

Example Output:

```text
alok-kumar
```

---

## 4. List Files and Directories

The `ls` command is used to list files and directories in the current location.

### Basic Command

```bash
ls
```

Displays the files and directories in the current working directory.

---

### View Hidden Files

```bash
ls -a
```

Displays all files, including hidden files (files starting with `.`).

---

### Long Listing Format

```bash
ls -l
```

Displays detailed information such as:
- File permissions
- Number of links
- Owner
- Group
- File size
- Last modified date and time
- File name

---

### Sort by Modification Time

```bash
ls -t
```

Displays files sorted by the most recently modified.

---

### Reverse the Sorting Order

```bash
ls -r
```

Displays files in reverse order.

---

### Human-Readable File Sizes

```bash
ls -lh
```

Displays file sizes in a human-readable format (KB, MB, GB).

---

### Combine Multiple Flags

```bash
ls -altrh
```

### Flag Explanation

- **a** → Show all files, including hidden files.
- **l** → Display detailed information (long listing format).
- **t** → Sort files by modification time.
- **r** → Reverse the sorting order.
- **h** → Display file sizes in a human-readable format.

---

## 5. Change Directory

The `cd` command is used to change the current working directory.

### Move into a directory

```bash
cd folder_name
```

Moves to the specified directory.

---

### Stay in the Current Directory

```bash
cd .
```

The `.` (dot) represents the current directory. This command keeps you in the same directory and is commonly used in scripts and with relative paths.

---

### Move to the Parent Directory

```bash
cd ..
```

The `..` (double dot) represents the parent directory.

---

### Go to the Home Directory

```bash
cd ~
```

The `~` (tilde) represents the current user's home directory.

---

### Go Back to the Previous Directory

```bash
cd -
```

Returns to the previously visited directory.

---

### Go to the Root Directory

```bash
cd /
```

Moves to the root (`/`) directory of the file system.

## Difference Between Root Directory and Home Directory

| Root Directory (`/`) | Home Directory (`/home/alok-kumar`) |
|-----------------------|--------------------------------------|
| It is the top-most directory in the Linux file system. | It is the personal directory of a user. |
| All files and directories start from the root directory. | It contains the user's personal files, folders, Downloads, Documents, etc. |
| Represented by `/`. | Usually represented by `~` in the terminal. |
| Shared by the entire operating system. | Belongs to a specific user. |




---

## 6. Create a New Directory

```bash
mkdir demo
```

Create nested directories:

```bash
mkdir -p project/src/components
```

---

## 7. Create One or More Empty Files

```bash
touch file.txt
```

Create multiple files:

```bash
touch file1.txt file2.txt file3.txt
```

---

## 8. Write Text to a File

The `echo` command is used to display text or write text into a file.

### Display Text

```bash
echo "Hello, Linux!"
```

Output:

```text
Hello, Linux!
```

---

### Write Text to a File

```bash
echo "Hello, Linux!" > file.txt
```

The `>` operator creates the file (if it doesn't exist) or overwrites its existing content.

---

### Append Text to a File

```bash
echo "Welcome to CLI" >> file.txt
```

The `>>` operator adds new content to the end of the file without removing the existing content.

---

## 9. View File Contents

```bash
cat file.txt
```

Large file:

```bash
less file.txt
```

or

```bash
more file.txt
```

---

## 10. Copy Files and Directories

Copy a file:

```bash
cp file.txt backup.txt
```

Copy a directory:

```bash
cp -r project backup
```

---

## 11. Move or Rename Files

Rename:

```bash
mv old.txt new.txt
```

Move:

```bash
mv file.txt Documents/
```

---

## 12. Remove Files and Directories

Delete a file:

```bash
rm file.txt
```

Delete an empty directory:

```bash
rmdir demo
```

Delete a directory with contents:

```bash
rm -r project
```

---

## 13. Count Lines, Words, and Characters

The `wc` (Word Count) command is used to count the number of lines, words, and characters in a file.

### Count Lines, Words, and Characters

```bash
wc file.txt
```

Example Output:

```text
5  20  120  file.txt
```

Where:

- **5** → Number of lines
- **20** → Number of words
- **120** → Number of characters (bytes)

---

### Common Flags

Count the number of lines:

```bash
wc -l file.txt
```

Count the number of words:

```bash
wc -w file.txt
```

Count the number of characters (bytes):

```bash
wc -c file.txt
```

### Flag Explanation

- **-l** → Count the number of lines.
- **-w** → Count the number of words.
- **-c** → Count the number of characters (bytes).

---

## 14. Sort File Content

```bash
sort names.txt
```

---

## 15. View the First Lines of a File

The `head` command is used to display the first 10 lines of a file by default.

```bash
head file.txt
```

Display the first 5 lines:

```bash
head -n 5 file.txt
```

---

## 16. View the Last Lines of a File

The `tail` command is used to display the last 10 lines of a file by default.

```bash
tail file.txt
```

Monitor a file in real time (commonly used for log files):

```bash
tail -f log.txt
```

---

## 17. Display Date and Time

```bash
date
```

Displays the current system date and time.

---

## 18. Display Directory Structure

```bash
tree
```

Displays the directory structure in a tree-like format.

If `tree` is not installed:

```bash
sudo apt install tree
```

---

## 19. Clear the Terminal

```bash
clear
```

Clears the terminal screen.

---

## 20. View Command History

The `history` command displays the list of previously executed commands.

```bash
history
```

Search command history interactively:

```bash
Ctrl + R
```

Type a keyword after pressing `Ctrl + R` to search for a previously executed command.