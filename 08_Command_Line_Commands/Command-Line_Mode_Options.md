# Introduction to the Command Line

- The command line interface provides the following advantages:
    - No GUI overhead is incurred
    - Virtually any and every task can be accomplished while sitting at the command line.
    - Implement scripts for often-used (or easy-to-forget) tasks and series of procedures
    - Sign into remote machines anywhere on the Internet.
    - Initiate graphical applications directly from the command line instead of hunting through menus

# Using a Text Terminal on the Graphical Desktop

- A terminal emulator program emulates a standalone terminal within a window or desktop.
- On `GNOME`, the `gnome-terminal` is used
- Other available terminal applications:
    - `xterm`
    - `konsole (default on KDE)`
    - `terminator`

# Basic Utilities

- There are basic commands that are used constantly, such as:
    - `cat:` used to type out a file (or combine files)
    - `head:` used to show first few lines of a file
    - `tail:` used to show the last few lines of a file
    - `man:` used to view documentation
- the pipe (`|`) is used to have one program take as input the output of another

# The Command Line

- Most input lines entered at the shell prompt have three basic elements:
    - `Command:` the name of the program or script that is to be executed
    - `Option:` usually start with one or two dashes `-p` or `--print` to differetiate them from arguments
    - `Arguments:` represent what the commands operate to
- a command can have no option or argument
- other elements can also appear on the command line while launching a task     

# sudo

- Provide the user administrative privileges
- Allows users to run programs using the privileges of another user, usually the root

# Virtual Terminals (VT)

- Console sessions that use the entire display and keyboard outside a graphical environment 
- Can be multiple active terminals
- One virtual terminal (usually VT 1 or VT 7) is reserved for the graphical environment, and text logins are enabled on the unused VTs. 
- VTs are helpful when the graphical desktop is not working
- To switch between VTs, press `CTRL-ALT-function` key for the VT
- `CTRL-ALT-F6` for VT-6

![Switching Between Virtual Terminals](image.png)

# Turning Off the Graphical Desktop

- Can be turned off with command:
```bash
$ sudo systemctl stop gdm 
$ sudo telenit 3
```
- And restarted with:
```bash
$ sudo systemctl start gdm
sudo telenit 5
```