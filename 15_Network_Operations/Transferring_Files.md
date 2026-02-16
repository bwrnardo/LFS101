# FPT (File Transfer Protocol)

- A built on client-server model 
- Used when security is not a concern

![FTP](images/image-9.png)

## FTP Clients

- Enables you to transfer files with remote computers
- Some command lines FPT clients are:
    - `ftp`
    - `sftp`
    - `ncftp`
    - `yafc (Yet Another FTP Client)`

![FTP Clients](images/image-10.png)

## SSH: Executing Commands Remotely

- Used for secure data communication 
- Used for remote services and other secure services on the network

![SSH](images/image-11.png)

- `ssh some_system` to login a remote system
- `ssh -l someone some_system` to run as another user

## Copying Files Securely with `scp`

- `scp <localfile> <user@remotesystem>:/home/user` to copy a local file into a remote system

![scp](images/image-12.png)