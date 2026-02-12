# File Manipulation Utilities

## `sort`

- used to rearrange the lines of a text file in either ascending or descending order

![sort](images/image-7.png)

- the `-u` option checks for unique values after sorting the lines

## `uniq` 

- removes duplicate consecutive lines in a text file
- used with `sort` to pipe the output 

```bash
$ sort file1 file2 | uniq > file3
$ sort -u file1 file2 > file3
$ uniq -c filename
```

## `paste`

- used to create files joining columns with other files

![paste](images/image-8.png)

- `-d` delimiters specify a list of delimiters to be used instead of tabs for separating consecutive values on a single line
- `-s` causes paste to append the data in series rather than in parallel

- to paste contents from two files:

```bash
$ paste file1 file2
$ paste -d, file1 file2
```

## `join`

- it first checks whether the files share common fields, such as names or phone numbers
- then joins the lines in two files based on a common field

![join](images/image-9.png)

- to combine two files on a common field:

```bash
$ join file1 file2
```

## `split`

- used to break up a file into equal-sized segments for easier viewing and manipulation
- `split` breaks up a file into 1000-line segments by default
- the original file remains unchanged and a set of new files is created 

![alt text](images/image-10.png)

- `lswords` will be split into `lswordsxx`:

```bash
$ split linux.words lwords
```