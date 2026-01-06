# Standard File Streams

- When commands are executed, by default there are three standard file streams

| Name	| Symbolic Name	 | Value | Example
| :--- | :--- | :--- | :--- |
|standard input	| `stdin` | 0	| keyboard
|standard output | `stdout` |	1 | terminal
|standard error	| `stderr` | 2 | log file

# I/O Redirection

- If we have a program called `do_something` that reads from `stdin` and writes to `stdout` and `stderr`, we can change its input source by using the `<` sign followed by the name of the file to be consumed for input data:

```bash
$ do_something < input-file
```

- To send the output to a file, use the `>` sign as in:

```bash
$ do_something > output-file
```

- Can do both at the same time as in:

```bash
$ do_something < input-file > output-file
```

- `stderr` is not the same as `stdout`, error messages will still be seen on the terminal windows in the above example.

- to redirect `stderr` to a separate file, you use `stderr`’s file descriptor number `(2)`, the `>` sign, followed by the name of the file you want to receive everything the running command writes to `stderr`:

```bash
$ do_something 2> error-file
```

- `do_something 1> output-file` is the same as `do_something > output-file.`

- A special shorthand notation can send anything written to file descriptor 2 `(stderr)` to the same place as file descriptor 1 `(stdout)`: `2>&1`.

```bash
$ do_something > all-output-file 2>&1
```

- bash permits an easier syntax for the above:

```bash
$ do_something >& all-output-file
```

# Pipes


- Pipes are used to separate process without having to wait for previous pipelines to complete their task
- The computing power available is utilized efficiently and quicker

```bash
$ command1 | command2 | command3
```

# locate

- `locate` performs a search of a previously constructed database of files and directories
- `grep` will print only the lines that contain one or more specified arguments

```bash
$ locate zip | grep bin
```

- `updatedb` is the database created by `locate`, most Linux distributions run automatically
    - Needs root privileges

# Wildcards and Matching Filenames

- You can search for a filename containing specific characters using wildcards.

| Wildcard | Result
| :--- | :---
| `?`	| Matches any single character
| `*`| Matches any string of characters
| `[set]` | Matches any character in the set of characters, for example [adf] will match any occurrence of a, d, or f
| `[!set] `| Matches any character not in the set of characters

- `?` is used to files you don't know the full name, like `myfi??.out` will find `myfile.out`
- `*` is used to files you don't remember at all, `*.out` will find `myfile.out`

# **find**

- `find` command recurses down the filesystem tree from anywhere
- Administrators scan for potentially large core files that are more than several weeks old in order to remove them
- When not given arguments, lists everything in every directory
- `-name` lists only files with a pattern in their name
- `-iname` ignore the file names
- `-type` restrict the results to files of a certain specified type, such as `-d` for directory, `-l` for symbolic link, or `-f` for a regular file, etc

## Using **find**

```bash
$ find /usr -name gcc

$ find /usr -type d -name gcc

$ find /usr -type f -name gcc
```

## Advanced **find** Options

- `-exec` run commands with your argument
    - Find and remove all files that end with .swp:
```bash
$ find -name "*.swp" -exec rm {} ';'
```

- `-ok` is the same as `-exec` but will prompt a confirmation

## Finding Files Based on Time and Size

- Find files based on time: 
    - `-ctime` will find the item based on the time it was created
    - `-atime` will find the item based on last acessed time
    - `-mtime` will find the item based on last modified time

- Can also be searched in minutes
    - `-cmin`, `-amin`, `-mmin` 

```bash
$ find / -ctime 3
```
    
- Find files based on size: 
    - bytes `(c)`, kilobytes `(k)`, megabytes `(M)`, gigabytes `(G)`, etc
    - exact numbers `(n)`, `+n`, `-n`

```bash
$ find / -size 0

$ find / -size +10M -exec command {} ’;’
```