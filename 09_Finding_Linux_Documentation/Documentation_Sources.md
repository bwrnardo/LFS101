# Linux Documentation Sources

- Important Linux documentation sources include:
    - The **man** pages (short for manual pages)
    - GNU Info
    - The `help` command and `--help` option
    - Other documentation sources, e.g., *Gentoo Handbook*, *Ubuntu Documentation*, or *Fedora Documentation*.

![Linux Documentation Sources](image.png)

# The **man** Pages

- Provide in-depth documentation about many program utilities such as:
    - Configuration files and programming APIs for system calls
    - Library routines
    - The kernel

- Present on all distributions
- **man** is abreviation for manual

# **man**
 
- Searches, formats and displays the information contained in the **man** page system
- `-f` to list all pages in the topic
- `-k` to list all pages of a specific topic
    - `man –f` generates the same result as typing `whatis`.
    - `man –k` generates the same result as typing `apropos`.

# Manual Chapters

- The man pages are numbered 1 through 9
- A letter is appended to the chapter number to identify a specific topic
- With the -a parameter, man will display all pages with the given name in all chapters, one after the other, as in:
```bash
$ man -a socket
``` 
    