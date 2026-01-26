# Comparing Files with `diff`

- `diff` is used to compare files and directories
- To compare two files, use `diff [options] <filename1> <filename2>`
- `diffuse`, `vimdiff` and `meld` are GUI to `diff`

|`diff` Option |	Usage
| :--- | :---
|`-c`	 | Provides a listing of differences that include three lines of context before and after the lines differing in content
|`-r`	 | Used to recursively compare subdirectories, as well as the current directory
|`-i`	| Ignore the case of letters
|`-w`	| Ignore differences in spaces and tabs (white space)
|`-q`	| Be quiet: only report if files are different without listing the differences

# Using `diff3` and `patch`

- `diff3` is for comparing three files at once
- Using one file as reference to the other two

```bash
$ diff3 MY-FILE COMMON-FILE YOUR-FILE
```

- `patch` is a file that contain the changes made 
- To see the patchfiles:

```bash
$ diff -Nur originalfile newfile > patchfile
```

- To apply a patch, updating a older version to the new one:

```bash
$ patch -p1 < patchfile
$ patch originalfile patchfile
```

# Using the file Utility

- A file's extension does not, by default, categorize its nature the way it might in other operating systems
-  For example, one cannot assume that a file named `file.txt` is a text file and not an executable program.
- most applications directly examine a file's contents to see what kind of object it is rather than relying on an extension.
- The nature of a file can be seen using `file` 