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

# **man**
 
- Searches, formats and displays the information contained in the **man** page system
- `-f` to list all pages in the topic
- `-k` to list all pages of a specific topic
    - `man –f` generates the same result as typing `whatis`.
    - `man –k` generates the same result as typing `apropos`.

# Manual Chapters

- The man pages are numbered 1 through 9
- A letter is appended to the chapter number to identify a specific topic
- With the `-a` parameter, man will display all pages with the given name in all chapters, one after the other, as in:
```bash
$ man -a socket
``` 
    
# GNU Info

- The GNU project alternative to **man**
- `info` works like `man`, but topics are connected using links
- View help for a topic typing `info <topic name>`
    - The system then searches for the topic in all available `info` files
    - `q` to quit, `h` for help, `Enter` to select a menu item

## **info** Page Structure

- The topic which you view in an info page is called a node.
- Items function like browser links are identified by and asterisk `*`
- Named items are identified with double-colon (::)

| Key | Function  
| :--- | :--- 
| n | Go to the next node 
| p | Go to the previous node 
| u | Move one node up in the index 

# The `--help` option

- Help gives a short description of the command

```bash
$ man --help
```

- Useful as a quick reference 
- Displays information faster

# Other Documentation Sources

- Desktop help system
- Package documentation
- Online resources

![Other Documentation Sources](image-1.png)

- There are also graphical help systems
- Such as: 
    - GNOME: `gnome-help` or `yelp`
    - KDE: `khelpcenter`

- Online Resources:    
    * [Ubuntu Documentation](http://help.ubuntu.com/)
    * [CentOS Documentation](https://docs.centos.org/)
    * [openSUSE Documentation](https://doc.opensuse.org/)
    * [Gentoo Documentation](https://www.gentoo.org/support/documentation/)
    * [Fedora Documentation](https://docs.fedoraproject.org/en-US/docs/)