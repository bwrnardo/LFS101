# Viewing Files

| Command | Usage |
| :--- | :--- |
| cat  |  For viewing files that are not very long; it does not provide any scroll-back.
| tac  |  Look at a file backwards, starting with the last line.
| less |  View larger files because it is a paging program. It pauses at each screen full of text, provides scroll-back capabilities, and lets you search and navigate within the file
| tail |  Print the last 10 lines of a file by default. Change the number of lines by doing -n 15 or just -15 if you wanted to look at the last 15 lines instead of the default.
| head | The opposite of tail; by default, it prints the first 10 lines of a file.

# **touch**

- Used to set or update the acess, change, and modify time of files.
- Resets a timestamp to the current date
- Can also create empty files with 
```bash
$ touch <filename>
```
- The `-t` option allows to set a especific timestamp
```bash
$ touch -t 12091600 myfile
```
- Sets **myfile** timestamp to (12 09 1600)

# **mkdir** and **rmdir**

- `mkdir` is used to create a directory
```bash
$ mkdir sampdir
```
- Creates a sample directory named `sampdir` under the current directory. 
```bash
$ mkdir /usr/sampdir 
```
- Creates a sample directory called `sampdir` under `/usr`.

- Remove a empty directory with `rmdir`
- Remove a directory with content with `rm -rf`

# Moving, Renaming or Removing a File

|Command | Usage
| :--- | :--- |
|`mv` | Rename a file
|`rm`	| Remove a file
|`rm -f` | Forcefully remove a file
|`rm -i` | Interactively remove a file 

- `mv` also moves a file to another location

# Modifying the Command Line Prompt

- `PS1` variable is the character string that is displayed as the prompt on the command line.
- Set as default in most distributions

- To change what is shown in the CLI, can be implemented as: 
```bash
$ echo $PS1
\$
$ PS1="\u@\h \$ "
student@r9 $ echo $PS1
\u@\h \$
student@r9 $
```