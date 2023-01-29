# WSL Installation

> [Install WSL 2](https://learn.microsoft.com/en-us/windows/wsl/install)

Open PowerShell in administrator mode.

Set default wsl version 2.
```
 wsl --set-default-version 2
```
Install Ubuntu 20.04
```
 wsl --install -d Ubuntu-20.04
```
Set your username and passwd to Ubuntu terminal.
```
Installing, this may take a few minutes...

Please create a default UNIX user account. The username does not need to match your Windows username.
For more information visit: https://aka.ms/wslusers
Enter new UNIX username: jenkins-docker
New password:
Retype new password:
passwd: password updated successfully
Installation successful!
```
