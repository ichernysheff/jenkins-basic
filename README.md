# Basic Jenkins in Docker

- Install WSL2
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

- Install Docker

> [Install Docker](https://docs.docker.com/engine/install/ubuntu/)
> [Post Install](https://docs.docker.com/engine/install/linux-postinstall/)

```
sudo apt-get update
```
```
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```
```
sudo mkdir -p /etc/apt/keyrings
```
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```
```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
```
sudo apt-get update
```
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin docker-compose
```
Add your user to docker group and logout.
```
sudo usermod -aG docker $USER
```
Start docker service
```
sudo service docker start
```
Run hello world container
```
docker run hello-world
```
