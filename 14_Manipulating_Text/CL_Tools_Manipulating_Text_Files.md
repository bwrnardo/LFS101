# `cat` 

- short for **concatenate**
- to view a file, it has the form:

```bash
$ cat <filename> 
```
- its main purpose is to combine multiples files together: 

![commands and usage of cat](images/image.png)

- `tac`: `cat` spelled backwards is a command to print the lines in reverse order

```bash
$ tac file
$ tac file1 file2 > newfile
```
## Using `cat` interactively

- To create a new file type `cat > <filename>` and press enter
    - After that, the command waits for the user to edit/enter the text
- `CTRL-D` to save and exit the editing

# `echo`

- `echo` simply echoes text 

```bash
$ echo string
string
```

- can be used to append a string to an already existing file using the `>>` operator
- 