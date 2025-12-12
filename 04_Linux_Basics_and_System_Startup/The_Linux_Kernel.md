# The Linux Kernel

- When the kernel is loaded in RAM, it initializes and configures the computer's memory and all the hardware attached
- Also loads necessary space applications
- Runs the `init` process, which is responsible for starting other process to launch the full system

## Init

- Starts at `/sbin/init`
- Responsible for keeping the system running and shutting it down
- Resonsible for starting system and network services at boot time
- Act when necessary as a manager for all non-kernel process
- Cleans itself after completion

## Startup Alternatives

- `SysVinit` is an older start process
- `Upstart`
    - Developed by Ubuntu and first included in 2006
    - Adopted by Fedora 9 in 2008 and in RHEL 6 and its clones
- `systemd`
    - Adopted by Fedora first in 2011
    - Adopted by RHEL 7 and SUSE
    - Replaced Upstart in Ubuntu 16.04
    - It has been adopted by all major distributions 
    - Star up faster than older `init` process
    - Permits multiple services to be initiated simultaneously
    - Points to `/lib/systemd/systemd`
    - `systemctl` is used for most basic tasks
        - Starting, stopping, restarting a service
        ```bash
        $ sudo systemctl start|stop|restart httpd.service
        ```
        - Enabling or disabling a system service from starting up at system boot
        ```bash
        $ sudo systemctl enable|disable httpd.service
        ```
        - Checking on the status of a service
        ```bash
        $ sudo systemctl status httpd.service
        ```