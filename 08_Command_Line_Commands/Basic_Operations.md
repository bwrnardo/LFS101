![Basic operations](image-1.png)

# Logging In and Out

- A terminal will prompt for a `login: ` and a `password: ` so you can perform basic operations
- Can also connect via remote system  using `Secure SHell (SSH)` 
    - Ex: `ssh student@remote-server.com` 
- `SSH` would connect to the remote machine `(remote-server.com)` and give `student` a command line window to sign in

# Rebooting and Shutting Down

- Preferred to shut down using the `shutdown` command to shut down properly
- The `init` will then take over the process
- The `halt` and `poweroff` commands issue `shutdown -h` to halt the system
- `reboot` issues `shutdown -r` 
- Requires root privileges
- When administering a multi-user system, you have the option of notifying all users prior to shutdown, as in:

```bash
$ sudo shutdown -h 10:00 "Shutting down for scheduled maintenance."
``` 

# Locating Applications 

- In general, executable programs live in `/bin, /usr/bin, /sbin, /usr/sbin` directories or in `/opt`
- Can also be in `/usr/local/bin` and `/usr/local/sbin` or `/home/student/bin`
- One way to locate the program is by using the `which` command

```bash
$ which diff
/usr/bin/diff
```

- Can also use the `whereis` command for deeper search

```bash
$ whereis diff
diff: /usr/bin/diff /usr/share/man/man1/diff.1.gz /usr/share/man/man1p/diff.1p.gz
```

# Acessing Directories 

- You can see the location of your home directory by typing `echo $HOME` 
- Most distributions open in `echo $HOME/Desktop`

- Commands useful for directory navigation: 

| COMMAND | RESULT |
| :--- | :--- |
| `pwd` | Displays the present working directory |
| `cd ~` or `cd` | Change to your home directory; shortcut name is ~ (tilde) |
| `cd ..` | Change to parent directory (..) |
| `cd -` | Change to previous working directory; - (minus) |

